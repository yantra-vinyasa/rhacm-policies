# Purpose of the Policy

Install and configure the External Secrets Operator on all HCP clusters.

External Secrets Operator is a Kubernetes operator that integrates external secret management systems like **GitLab Variables**, Hashicorp Vault and many others.
The operator reads information from external APIs and automatically injects the values into a Kubernetes secret.

# Notes
- The External Secrets Operator is instlaled on the Hub clusters using the **boostrap process**

## Links
- [External Secrets Operator integrates with GitLab](https://external-secrets.io/latest/provider/gitlab-variables/)
- [ESO Secret Types](https://external-secrets.io/latest/guides/common-k8s-secret-types/)
- [Red Hat Blog: How an External Secrets Operator fetches the GitLab CI variable](https://www.redhat.com/en/blog/how-to-feed-external-secrets-for-kubernetes-applications-with-the-external-secret-operator-and-gitlab-on-red-hat-openshift)
 