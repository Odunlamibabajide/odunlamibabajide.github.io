# Cybersecurity GRC Portfolio — project pages and demos

## Package contents
- `index.html`: the updated portfolio homepage (existing design retained).
- `projects/`: 11 Markdown case studies used by the site's existing project-detail routes.
- `demos/risk-assessment-simulator.html`: illustrative 5×5 risk scoring tool with CSV export.
- `demos/aws-response-simulator.html`: simulated AWS detection-to-containment walkthrough; it does not connect to AWS.

## Publish on GitHub Pages
1. Open the repository `Odunlamibabajide/odunlamibabajide.github.io`.
2. Upload `index.html` to the repository root, replacing the existing homepage.
3. Upload the complete `projects` folder and the complete `demos` folder to the repository root. Keep the folder names exactly as shown.
4. Commit the changes to the branch used by GitHub Pages (usually `main`).
5. Wait for the Pages deployment to finish, then test the homepage, at least two project cards, and both demo links.

Project case studies are available through the existing hash routes, e.g. `/#projects/aws-secrets-containment`. The project Markdown files are fetched from `projects/` and the existing embedded fallback remains in the homepage.

## Evidence integrity
The demos are explicitly illustrative. The AWS simulator does not perform AWS actions. Do not publish client records, real credentials, private IPs, or unredacted screenshots. Add genuine screenshots, diagrams, Packet Tracer files, sanitized configuration samples, and reports only when you have verified them and have permission to share them.
