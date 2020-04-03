Steps for EKS:
---------------------

1. Create VPC and Networking Components Using amazon-eks-vpc-private-subnets.yaml Template

2. Create EKS Cluster Using AWS EKS Cluster with created VPC and SG

3. Create Nodegroup using amazon-eks-nodegroup.yaml Template file.

4. Install prerequisites siftware like, kubeclt, aws-iam-authenticator, aws cli tools

5. Establish the connection to  EKS Cluster from client machine using below cmd,
   aws eks update-kubeconfig --name CLUSTER-NAME --region REGION

6. To enable worker nodes to join your cluster, use aws-auth-cm.yaml and replace NodeInstanceRole 
  kubectl apply -f aws-auth-cm.yaml

