# platform-sre-lab

## Estrutura do repositório
```Bash
platform-sre-lab/
├── README.md
├── .github/
│   └── workflows/
│       └── deploy.yaml                  # GitHub Actions com OIDC
├── infra/
│   ├── terraform/
│   │   ├── gke/
│   │   │   ├── main.tf
│   │   │   ├── variables.tf
│   │   │   └── outputs.tf
│   │   ├── iam/
│   │   │   └── workload_identity.tf
│   │   └── network/
│   │       └── vpc.tf
│   └── argo-cd/
│       └── bootstrap.yaml               # Instalação inicial via manifests
├── apps/
│   ├── demo-app/
│   │   ├── kustomization.yaml
│   │   └── deployment.yaml
│   └── istio/
│       └── gateway.yaml
├── monitoring/
│   ├── prometheus/
│   │   └── prometheus-values.yaml       # Helm values
│   ├── grafana/
│   │   ├── dashboards/
│   │   └── grafana-values.yaml
│   └── loki/
│       └── loki-values.yaml
├── security/
│   ├── vault/
│   │   └── vault-helm-values.yaml
│   ├── trivy/
│   │   └── scan-config.yaml
│   └── policies/
│       └── opa/
│           └── restrict-deployments.rego
└── docs/
    ├── architecture-c4.md
    ├── observability.md
    └── security-model.md

```
