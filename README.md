# EKS Tetris Deployment 🎮

Deploy a Tetris game on AWS EKS Auto Mode with ALB ingress.

## Prerequisites
- AWS CLI configured
- kubectl installed
- AWS account with EKS permissions

## Architecture
VPC (3 public + 3 private subnets) → EKS Auto Mode + Karpenter → ALB → Tetris App

## Quick Start
1. Create VPC with public/private subnets
2. Create IAM role (eks-tetris-cluster-role)
3. Create EKS cluster (Auto Mode)
4. Connect local machine via kubeconfig
5. Tag subnets for ALB
6. Deploy Tetris app + ALB ingress
7. Access via ALB DNS URL

## Files
- tetris-app.yaml     — Deployment + Service
- ingressclass.yaml   — ALB IngressClass
- tetris-ingress.yaml — ALB Ingress rules

## Cleanup
Delete EKS cluster, NAT Gateways, and VPC to avoid AWS charges.
