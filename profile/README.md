# 🐝 SwarmMarket — A Decentralized AI Training Marketplace on Gensyn

> The future of machine learning is decentralized — we're building the interface to make it usable.

SwarmMarket is a marketplace-style frontend built on top of Gensyn’s RL Swarm protocol. It allows users to submit reinforcement learning or LLM fine-tuning jobs, dispatch them across a decentralized network of training nodes, and track training, billing, and protocol-level verification in real-time. This project brings Gensyn’s testnet vision to life with a clean, intuitive user experience.

---

## 🔭 Project Vision

While Gensyn provides the protocol and infrastructure for decentralized ML training, SwarmMarket provides the **first user-facing layer** that makes this power accessible.

With SwarmMarket, users can:
- Submit training jobs with configuration and budget
- Watch jobs get picked up by swarm nodes
- Track model performance and real-time costs
- Simulate smart contract-based job verification
- Download trained models and view full invoices

---

## 💡 Why This Matters

Centralized AI infrastructure is costly, opaque, and restricted to big players. Gensyn’s decentralized compute protocol aims to change that.

SwarmMarket shows **how real users can interact** with this infrastructure:
> “Once the protocol exists, how do I actually use it to train my models?”

---

## 🧑‍💻 End-User Flow

1. **Submit a Training Job**
   - Choose a model (e.g., CartPole PPO, LunarLander, Mini-LLaMA)
   - Enter dataset (IPFS/GCS/S3 URL)
   - Set training config (epochs, batch size, learning rate)
   - Define budget (in GNS tokens)

2. **Cost Estimation**
   - System simulates time & cost based on config
   - User pre-authorizes budget via simulated wallet

3. **Swarm Training Begins**
   - Nodes pick up job
   - Training happens across nodes in a simulated swarm
   - Live metrics and logs are shown to the user

4. **Job Completion + Output**
   - Model file is downloadable
   - Invoice shows full cost breakdown
   - Smart contract logs simulate decentralized verification

---

## 🛠️ Tech Stack

### 🖥 Frontend
- **Next.js** + **Tailwind CSS** (UI Framework)
- **Recharts** (Training metric visualizations)
- **Axios** (API calls)
- **Optional**: Monaco editor (IDE mode for advanced users)

### 🧠 Backend
- **FastAPI** (Job submission + status API)
- **Stable-Baselines3** + **Gym** (RL training engine)
- **SQLite / in-memory storage** (Job & wallet data)
- **Multi-process Python simulation** for swarm behavior

### 🪙 Smart Contract / Billing Simulation
- JSON-based log events for protocol interactions
- Simulated token system (GNS) with wallet pre-auth + refunds
- Optional: Hardhat + Web3.py for real smart contract layer

---

## 💰 Token & Billing Logic

- Pricing simulated per task: `epochs × GNS/unit`
- Budget “locked” on job start (mock wallet)
- Live cost meter updates in real-time
- Refund issued for unused compute
- Invoices generated at job completion

---

## 📊 Key Features

| Feature                     | Description                                       |
|-----------------------------|---------------------------------------------------|
| 🧠 Job Submission UI        | Simple config interface for training jobs         |
| 🐝 Swarm Node Simulation    | Simulates job pickup, swarm sync, and rewards     |
| 📈 Training Progress        | Live chart: reward vs episode                     |
| 🧾 Token Meter & Invoices   | Budget lock, dynamic cost display, full receipt   |
| 🌐 Smart Contract Logs      | Simulated on-chain events (job accepted, verified)|
| 🧪 Verification UI          | Logs verifier actions + challenge outcomes        |
| 💼 IDE Mode (Optional)      | Advanced users can upload configs / code          |

---

## 🚀 Getting Started

```bash
# Backend Setup
cd backend
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows
pip install -r requirements.txt
uvicorn main:app --reload

# Frontend Setup
cd frontend
npm install
npm run dev
