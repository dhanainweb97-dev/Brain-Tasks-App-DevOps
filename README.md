cat > README.md <<'EOF'
# Brain Tasks App – AWS DevOps Deployment

## Overview

This project demonstrates the deployment of a React-based Brain Tasks application using a production-oriented AWS DevOps workflow.

The application is packaged into a Docker container, stored in Amazon ECR, and deployed to an Amazon EKS Kubernetes cluster through AWS CodeBuild and a GitHub webhook.

## Architecture

```text
Developer Push
      |
      v
GitHub Repository
      |
      v
GitHub Webhook
      |
      v
AWS CodeBuild
      |
      +---- Docker Build
      |
      v
Amazon ECR
      |
      v
Amazon EKS
      |
      +---- Pod 1
      |
      +---- Pod 2
      |
      v
Kubernetes LoadBalancer
      |
      v
Brain Tasks Application
