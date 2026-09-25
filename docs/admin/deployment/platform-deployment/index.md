---
id: platform-deployment-overview
title: Platform Deployment
sidebar_label: Platform Deployment
sidebar_position: 1
---

# Platform Deployment

This section covers deploying AI/Run CodeMie application components onto a Kubernetes cluster. All guides support AWS, GCP, and Azure in a unified format using cloud tabs.

:::info Prerequisites
Before proceeding, ensure you have completed [Infrastructure Deployment](../infrastructure-deployment/index.md) and have a running Kubernetes cluster with the `deployment_outputs.env` file from the infrastructure phase.
:::

## Deployment Methods

| Method                                           | Description                                                                   | Recommendation                                           |
| ------------------------------------------------ | ----------------------------------------------------------------------------- | -------------------------------------------------------- |
| [**Automated Deployment**](./automated/index.md) | Single script (`helm-charts.sh`) installs all components in the correct order | Recommended for most users                               |
| [**Manual Deployment**](./manual/index.md)       | Install each component individually with full control over configuration      | Advanced use cases, troubleshooting, custom integrations |

## What Gets Deployed

Both methods install the same set of components:

| Component Group         | Components                                           |
| ----------------------- | ---------------------------------------------------- |
| **Infrastructure**      | Nginx Ingress Controller, Storage Class              |
| **Data Layer**          | Elasticsearch                                        |
| **Security & Identity** | Keycloak Operator, Keycloak, OAuth2 Proxy            |
| **Plugin Engine**       | NATS, NATS Auth Callout                              |
| **Core Services**       | CodeMie API, CodeMie UI, MCP Connect, Mermaid Server |
| **Observability**       | Fluent Bit, Kibana, Kibana Dashboards                |
