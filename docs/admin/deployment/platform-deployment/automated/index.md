---
id: platform-automated-overview
title: Automated Platform Deployment
sidebar_label: Automated Deployment
sidebar_position: 1
---

# Automated Platform Deployment

Automated deployment uses the `helm-charts.sh` script to install all AI/Run CodeMie components in the correct dependency order with a single command.

:::tip Recommended Approach
Scripted deployment is recommended for standard installations as it automates component ordering, validates prerequisites, and ensures consistent configuration across all components.
:::

## Deployment Tracks

| Track                              | Description                                                                         |
| ---------------------------------- | ----------------------------------------------------------------------------------- |
| [**Kubernetes**](./kubernetes.mdx) | Deploy all components onto an EKS / GKE / AKS cluster using Helm charts             |
| [**On VM**](./on-vm.mdx)           | Deploy the CodeMie stack onto a provisioned VM using the `./deploy.sh --byo` script |

## Script Modes

| Mode          | Components Installed                                         | Use Case                                 |
| ------------- | ------------------------------------------------------------ | ---------------------------------------- |
| `all`         | All components including Nginx Ingress Controller            | Fresh cluster without existing ingress   |
| `recommended` | All components except Nginx Ingress Controller               | Cluster with existing ingress controller |
| `update`      | Only CodeMie core components (API, UI, MCP Connect, Mermaid) | Updating existing installation           |
