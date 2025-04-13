# A Visual Dashboard for Gensyn’s RL Swarm Protocol

<p style="text-align: center; font-size: 4em;">
    <a href="https://drive.google.com/file/d/19fRpBSP6yJlh4DGQs71IQ7AwFbHT7ZaQ/view?usp=sharing" style="font-weight: bold; color: blue; text-decoration: none;">
        VIDEO
    </a>
</p>


![Alt text](../Gensyn%201.png))
![Alt text](../Gensyn%202.png)

SwarmMarket is a frontend-only visualization dashboard built on top of Gensyn’s **RL Swarm protocol**. It presents a real-time view of decentralized AI training jobs as they are distributed across simulated swarm nodes. 

---
## Links!

<a href="https://github.com/gensyn-customer/SwarmUI" style="font-weight: bold; color: blue; font-size: 1.2em;">Project Repo</a>

## 🔭 Project Vision

Gensyn is building the infrastructure for verifiable, decentralized ML compute.  
**SwarmMarket** provides a visual layer that answers:

> “What does it actually look like when decentralized model training is happening?”

This dashboard simulates the **training lifecycle**, from job creation to model output, across multiple swarm nodes — including visualizations of rewards, verification logs, and cost estimation.

---

## 💡 Why This Matters

Modern ML is fragmented, expensive, and closed off. Gensyn is changing that with its distributed training protocol. But protocols are invisible without interfaces.

SwarmMarket gives developers and researchers a way to:
- Understand how swarm learning improves model performance
- Track training in real time
- View on-chain-style interactions between nodes and jobs
- Simulate dynamic billing, verification, and job completion — all from the user’s perspective

---

## 🧑‍💻 User Flow

1. **Job Selection**
   - Choose a predefined training task (CartPole PPO, Mini-LLaMA stub, etc.)
   - Simulated dataset & model config shown

2. **Job Submission + Cost Estimation**
   - Preview job cost (based on task + duration)
   - Simulate budget lock from GNS wallet

3. **Swarm Training**
   - Job picked up by simulated swarm nodes
   - Training metrics update in real time
   - Logs show node activity and rewards
   - Contract-like logs simulate job lifecycle

4. **Job Complete**
   - Summary screen with final reward
   - Simulated model file download
   - Invoice + verification trail

---

## 🧠 What It Visualizes

| Perspective                  | Insight Provided                                 |
|-----------------------------|--------------------------------------------------|
| 📈 Model Training            | Reward per episode, faster swarm convergence     |
| 🐝 Node Activity             | Node-level job pickups, training durations       |
| 🌐 Protocol Events           | JobAccepted, JobCompleted, VerifierChallenge     |
| 💰 Billing Flow              | Real-time GNS burn, final cost, refund           |
| 🧾 Verifier Logs             | Swarm integrity, challenge-responses, rewards    |

---

## 🛠️ Tech Stack

### 🖥 Frontend
- **Next.js** + **Tailwind CSS** — clean UI framework
- **Recharts** — interactive metrics graphs
- **Axios** — for loading mock JSON log data
- **Framer Motion** — for polished animations
- **Monaco Editor (optional)** — advanced IDE-style input

### 💡 Backend?
- ❌ No backend required for this bounty
- ✅ All training/job/contract logs are **simulated via static JSON files**

### 🪙 Token + Contract Simulation
- JSON log files with timestamped `JobAccepted`, `TrainingStarted`, `VerifierDispute`
- Local GNS token simulation
- Pre-auth + refund logic mocked in UI only

## 🚀 Getting Started

```bash
# Frontend Setup
cd frontend
npm install
npm run dev
