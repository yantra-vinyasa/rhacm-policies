# OpenShift GitOps Base Configuration

This directory contains the base Kustomize configuration for deploying and configuring OpenShift GitOps (Argo CD) via ACM (Advanced Cluster Management) policies.

OpenShift GitOps enables users to deploy and manage applications and cluster configuration in a reliable and consistent fashion using the GitOps methodology. It leverages standard Git workflow practices to enable teams to monitor configuration drift with optional automatic remediation as well as providing increased visibility and audit for changes.

## Components

This base configuration is divided into three main components:

*   **`operator/`**: Deploys the OpenShift GitOps operator from the OperatorHub.
*   **`instance/`**: Creates the `ArgoCD` custom resource, which provisions an Argo CD instance. It also includes necessary configurations like the namespace and cluster role bindings.
*   **`appofapps/`**: Deploys a bootstrap "app-of-apps" `Application` resource. This application is intended to point to a Git repository that defines the applications for a specific cluster.

# Purpose of the Policy

Install and configure the **Red Hat OpenShift GitOps Operator** (ArgoCD) on all HCP clusters.

# Notes
- The **Red Hat OpenShift GitOps Operator** (ArgoCD)  is instlaled on the Hub clusters using the **boostrap process**

## Link of interest 
* [Getting Started with OpenShift GitOps](https://developers.redhat.com/blog/2025/05/28/getting-started-openshift-gitops#)
* [OpenShift Demos: OpenShift GitOps Workshop Examples](https://github.com/OpenShiftDemos/openshift-gitops-workshop/tree/main/content/modules/ROOT/examples)
* [OpenShift GitOps recommended practices](https://developers.redhat.com/blog/2025/03/05/openshift-gitops-recommended-practices#)
 