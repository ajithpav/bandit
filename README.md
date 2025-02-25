# 🔒 Security Checks GitHub Action

This GitHub Action automates security checks on Python dependencies and code using **Bandit, pip-audit, and Safety**.

## 📌 Workflow Triggers
Runs on push & pull requests to:
- `release/*`, `feature/*`, `july-updates`
- Changes to `requirements.txt`

## 🏗️ Job Execution
Runs on **Ubuntu** & **Windows**.

### ✅ Steps
1. **Checkout Code**  
2. **Set up Python (3.x)**  
3. **Install Dependencies**  
4. **Run Bandit** (Code security analysis)  
5. **Run pip-audit** (Dependency vulnerability check)  
6. **Run Safety** (Security scan on dependencies)  
7. **Upload Bandit Report** (`bandit-report.json`)

## 🚀 Run Locally
```sh
pip install pip-audit safety bandit
bandit -r .
pip-audit
safety check -r requirements.txt
