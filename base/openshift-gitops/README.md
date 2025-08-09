# OpenShift GitOps Base Configuration

This directory contains the base Kustomize configuration for deploying and configuring OpenShift GitOps (Argo CD) via ACM (Advanced Cluster Management) policies.

## Components

This base configuration is divided into three main components:

*   **`operator/`**: Deploys the OpenShift GitOps operator from the OperatorHub.
*   **`instance/`**: Creates the `ArgoCD` custom resource, which provisions an Argo CD instance. It also includes necessary configurations like the namespace and cluster role bindings.
*   **`appofapps/`**: Deploys a bootstrap "app-of-apps" `Application` resource. This application is intended to point to a Git repository that defines the applications for a specific cluster.
