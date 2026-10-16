# Rec Studios GitHub Pages status feed

## Publish the feed

1. On GitHub, create a **public** repository named `recstudios-status` and choose to add a README.
2. Upload `index.html` and `status.json` from this folder to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch **main** and folder **/(root)**, then click **Save**.
6. Wait for Pages to publish. Your JSON feed will be:
   `https://YOUR-GITHUB-USERNAME.github.io/recstudios-status/status.json`
7. Replace `YOUR-GITHUB-USERNAME` in `recstudios/Script/status-config.js` with your GitHub username.
8. Publish the updated Rec Studios website files to its hosting provider.

Edit `status.json` whenever a service changes. Commit the update to the repository and Pages will republish it. The statuses supported are `operational`, `degraded`, `outage`, `maintenance`, and `unknown`. `overall` uses one of the same values. Each component needs an `id`, `name`, and `status`; `latencyMs` can be a number or `null`.

GitHub Pages hosts a static JSON file; it does not monitor servers by itself. This setup displays the status you enter in `status.json`.
