# EKS Setup

## EKS Clusters Creation

eksctl create cluster --name hub-cluster --region us-west-1

eksctl create cluster --name spoke-cluster-1 --region us-west-1

eksctl create cluster --name spoke-cluster-2 --region us-west-1

## EKS Clusters Deletion

eksctl delete cluster --name hub-cluster --region us-west-1

eksctl delete cluster --name spoke-cluster-1 --region us-west-1

eksctl delete cluster --name spoke-cluster-2 --region us-west-1

# 1. List all available clusters (contexts):

    kubectl config get-contexts

# 2. Check the current cluster (context) you're connected to:

    kubectl config current-context

# 3. Switch to another cluster/context:

    kubectl config use-context <context-name>


# Switch to hub context and instll argocd

for installation of argocd please refer prerequesites.md

Next:

     kubectl get cm -n argocd

![image](https://github.com/user-attachments/assets/d7cb5ab4-952b-473e-a03a-68af0e4253c3)

Edit:

    kubectl edit configmap argocd-cmd-params-cm

and paste this inside

# Run server without TLS
      data:
       server.insecure: "true"

 ![image](https://github.com/user-attachments/assets/82ca7550-a52f-44fd-9cf3-76607ab20bb8)

# Change the arocd-server type to NodePort mode

     kubectl edit svc argocd-server -n argocd



