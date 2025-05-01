# Multi Cluster Deployment using Argo CD

Argo CD (short for Argo Continuous Delivery) is a declarative, GitOps-based continuous delivery tool for Kubernetes. It helps you automate the deployment and management of applications in a Kubernetes cluster by syncing the desired state defined in Git repositories with the actual state in the cluster.

# Key Concepts:

GitOps: Argo CD uses Git as the single source of truth. You store your Kubernetes manifests or Helm charts in a Git repo, and Argo CD keeps your cluster in sync with it.

Declarative: You describe what the system should look like (e.g., via YAML files), and Argo CD makes it so.

Application Controller: Continuously monitors running applications and compares them to the Git repo.

Syncing: Argo CD can automatically or manually sync the live cluster state to match the Git repo.

# Features:

Visual dashboard and CLI to manage applications.

Real-time monitoring of app health and sync status.

Rollbacks to previous Git commits.

Support for Helm, Kustomize, Jsonnet, and plain YAML.

RBAC and SSO integration.

# Use Case Example:

You push a new version of your Helm chart to Git. Argo CD detects the change, and if set to auto-sync, it updates your app in the Kubernetes cluster automatically.

![image](https://github.com/user-attachments/assets/d5351011-bae7-412c-9562-d98e0f46960b)


![Untitled design(4)](https://github.com/iam-veeramalla/argocd-hub-spoke-demo/assets/43399466/3fc8e4f6-408c-4575-9b96-e737fc1d0526)



