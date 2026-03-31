# 🛠️ ChangeGate AI  

## 🚦 Intelligent Change Approval System  

**Python • YAML • Policy Engine • CLI**   

![FastAPI](https://img.shields.io/badge/FastAPI-005571?style=for-the-badge&logo=fastapi)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker)
![Kubernetes](https://img.shields.io/badge/Kubernetes-326CE5?style=for-the-badge&logo=kubernetes)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins)

A deterministic, rule-based approval system designed to protect production environments and automate deployment decisions with confidence 

------------------------------------------------------------------------------------------------------------------------------------------------------

## 📸 Screenshots / Demo  

### 🚦 API Interface (Swagger UI)
![API](https://github.com/user-attachments/assets/e313ce43-a3f1-49a8-84d4-8059ac7dbc6a)

---


### ❌ Blocked Scenario (High Risk Change)
![Blocked](https://github.com/user-attachments/assets/5caed881-08fc-498f-a63f-be4bb86f7742)

---

### ✅ Auto-Approved Scenario
![Approved](https://github.com/user-attachments/assets/2f8bd595-bde0-4aab-b394-f5127655ae10)


--------------------------------------------------------------------------------------------------------------------------------------------------------

## 🌟 Why ChangeGate AI?  

Modern deployments move fast—but unsafe changes move faster.  

ChangeGate AI acts as your automated gatekeeper, ensuring every change is evaluated against strict, transparent policies before it reaches production.  

--------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🚨 The Problem  

In modern DevOps:

- Engineers deploy directly to production  
- Small mistakes can cause major outages  
- No consistent approval system exists  
- Risky changes slip through unnoticed  

---

## ✅ The Solution  

ChangeGate AI acts as a **gatekeeper for your infrastructure**  

👉 Every change is evaluated before execution  
👉 Risky operations require human approval  
👉 Dangerous actions are blocked automatically  

**Result:** Safer, smarter, production-ready deployments

------------------------------------------------------------------------------------------------------------------------------------------------------------------


## 🌟 Features  


🚦 **Smart Change Approval System**  
Automatically decides whether a change should be:
- ✅ Auto-approved (safe changes)  
- ⚠️ Sent for manual approval (risky production changes)  
- ❌ Blocked (dangerous operations)

  

⚖️ **Production-Aware Decision Engine**  
Understands the **environment context**:
- Dev / Staging → fast & flexible  
- Production → strict & controlled  

👉 Ensures **critical systems are never changed without oversight**



📄 **Simple YAML-Based Input**  
Define changes in a clean, readable format  
No complex configs — just clear intent



🧠 **Deterministic Decisions (No Guesswork)**  
Same input → same output, every time  
No AI randomness, no surprises  

👉 Perfect for **auditable systems & compliance**



🔒 **Built-in Safety Guardrails**  
Prevents risky production actions like:
- Deleting critical resources  
- Over-scaling infrastructure  
- Unsafe deployments  



⚠️ **Automatic Manual Approval Trigger**  
High-risk production changes are **not executed blindly**  

👉 They are **flagged for human approval**, ensuring:
- Zero accidental outages  
- Safer deployments  
- Better control over infrastructure  



📊 **Transparent Decision Logs**  
Every decision is explained clearly:
- What was checked  
- Why it passed/failed  
- What rule triggered it  

👉 Makes debugging & audits effortless  



🧩 **Extensible Policy Engine**  
Easily add your own rules:
- Organization-specific policies  
- Security constraints  
- Deployment limits  

👉 Adaptable to any company workflow  

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🏗️ System Architecture  

![API](https://github.com/user-attachments/assets/06a96cbe-3d4d-4945-b8d9-4c9c2d503960)


----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🚀 Quick Start  

### 🔧 Prerequisites  

- Python 3.9+

- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ⚙️ Installation  

# Clone the repository
git clone https://github.com/KanupriyaPrachande/ChangeGate-AI

cd change-approval-system

# Create virtual environment
python -m venv venv
venv\Scripts\activate   # Mac/Linux: source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

### ▶️ Run the Engine  

python change_gate.py sample.yaml

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ⚙️ Decision Exit Codes  

| Code | Status | Meaning |
|------|--------|--------|
| 0 | ✅ Approved | Safe to deploy automatically |
| 1 | ⚠️ Review | Requires human approval |
| 2 | ❌ Blocked | Unsafe change |

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📜 Built-in Policy Rules  

🛑 Production Delete Protection  
→ Any delete operation in production is BLOCKED  

⚠️ High Scale Safeguard  
→ Scaling beyond 5 replicas in production requires APPROVAL  

✅ Staging Freedom  
→ All staging changes are AUTO-APPROVED  

🟢 Safe Defaults  
→ All non-risky operations pass automatically  

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🧠 Design Philosophy  

“Make the safe path the default path.”  

- Clarity over cleverness  
- Separation of concerns  
- Deterministic outcomes only  
- Enums over magic strings  
- Observability by design

- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📁 Project Structure

```text
change-approval-system/
├── change_gate.py
├── rules.py
├── models.py
├── parser.py
├── tests/
├── sample.yaml
└── requirements.txt
```

-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## ⚙️ Engineering Highlights  

🧩 Modular Rule System  
🔢 Enum-Driven Decisions  
🛡️ Robust Error Handling  
📦 Deterministic Outputs  
🧪 Fully testable (pytest)  

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📌 Assumptions  

- Scaling validation applies only to scale actions  
- Replica threshold is fixed at 5  
- YAML schema is intentionally minimal

- ---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🔮 Roadmap / Future Enhancements  

🚀 Policy engine abstraction layer  
⚙️ Configurable thresholds  
📄 JSON Schema validation  
📜 Audit logging  
🌐 FastAPI wrapper  
🔁 GitHub Actions integration  

------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🤝 Contributing  

Want to improve ChangeGate AI? Contributions are welcome!  

- Fork the repo  
- Create a feature branch  
- Submit a PR 🚀

- -------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 📄 License  

MIT License  

---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## 🙏 Acknowledgments  

💙 Python Community

📦 PyYAML Contributors

🧪 pytest Framework  

