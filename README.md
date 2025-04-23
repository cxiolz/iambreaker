# IAMBreaker 🛡️

**Offensive IAM Analyzer for AWS**  
_Uncover privilege escalation paths, misconfigurations and exploitable trust relationships across IAM components._

![License](https://img.shields.io/github/license/seunome/IAMBreaker)  
![Python](https://img.shields.io/badge/python-3.11+-blue)  
![Status](https://img.shields.io/badge/status-in%20development-orange)

---

## 🧠 Overview

**IAMBreaker** is a red team and pentest-oriented tool for **identifying and simulating real-world privilege escalation paths** in **Amazon Web Services (AWS)** environments. It goes beyond static analysis by **executing validation tests**, simulating IAM-based attacks, and producing **actionable reports** for both technical and executive audiences.

---

## 💡 Why IAMBreaker?

- Traditional IAM analyzers stop at listing policies.  
- IAMBreaker **tests**, **simulates**, and **executes** possible attack vectors using given credentials.  
- Helps assess **"what can I really do?"** with limited access.

---

## ⚙️ Features

### ✅ Permission Simulation & Validation
- Actively tests if actions are **allowed and exploitable**.
- Uses `SimulatePrincipalPolicy` and direct execution attempts.

### 🔍 Deep Recon & Enumeration
- Enumerates all accessible:
  - Roles, users, groups
  - Policies (inline/attached)
  - Trust relationships
  - Session context (STS)

### 🚀 Privilege Escalation Simulations
- Attempts known AWS escalation paths, including:
  - Create new users with Admin policies
  - Attach policies to privileged roles
  - Abusing Lambda, CloudFormation and EC2 permissions
  - Exploiting `PassRole` and `AssumeRole`

### 🕸️ IAM Attack Graphs
- Automatically builds graphs of **attack paths** using IAM data.
- Exportable in Graphviz/DOT format.

### 📄 Reporting
- Markdown & PDF reports with:
  - Tested actions
  - Success/failure flags
  - Exploitable paths
  - Remediation tips

---

## 📦 Installation

```bash
git clone https://github.com/cxiolz/iambreaker.git
cd iambreaker
pip install -r requirements.txt
