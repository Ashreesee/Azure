# Azure Application Gateway Ingress Controller (AGIC) - HTTP & HTTPS Access Demo

## Overview
This document outlines the step-by-step process to deploy a demo application on Azure Kubernetes Service (AKS) with both HTTP and HTTPS ingress using the Azure Application Gateway Ingress Controller (AGIC). It also includes TLS termination, hostname-based routing, HTTP-to-HTTPS redirection, multi-service ingress configuration, and troubleshooting tips.

---

## 🚀 Prerequisites

- Azure CLI
- kubectl
- Helm v3+
- Access to Azure Subscription
- OpenSSL (for generating self-signed certs)

---

## ⚙️ Environment Setup

### Set Variables

```bash
RESOURCE_GROUP="agic-demo-rg"
LOCATION="eastus"
CLUSTER_NAME="agic-demo-cluster"
APP_GATEWAY_NAME="agic-demo-appgw"
SUBSCRIPTION_ID=$(az account show --query id -o tsv)
