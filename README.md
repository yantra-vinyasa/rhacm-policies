# RHACM Policies

## Overview
Policies in Red Hat Advanced Cluster Management for Kubernetes (RHACM) can define desired states for managed clusters within a fleet. Multiple policies are often required to accomplish one desired end result, such as putting the console banner.

## Policies Setup
This directory and sub-directories contain the environment specific overlays for the clusters.

### Conventions
* **Do** Use **lower case** characters for policies and policySets.
* **Do** Separate policies based on category.
* **Do** Create new categories if one does not fit.
* **Do** Use placements via [PlacementPath](https://github.com/stolostron/policy-generator-plugin/blob/main/docs/policygenerator-reference.yaml#L146).

## Links of interest
[Policy Generator Reference](https://github.com/stolostron/policy-generator-plugin/blob/main/docs/policygenerator-reference.yaml)

# Overview of included Policies

The following policies are provided in directory `base`.
The `overlay` directory covery information to which clusters the policies are applied.

| **Directory** | **Hub Cluster** | **Workload Cluster** | **Description** |
|---|---|---|---|
| audit | | X | Audits deployment health and External Secrets Operator status. |
| console-banner | X | X | Displays a banner on the OpenShift Web Console. |
| hcp-idp | X | | Configures htpasswd/LDAP identity providers for Hosted Clusters. |
| ocp/self-provisioner | X | | Grants self-provisioning rights to users. |

