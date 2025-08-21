# HCP Chrony Configuration Policies

This directory contains a set of policies to configure Chrony on Hosted Control Plane (HCP) clusters managed by Red Hat Advanced Cluster Management (RHACM).

## Policies

The following policies are included:

- **hcp-chrony-cm-chrony-machineconfig**: This policy creates a `ConfigMap` containing a `MachineConfig` object. The `MachineConfig` sets the Chrony configuration for worker nodes.

- **hcp-chrony-nodepool-worker**: This policy applies the `MachineConfig` to the `nodepool-worker` `NodePool` in each Hosted Cluster.

## Prerequisites

- A running instance of Red Hat Advanced Cluster Management (RHACM).
- Hosted Clusters managed by RHACM.

## Usage

To use these policies, apply them to your RHACM hub cluster. The policies will automatically discover and configure all Hosted Clusters.

## How to update the Chrony configuration

The chrony configuration is stored as a base64 encoded, gzipped string in `cm-chrony-machineconfig.yaml`. To update it:

1.  Modify the `dummy-data/dummy-chrony.conf` file with your desired configuration.
2.  Generate the new base64 string by running the following command from the `base/hcp-chrony` directory:

    ```bash
    gzip -c dummy-data/dummy-chrony.conf | base64
    ```

3.  Replace the `source` value in `cm-chrony-machineconfig.yaml` with the new string.