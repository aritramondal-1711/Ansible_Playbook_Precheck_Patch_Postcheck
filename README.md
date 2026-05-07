# 🚀 Ansible-Based Automated OS Patching Framework

## 📌 Overview

This project is an agentless automation framework built using Ansible to streamline and standardize OS patching across Linux/Solaris environments. It follows a structured three-phase approach: **Pre-Check → Patching → Post-Check** to ensure reliability, consistency, and minimal downtime.

---

## ⚙️ Features

* 🔹 Fully automated OS patching workflow
* 🔹 Modular design using Ansible roles
* 🔹 Agentless architecture (SSH-based execution)
* 🔹 Pre and post validation with report generation
* 🔹 Scalable for large server environments

---

## 🧩 Project Structure

```
Patching/
├── hosts
├── patch.yml
├── PRECHECK/
├── PATCH/
├── POSTCHECK/
├── prechecks/
└── postchecks/
```

### 🔹 Roles

* **PRECHECK**: Collects system information, validates prerequisites, and stores baseline data
* **PATCH**: Performs OS patching using package management
* **POSTCHECK**: Validates system state after patching and compares results

---

## 🔄 Workflow

### 1️⃣ Pre-Check Phase

* System health validation
* Disk, CPU, memory checks
* Service status collection
* Baseline data storage

### 2️⃣ Patching Phase

* Applies latest available updates
* Uses package manager (yum/apt/pkg depending on OS)
* Ensures controlled execution

### 3️⃣ Post-Check Phase

* Re-validates system health
* Compares with pre-check results
* Generates reports for verification

---

## ▶️ How to Run

1. Update inventory file:

```
hosts
```

2. Execute playbook:

```
ansible-playbook -i hosts patch.yml
```

---

## 📊 Output

* Pre-check reports stored in `prechecks/`
* Post-check reports stored in `postchecks/`
* Logs available for auditing and troubleshooting

---

## 💡 Use Cases

* Enterprise patch management
* Compliance and security updates
* Automated maintenance windows
* Large-scale infrastructure operations

---

## 🛠️ Tech Stack

* Ansible
* Linux / Solaris
* Shell scripting

---

## 📈 Future Enhancements

* Reboot validation and automation
* Email/Slack notifications
* Integration with monitoring tools
* Patch rollback mechanism

---

## 👨‍💻 Author

Aritra (Linux Administrator | Automation Enthusiast)

---

## ⭐ Contribution

Feel free to fork, enhance, and raise pull requests!
