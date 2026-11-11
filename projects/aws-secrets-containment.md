# AWS Automated Secrets Access Defense Lab & Containment
**Architecture Model:** Event-Driven Serverless Compliance Defense  
**Core Framework:** NIST CSF DE.CM (Continuous Security Monitoring)

---

## Architecture Diagram Overview
```
[Attacker API Call] 
       │ (GetSecretValue)
       ▼
[AWS Secrets Manager] ──► [CloudTrail Logs] ──► [EventBridge Rule]
                                                      │
                                                      ├─► [SNS Alert Email]
                                                      ▼
                                            [Python Lambda Kill-Switch]
                                                      │
                                                      ▼
                                            [Detach Attacker IAM Policies]
```

---

## Technical Project Narrative
This project simulates an internal credential leakage scenario. A "honeytoken" database credential secret (`Production_Database_Credentials`) was intentionally positioned inside AWS Secrets Manager to capture attacker scanning patterns.

### Detection Mechanisms Created
1.  **Metric Filtering (CloudWatch):** Constructed thresholds to track calls to the `GetSecretValue` API.
2.  **Real-Time Trigger (EventBridge):** Processed the real-time event JSON stream for near-zero delay analysis.

### Active Serverless Response Logic (Python AWS SDK)
Once an unauthorized source initiated an access attempt, EventBridge captured the activity and triggered a Lambda container within seconds.

The deployed Python script parsed the event structure, identified the offending user profile, and programmatically isolated it:

```python
import boto3
import json

def lambda_handler(event, context):
    iam_client = boto3.client('iam')
    # Extract the user profile initiating the call
    user_identity = event['detail']['userIdentity']['userName']
    
    print(f"Target Intruder Identified: {user_identity}")
    
    # Detach attached policies to neutralize access
    attached_policies = iam_client.list_attached_user_policies(UserName=user_identity)
    for policy in attached_policies['AttachedPolicies']:
        iam_client.detach_user_policy(
            UserName=user_identity,
            PolicyArn=policy['PolicyArn']
        )
    print("Intruder isolated successfully.")
```

### Verification Evidence
During simulations, the attacker succeeded on their initial attempt. However, within seconds, the Lambda script completed the containment sequence. The attacker's subsequent API calls returned an immediate `AccessDeniedException` response.


## Interactive Demonstration
This browser-based walkthrough demonstrates the detection, notification and containment sequence using simulated events. It does not connect to AWS or change any cloud resources.

[Launch the AWS Response Flow Simulator →](../demos/aws-response-simulator.html)
