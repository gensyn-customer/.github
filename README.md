# 🐝 SwarmMarket — A Decentralized AI Training Marketplace on Gensyn

> The future of machine learning is decentralized — we're building the interface to make it usable.

SwarmMarket is a marketplace-style frontend built on top of Gensyn’s RL Swarm protocol. It allows users to submit reinforcement learning or LLM fine-tuning jobs and dispatch them across a decentralized network of training nodes. Our system simulates real-time training, cost estimation, on-chain job logs, and swarm learning — making Gensyn’s infrastructure understandable, usable, and demoable.

---

## 🔭 Project Vision

Gensyn is creating the trustless infrastructure for decentralized ML training. We're creating the **first user-facing layer** that sits on top of that — a simple and powerful interface where users can:

- Upload training jobs
- Estimate costs
- Watch decentralized training progress
- View smart contract interactions
- Receive verifiable models and final invoices

---

## 💡 Why This Matters

Modern AI requires massive compute, often gated behind expensive cloud providers. Gensyn envisions a world where training happens across a global network of machines — verifiable, distributed, and open.

**SwarmMarket** answers the question:  
> “Once that protocol exists, how do users actually interact with it?”

---

## 🧑‍💻 End-User Flow

1. **Submit a Training Job**
   - Upload a script or choose a preset (e.g., CartPole, LLaMA fine-tune)
   - Define dataset, model type, budget, and deadline

2. **Receive Cost Estimate**
   - Our engine simulates training time and cost
   - User pre-authorizes payment via mock wallet

3. **Swarm Training Begins**
   - Nodes pick up jobs
   - Users track real-time logs, progress, and swarm coordination
   - Simulated on-chain logs display node activity

4. **Receive Results + Invoice**
   - Trained model returned (or simulated)
   - On-chain logs finalized
   - Remaining balance refunded

---

## 🛠️ Tech Stack

### Backend
- Python + Flask (API)
- Stable-Baselines3 (RL Training — e.g., PPO on CartPole)
- Simulated swarm weight-sharing logic
- SQLite / in-memory store for logs and job history

### Frontend
- Next.js + Tailwind CSS
- Recharts / Chart.js for visualizations
- Job submission + node explorer UI
- Live metrics and token meter simulation

### Simulated On-Chain Layer
- JSON-based mock smart contract logs
- (Optional) Hardhat + web3.py for real contract simulation

---

## 💰 Billing System

- Estimated cost based on job config (epochs, batch size, env)
- Simulated GPU/hour pricing
- User pre-authorizes funds (fake GNS tokens)
- Final billing computed from actual training duration
- Remaining funds refunded

---

## 📊 Key Features

| Feature                       | Description                                      |
|-------------------------------|--------------------------------------------------|
| 🧠 Job Submission UI          | Upload scripts, define model/task               |
| 🔁 Swarm Simulation           | Nodes collaborate to improve model performance  |
| 📈 Real-time Training Logs    | Watch metrics evolve over time                  |
| 🌐 Smart Contract Visualizer  | See when nodes pick up and complete jobs        |
| 💸 Token-based Billing        | Simulated GNS/USDC system with dynamic pricing  |
| 🧾 Invoice Generator          | Transparent breakdown of compute usage          |

---

## 🚀 Getting Started (Dev Setup)

```bash
# Backend
cd backend
pip install -r requirements.txt
python app.py

# Frontend
cd frontend
npm install
npm run dev
