ChangeGate AI - Intelligent Change Approval System

Python YAML Policy Engine CLI

Rule-based change approval system with deterministic decision engine

🎥 Project Demo.mp4
📄 Documentation

🔗 Deployment Link
Click Me

🌟 Features

⚖️ Policy-Driven Decisions – Deterministic rule evaluation for consistent approvals
📄 YAML-Based Input – Simple, human-readable change definitions
🚦 Automated Approval Flow – Instant approve / reject / review decisions
🧠 Explicit Decision Engine – Enum-based outcomes (no ambiguity)
📊 Production-Style Logging – Structured logs for traceability
🔒 Safe Deployment Rules – Prevent risky production changes
🧩 Extensible Rules Engine – Easily add new policies

🏗️ Architecture
┌──────────────┐
│   YAML Input │
└──────┬───────┘
       ▼
┌──────────────┐
│ Parse &      │
│ Validate     │
└──────┬───────┘
       ▼
┌──────────────┐
│ Generate Plan│
└──────┬───────┘
       ▼
┌──────────────┐
│ Policy Rules │
│   Engine     │
└──────┬───────┘
       ▼
┌──────────────┐
│ Decision     │
│ Engine       │
└──────┬───────┘
       ▼
┌──────────────┐
│ Final Result │
│ + Exit Code  │
└──────────────┘
🚀 Quick Start
Prerequisites
Python 3.9+
Installation
# Clone repository
git clone <your-repo-link>
cd change-approval-system

# Create virtual environment
python -m venv venv
venv\Scripts\activate   # Mac/Linux: source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
▶️ Run the System
python change_gate.py sample.yaml
⚙️ Exit Codes
Code	Meaning
0	✅ AUTO-APPROVED
1	⚠️ APPROVAL REQUIRED
2	❌ BLOCKED
📜 Policy Rules Implemented

🚫 Delete operation in production → BLOCKED
⚠️ Scaling > 5 replicas in production → APPROVAL REQUIRED
✅ Apply in staging → AUTO-APPROVED
🟢 Safe operations → AUTO-APPROVED

🧠 Design Philosophy
Clarity over cleverness
Strict separation of concerns
Deterministic rule evaluation
Explicit decision modeling using Enums
Production-grade logging
🗂️ Project Structure
change-approval-system/
├── change_gate.py     # Main execution engine
├── rules.py           # Policy rules
├── models.py          # Enums & data models
├── parser.py          # YAML parsing & validation
├── tests/             # Unit tests (pytest)
├── sample.yaml        # Example input
└── requirements.txt
⚙️ Engineering Decisions
🧩 Rules isolated in rules.py for scalability
🔢 Enum-based decisions to eliminate magic strings
🛡️ Structured error handling
📦 Deterministic outputs for reliability
🧪 Fully testable rule logic using pytest
📌 Assumptions
Replica validation applies only to scale actions
Threshold fixed at 5 replicas
YAML schema kept minimal for simplicity
🔮 Future Improvements

🚀 Policy engine abstraction layer
⚙️ Configurable rule thresholds
📄 JSON schema validation
📜 Audit logging system
🌐 REST API wrapper (FastAPI)
🔁 GitHub Actions integration

🤝 Contributing

Contributions are welcome!
Feel free to open issues or submit pull requests 🚀

📄 License

MIT License

🙏 Acknowledgments

Python Community
PyYAML Contributors
pytest Framework
