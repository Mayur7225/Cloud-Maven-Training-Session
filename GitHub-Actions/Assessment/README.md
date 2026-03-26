# 🚀 GitHub Actions CI/CD Assessment (Cloud-Maven)

## 📌 Overview

Is project me maine GitHub Actions ka use karke complete CI/CD pipeline implement kiya hai.
Isme Docker build & push, reusable workflows, security scanning (Trivy), aur Slack notifications integrate kiye gaye hai.

---

# 🧩 Task 1 – Hello Workflow

## ✅ Purpose

Basic GitHub Actions workflow test karna.

## ⚙️ Implementation

* File: `.github/workflows/hello.yml`
* Trigger: push on any branch
* Action: "Hello GitHub Actions!" print

## 🔍 Verification

* GitHub Actions tab me workflow successfully run hua
* Logs me message visible

---

# 🐳 Task 2 – Docker Build & Push

## ✅ Purpose

Application ko containerize karke DockerHub pe push karna.

## ⚙️ Implementation

* Multi-stage Dockerfile use kiya
* `.dockerignore` add kiya
* Workflow: `.github/workflows/docker.yml`

## 🔐 Secrets Used

* `DOCKER_USERNAME`
* `DOCKER_PASSWORD` (Docker access token)

## 🏷️ Image Tagging

* `latest`
* `commit SHA`

## 🔍 Verification

* DockerHub pe images successfully push hui
* Actions logs me build & push success

---

# 🔁 Task 3 – Reusable Workflow

## ✅ Purpose

Reusable CI workflow create karke code duplication avoid karna.

## ⚙️ Implementation

* File: `.github/workflows/docker-ci.yml`
* `workflow_call` use kiya
* Caller workflow: `caller.yml`

## 🔄 Behavior

* `develop` branch → `staging-<commit_sha>`
* `main` branch → `prod-<commit_sha>`

## 🔍 Verification

* Caller workflow successfully reusable workflow call karta hai
* Different tags generate hote hai

---

# 🔐 Task 4 – Security & Notifications

## 🛡️ Trivy Security Scan

* Tool: Trivy
* Severity: HIGH, CRITICAL
* Pipeline fail hota hai agar vulnerability mile

## 🔔 Slack Notification

* Slack webhook integrate kiya
* Success aur failure dono pe notification

## 🔐 Secrets Used

* `SLACK_WEBHOOK`

## 🔍 Verification

* Scan logs Actions me visible
* Slack pe notification receive hua

---

# 🧪 Key Learnings

* GitHub Actions workflows automation
* Docker image build & push process
* Reusable workflows ka concept
* Secrets management in CI/CD
* Security scanning using Trivy
* Real-time notifications using Slack

---

# ✅ Conclusion

Is assessment me maine ek complete CI/CD pipeline implement kiya jisme automation, security aur monitoring sab cover kiya gaya hai.

---

