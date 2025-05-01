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

     
