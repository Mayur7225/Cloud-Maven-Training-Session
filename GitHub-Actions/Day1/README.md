# 🚀 CI/CD Fundamentals - GitHub Actions

## 📌 Project Overview

This project demonstrates basic CI/CD pipeline using GitHub Actions.
Whenever code is pushed to the repository, a workflow automatically runs to test the application.

---

## 📁 Project Structure

```
github-actions-ci-cd/
│
├── .github/workflows/ci.yml   # GitHub Actions workflow
├── app/app.py                # Sample Python app
├── requirements.txt          # Dependencies
├── README.md                 # Documentation
```

---

## ⚙️ What is CI/CD?

CI/CD is a process where code changes are automatically:

* Built
* Tested
* Deployed

👉 Pipeline flow:

```
Code → Build → Test → Deploy → Monitor
```

---

## 🔄 GitHub Actions Workflow

GitHub Actions works on:

* **Trigger** → When event happens (push / pull request)
* **Workflow** → Collection of jobs
* **Job** → Runs on runner (machine)
* **Steps** → Commands executed

---

## 📌 Workflow File (ci.yml)

```yaml
name: CI Pipeline

on:
  push:
    branches: [ "main" ]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
    - name: Checkout Code
      uses: actions/checkout@v3

    - name: Setup Python
      uses: actions/setup-python@v4
      with:
        python-version: '3.9'

    - name: Install Dependencies
      run: |
        pip install -r requirements.txt

    - name: Run Application
      run: |
        python app/app.py
```

---

## 📌 Sample Application

```python
print("Hello from GitHub Actions CI Pipeline 🚀")
```

---

## 📊 Tasks Answer

### ✅ Task 1: Problems Without CI/CD

* Manual deployment
* Human errors
* No rollback
* Slow releases
* No tracking/logs

---

### ✅ Task 2: GitHub Actions Observation

* **Trigger** → push event
* **Job** → build
* **Goal** → Run application automatically

---

### ✅ Task 3: Correct CI/CD Flow

```
1. Write Code
2. Build
3. Run Tests
4. Deploy Application
5. Monitor Application
```

---

## 🎯 Conclusion

GitHub Actions automates:

* Testing
* Building
* Deployment

👉 This reduces manual work and improves software quality.

---

## 📚 References

* https://docs.github.com/en/actions
* https://martinfowler.com/articles/continuousIntegration.html

