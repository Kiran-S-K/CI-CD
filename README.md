# CI/CD Pipelines using GitHub Actions

##  Overview
This project is created to understand and implement **CI/CD (Continuous Integration and Continuous Deployment)** using **GitHub Actions**.

The goal is to automate tasks such as **testing, building, and deploying applications** whenever certain events occur in a GitHub repository (like pushing code or creating a pull request).  

This repository focuses on **CI concepts first**, with a strong foundation before moving to advanced tools like Kubernetes.  

---

## What is CI/CD?

### 🔹 Continuous Integration (CI)
CI is the practice of **automatically checking and testing code** whenever developers push changes to a repository.  

**Example:**
- A developer pushes code  
- Tests run automatically  
- Build fails if something is broken  

### 🔹 Continuous Deployment (CD)
CD automatically **deploys the application** after the CI process passes successfully.

**Example:**
- Tests are run  
- Application is built  
- Application is deployed automatically  

---  

## What is GitHub Actions?

**GitHub Actions** is GitHub’s built-in CI/CD tool that allows us to:  
- Automatically run tasks  
- Trigger pipelines on events  
- Define workflows using YAML files  

GitHub Actions eliminates the need for external CI/CD tools for many use cases.  

---  

## What are Workflows?

A **workflow** is an **automated process** that runs one or more jobs when a specific event happens in the repository.  
 Workflows are defined using **YAML files** and stored inside:  
 ### In simple terms:
> **Event → Workflow → Jobs → Steps**

---

## ⚡ GitHub Events  

Workflows are triggered by **events**.

Common GitHub events:  
- `push` – when code is pushed  
- `pull_request` – when a PR is opened  
- `workflow_dispatch` – manual trigger  
- `release` – when a release is created  

**Example:**
```yaml  
on:  
  push:  
    branches: [ main ]

When an event is performed, series of actions takes place, these chain of actions are called workflows.  
