# Building and Deploying the Spec

This directory contains the spec and its generated output. The spec uses spec-up for rendering.

## Manual Build Process

To build the spec locally:

1. Ensure you're in the project root directory
2. Install dependencies:
   ```bash
   npm install
   ```
3. Run the render command:
   ```bash
   npm run render
   ```

## Deployment Process

The spec is deployed using GitHub Actions. To deploy:

1. Go to the "Actions" tab in the GitHub repository
2. Find the "Deploy static content to Pages" workflow
3. Click "Run workflow"
4. Select the branch you want to deploy from (e.g., "initial-spec-draft")
5. Click "Run workflow"

The workflow will build and deploy the spec to GitHub Pages. You can monitor the deployment progress in the Actions tab.

Note: The generated index.html is checked into the repository, so you can also view changes locally after building.
