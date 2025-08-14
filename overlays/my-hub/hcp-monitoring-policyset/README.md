# HCP Monitoring Policyset

This policyset enables monitoring for Hosted Control Planes (HCP) on OpenShift.

## Policies

This policyset applies the following configurations to the managed clusters:

1.  **Enable Monitoring Dashboards**: Creates a `ConfigMap` named `hypershift-operator-install-flags` in the `local-cluster` namespace. This enables the monitoring dashboards for each hosted cluster managed by the HyperShift Operator.

2.  **Configure Metrics Set**: Enforces the `METRICS_SET` environment variable in the `hypershift-operator` deployment in the `hypershift` namespace. The value is set to `SRE`, which includes metrics for producing alerts and troubleshooting control plane components.

## Usage

This policyset is applied to the `local-cluster` (the hub cluster) where the HyperShift Operator is running.
