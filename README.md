# IDP PoC Apps

This repository demonstrates a **GitOps** workflow using **ArgoCD** and **Backstage**.

## Structure

*   **`charts/static-web`**: A Helm chart for deploying static websites with Nginx.
*   **`apps/`**: ArgoCD Application manifests. Each file here represents a deployed application.
*   **`app-values/`**: Value overrides and HTML content for each application.
*   **`root-app.yaml`**: The "App of Apps" entry point for ArgoCD.

## Usage

1.  Connect this repo to ArgoCD.
2.  Apply `root-app.yaml` to the cluster.
3.  ArgoCD will automatically discover and deploy all apps defined in `apps/`.
