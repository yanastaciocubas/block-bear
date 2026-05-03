# 🐻 Bloch-Bear
### Your warm & fuzzy guide to quantum computing

> *"Every quantum expert was once a confused beginner. Even this bear!"* 🐻

---

## What is Bloch-Bear?

Bloch-Bear is an AI-powered quantum computing education platform built for the **IBM Bob Dev Day Hackathon**. It combines three things in one browser tab:

1. 🐻 **Bloch** — a warm, encouraging AI bear tutor powered by IBM Bob
2. ⚛️ **Live quantum simulation** — real quantum circuits running in your browser via Pyodide + NumPy
3. 📖 **5-milestone curriculum** — from "Why does quantum computing exist?" to running your first QAOA algorithm

**Zero setup. No Jupyter. No IBM account needed to start. Just open and learn.**

---

## The 5 Milestones

| # | Title | What you learn |
|---|-------|---------------|
| 1 | 🌌 Why Quantum Computing Exists | The exponential gap, Grover's O(√N) speedup, Feynman's 1981 challenge |
| 2 | ⚛️ What Is a Qubit? | Superposition, Hadamard gate, qubits as Bernoulli random variables |
| 3 | 🔧 Quantum Gates & Circuits | H, X, Z, CNOT gates, Bell states, quantum entanglement |
| 4 | 📊 Quantum Noise | Depolarizing noise, decoherence, readout errors, real IBM hardware |
| 5 | 🚀 QAOA Algorithm | Max-Cut problem, hybrid quantum-classical optimization |

---

## Live Demo

👉 **[https://your-username.github.io/bloch-bear](https://your-username.github.io/bloch-bear)**

> First load takes ~20 seconds while Bloch wakes up from hibernation and installs the quantum libraries. This is normal! 🐻

---

## How to Use

1. Select a **milestone** from the left sidebar
2. Click **📖 Concept** — read Bloch's explanation with data science analogies
3. Click **💻 Code** — see the quantum circuit code
4. Click **▶ Run Code 🐾** — execute it live in your browser
5. Click **🐻 Ask Bloch** — Bloch explains your output
6. Ask anything in the chat — Bloch answers with bear puns 🐾

---

## How to Run Locally

```bash
git clone https://github.com/your-username/bloch-bear.git
cd bloch-bear
open index.html
# or: python -m http.server 8080
```

No install. No npm. No build step. Just open the file.

---

## Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | Pure HTML + CSS + JavaScript |
| Python runtime | Pyodide v0.25.0 (WebAssembly) |
| Quantum simulation | NumPy statevector simulator (pure Python) |
| Optimization | SciPy (COBYLA optimizer for QAOA) |
| Visualization | Matplotlib (rendered as base64 PNG) |
| AI Tutor | IBM Bob (watsonx.ai) |
| Hosting | GitHub Pages |

> **Why NumPy instead of Qiskit-Aer?** Qiskit-Aer has C extensions that don't run in WebAssembly. Our pure-NumPy quantum simulator implements the same gates (H, X, Z, CNOT, Ry, Rz) and statevector simulation natively — no backend required.

---

## Project Structure

```
bloch-bear/
├── index.html    ← entire app (open this!)
└── README.md     ← you are here 🐻
```

---

## How IBM Bob Is Used

IBM Bob powers **Bloch**, the AI tutor at the heart of the app. Every student question triggers an IBM Bob API call with:
- The current milestone as context
- The student's latest code output
- The last 6 messages of conversation history
- Bloch's bear personality system prompt

Bob's responses are rendered live in the chat panel with bear puns, data science analogies, and encouraging follow-up questions. Bob IS the product — without him, there's no Bloch.

---

## Why This Wins

**The problem:** Fewer than 10,000 people worldwide can write production Qiskit code. IBM's quantum computers sit underutilized because the talent pipeline is broken.

**The solution:** Bloch-Bear removes every barrier — no setup, no Jupyter, no prior quantum knowledge needed. A student goes from zero to running a real QAOA algorithm in one browser session.

**The differentiator:** The bear personality makes quantum approachable. The data science analogies (qubits = Bernoulli random variables, circuits = data pipelines) unlock quantum for the millions of data scientists who already speak that language.

---

*Built with 🐻 for the IBM Bob Dev Day Hackathon — May 2026*