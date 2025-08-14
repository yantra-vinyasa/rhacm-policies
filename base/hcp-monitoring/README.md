# HCP Monitoring

This directory contains resources for monitoring Hosted Control Planes (HCP).

For more information, refer to the Red Hat Knowledge Base article:
[How to deploy and configure the Hypershift Operator dashboard](https://access.redhat.com/solutions/7106136)

## Bypassing Template Processing

By default, Red Hat Advanced Cluster Management for Kubernetes processes all Go templates within policies. However, you might need to prevent this processing, for instance, when a template is intended for a different templating engine.

 **Disable Templates for an Entire `ConfigurationPolicy`:**
    To completely disable template resolution for a specific `ConfigurationPolicy`, add the following annotation to the `ConfigurationPolicy` resource that is defined within your main `Policy` resource.

    -   **Annotation:**
        ```yaml
        metadata:
          annotations:
            policy.open-cluster-management.io/disable-templates: "true"
        ```

For more information, see the [Red Hat Advanced Cluster Management for Kubernetes documentation](https://docs.redhat.com/en/documentation/red_hat_advanced_cluster_management_for_kubernetes/2.13/html/governance/governance#bypass-template-processing).
