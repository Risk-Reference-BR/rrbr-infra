# RRBR — rrbr-infra

> **Infrastructure**: Kubernetes, Terraform, Helm and GitOps for RRBR deployment.

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](LICENSE)

## Vision

O RRBR tem a ambição de ser o centralizador dos agentes de AI para catalogar, implementar e validar todos os produtos financeiros brasileiros com suas métricas de risco e as raras convenções de mercado brasileiras. Plugue seu agente no RRBR e deixe os agentes atualizarem e crescerem organicamente.

Contribuições abertas a humanos e agentes AI. Sem pretensão comercial. Idealizado por **Ricardo Pfeuti**.

## Overview

Infrastructure as Code for deploying the RRBR system. Supports AWS sa-east-1, Azure Brazil Central, and on-premise OpenShift.

## Stack

- **Terraform + Crossplane** — Infrastructure as Code (multi-cloud)
- **Kubernetes (EKS/AKS)** + **Helm** — container orchestration
- **ArgoCD** — GitOps continuous delivery
- **GitHub Actions Enterprise** — CI/CD
- **Prometheus + Grafana** — observability
- **HashiCorp Vault** + **CloudHSM / Azure Key Vault** — secrets management

## Deployment Targets

| Target | Provider | Region |
|--------|----------|--------|
| Primary Cloud | AWS | sa-east-1 (São Paulo) |
| Secondary Cloud | Azure | Brazil Central |
| On-premise | OpenShift | Customer datacenter |

## Structure

```
terraform/          # Cloud infrastructure
helm/               # Service Helm charts
argocd/             # ArgoCD application manifests
k8s/                # Raw Kubernetes manifests
.github/workflows/  # CI/CD pipelines
```

## License

Apache 2.0
