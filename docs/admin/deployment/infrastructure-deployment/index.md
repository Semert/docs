---
id: infrastructure-deployment-overview
title: Infrastructure Deployment
sidebar_label: Infrastructure Deployment
sidebar_position: 1
---

# Infrastructure Deployment

This section covers deploying the cloud infrastructure required to run AI/Run CodeMie — managed Kubernetes clusters, virtual machines, networking, storage, and databases. All guides support AWS, GCP, and Azure in a unified format using cloud tabs.

:::info Existing Infrastructure
If you already have a provisioned cluster or VM with all required services, skip this section and proceed directly to [Platform Deployment](../platform-deployment/index.md).
:::

## Deployment Tracks

Choose the deployment track that matches your target environment:

| Track                              | Description                                                                                                                                     | When to Use                                                     |
| ---------------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------- |
| [**Kubernetes**](./kubernetes.mdx) | Provision a managed Kubernetes cluster (EKS / GKE / AKS) along with supporting cloud resources (networking, storage, databases) using Terraform | When running CodeMie on Kubernetes (recommended for production) |
| [**On VM**](./on-vm.mdx)           | Provision a single virtual machine (EC2 / GCE / Azure VM) and deploy the full CodeMie stack via Docker Compose                                  | When a lightweight, single-node deployment is preferred         |

## Deployment Methods

Both tracks support two deployment methods:

| Method       | Description                                                      | Recommendation                          |
| ------------ | ---------------------------------------------------------------- | --------------------------------------- |
| **Scripted** | Automated shell script handles all Terraform phases in sequence  | Recommended for most users              |
| **Manual**   | Step-by-step Terraform commands for full control over each phase | Advanced use cases, custom integrations |

## Next Steps

After completing infrastructure deployment, proceed to [Platform Deployment](../platform-deployment/index.md) to install AI/Run CodeMie application components.
