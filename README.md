🛠️ ChangeGate AI
🚦 Intelligent Change Approval System

Python • YAML • Policy Engine • CLI

A deterministic, rule-based approval system designed to protect production environments and automate deployment decisions with confidence


🔗 Deployment Link
Click Me

🌟 Why ChangeGate AI?

Modern deployments move fast—but unsafe changes move faster.
ChangeGate AI acts as your automated gatekeeper, ensuring every change is evaluated against strict, transparent policies before it reaches production.

✨ Features

⚖️ Deterministic Policy Engine
No randomness, no surprises—every decision is predictable and explainable

📄 Human-Friendly YAML Input
Define infrastructure changes in a clean, readable format

🚦 Instant Decision System
Automatically classify changes into:

✅ Approved
⚠️ Needs Review
❌ Blocked

🧠 Explicit Decision Modeling
Enum-based outcomes ensure zero ambiguity in results

📊 Production-Grade Logging
Trace every decision with structured, debuggable logs

🔒 Built-in Safety Rules
Prevents dangerous production actions before they happen

🧩 Plug-and-Play Rule Engine
Easily extend with custom policies for your organization

🏗️ System Architecture
┌────────────────────┐
│   YAML Change Spec │
└─────────┬──────────┘
          ▼
┌────────────────────┐
│  Parse & Validate  │
└─────────┬──────────┘
          ▼
┌────────────────────┐
│   Execution Plan   │
└─────────┬──────────┘
          ▼
┌────────────────────┐
│   Policy Engine    │
│ (Rule Evaluation)  │
└─────────┬──────────┘
          ▼
┌────────────────────┐
│  Decision Engine   │
└─────────┬──────────┘
          ▼
┌────────────────────┐
│ Result + Exit Code │
└────────────────────┘
🚀 Quick Start
🔧 Prerequisites
Python 3.9+
⚙️ Installation

# Clone the repository
git clone <your-repo-link>
cd change-approval-system

# Create virtual environment
python -m venv venv
venv\Scripts\activate   # Mac/Linux: source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

▶️ Run the Engine
python change_gate.py sample.yaml

⚙️ Decision Exit Codes

| Code | Status     | Meaning                          |
| ---- | ---------- | -------------------------------- |
| `0`  | ✅ Approved | Safe to deploy automatically     |
| `1`  | ⚠️ Review  | Requires human approval          |
| `2`  | ❌ Blocked  | Unsafe change, deployment denied |

📜 Built-in Policy Rules

🛑 Production Delete Protection
→ Any delete operation in production is BLOCKED

⚠️ High Scale Safeguard
→ Scaling beyond 5 replicas in production requires APPROVAL

✅ Staging Freedom
→ All staging changes are AUTO-APPROVED

🟢 Safe Defaults
→ All non-risky operations pass automatically

🧠 Design Philosophy

“Make the safe path the default path.”

🔍 Clarity over cleverness
🧱 Separation of concerns
🎯 Deterministic outcomes only
🔢 Enums over magic strings
📊 Observability by design
🗂️ Project Structure

change-approval-system/
├── change_gate.py     # Core execution engine
├── rules.py           # Policy definitions
├── models.py          # Enums & data contracts
├── parser.py          # YAML parsing & validation
├── tests/             # Unit tests (pytest)
├── sample.yaml        # Example input
└── requirements.txt

⚙️ Engineering Highlights

🧩 Modular Rule System
Rules are fully isolated for easy extension

🔢 Enum-Driven Decisions
Eliminates ambiguity and string-based errors

🛡️ Robust Error Handling
Graceful failure with clear diagnostics

📦 Deterministic Outputs
Same input → same result, always

🧪 Test-First Approach
Designed for high testability with pytest

📌 Assumptions
Scaling validation applies only to scale actions
Replica threshold is fixed at 5
YAML schema is intentionally minimal for clarity
🔮 Roadmap / Future Enhancements

🚀 Policy engine abstraction layer
⚙️ Configurable thresholds via config files
📄 JSON Schema validation
📜 Full audit logging & history tracking
🌐 REST API wrapper (FastAPI)
🔁 CI/CD integration (GitHub Actions)

🤝 Contributing

Want to improve ChangeGate AI? Contributions are welcome!

Fork the repo
Create a feature branch
Submit a PR 🚀
📄 License

MIT License

🙏 Acknowledgments

💙 Python Community
📦 PyYAML Contributors
🧪 pytest Framework
