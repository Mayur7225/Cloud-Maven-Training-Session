# GitHub Actions CI/CD Lab

## Task 1 – Hello Workflow

Purpose: Basic GitHub Actions testing
Verification: Logs show "Hello GitHub Actions!"

## Task 2 – Docker Build & Push

Purpose: Build multi-stage Docker image
Secrets:

* DOCKER_USERNAME
* DOCKER_PASSWORD
  Verification:
* Image available on Docker Hub
* Tags: latest, commit SHA

## Task 3 – Reusable Workflow

Purpose: Centralized CI/CD
Details:

* workflow_call used
* Release tag v1.0.0
  Verification:
* develop → staging image
* main → prod image

## Task 4 – Security & Notifications

Purpose:

* Scan image vulnerabilities
* Notify via Slack
  Tools:
* Trivy
* Slack Webhook
  Verification:
* Pipeline fails on HIGH/CRITICAL
* Slack messages received

## Conclusion

Implemented full CI/CD pipeline with reusable workflows, security scanning, and notifications.

