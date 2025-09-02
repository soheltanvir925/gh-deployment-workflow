This repository is a sample project that demonstrates how to automatically deploy a simple static website to GitHub Pages using a powerful Continuous Integration/Continuous Deployment (CI/CD) workflow with GitHub Actions.

This is an ideal starting point for anyone looking to automate the deployment of a portfolio, landing page, or personal blog.

Key Features
Automated Deployment: Any push to the main branch automatically triggers the deployment.

Efficient Workflow: The workflow is configured to only run when changes are made to the static website files, saving build time and resources.

Best Practices: Uses the modern and official actions/deploy-pages method for seamless integration with GitHub Pages.

How It Works
The core of this project is the GitHub Actions workflow file located at .github/workflows/deploy.yml. This file defines the steps needed to get your website from the repository to a live URL.

The workflow performs the following actions:

Trigger: It is triggered by a push to the main branch.

Permissions: It requests the necessary permissions to read your repository's content and deploy to GitHub Pages.

Checkout: It uses actions/checkout@v4 to get a copy of your repository's code.

Setup Pages: It configures the GitHub Pages environment.

Upload Artifact: It takes your website files and uploads them as a temporary artifact for deployment.

Deploy: It uses actions/deploy-pages@v4 to publish the artifact to your GitHub Pages URL.

Step-by-Step Deployment Guide
Follow these steps to get your website deployed and live.

1. Configure the Workflow
Open the .github/workflows/deploy.yml file.

Optional: If your static files are not in the root directory (e.g., in a folder named docs or public), change the path: '.' line under the Upload artifact step to path: 'docs' (or your folder's name).

2. Commit and Push
Make sure your index.html file and the deploy.yml workflow file are in your main branch.

Commit and push your changes to the repository.

3. Enable GitHub Pages
The final step is to tell GitHub to use the GitHub Actions workflow for deployment.

Go to your repository on GitHub.

Click the Settings tab.

In the left sidebar, click on Pages.

Under the Build and deployment section, select GitHub Actions as the source.

Click Save.

That's it! After a few moments, the workflow will run and you will be able to access your live website at a URL like:

https://soheltanvir925.github.io/gh-deployment-workflow/

You can track the deployment progress by clicking on the Actions tab in your repository.
