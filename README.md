# 🌀 RecurLens v2.0: Recursive Meta-Cognition Engine

> **"Stop settling for the first thought. Let the machine think about how it thinks."**

![License](https://img.shields.io/badge/License-MIT-blue.svg)
![Status](https://img.shields.io/badge/Status-Operational-emerald)
![AI Core](https://img.shields.io/badge/Core-Gemini_2.5_Flash-purple)
![Reasoning](https://img.shields.io/badge/Logic-Recursive_Loop-rose)

**RecurLens** is not a chatbot. It is a **recursive multimodal meta-prompting engine**. It refuses to answer your question immediately. Instead, it ingests your reality (Vision + Audio), critiques its own understanding, refines its approach, and only executes when it has converged on an optimal strategy.

---

## 🧠 The Architecture

RecurLens operates on a **Human-in-the-Loop Recursive Cycle**:

```mermaid
graph LR
    A[Raw Input (Audio/Vision)] --> B{Initializer}
    B --> C[Meta-Prompt v0]
    C --> D{The Critic}
    D -- "Ambiguous?" --> E[Ask User Clarification]
    D -- "Flawed?" --> F[The Refiner]
    F --> C
    D -- "Converged (Score > 0.88)" --> G[Executor]
    G --> H[Deep Thinking Model]
    H --> I[Final Output + Visualization]
```

### 1. 👁️ Multimodal Cortex
*   **Vision Stream:** Analyzes images for spatial relations, objects, and *ambiguities*.
*   **Audio Stream:** Transcribes speech and detects **Emotional Tone** (Urgency, Frustration, Curiosity) to adjust the personality of the response.

### 2. 🔄 The Loop (The "Ghost" in the Machine)
The system enters a `while(true)` loop of self-improvement:
*   **The Critic:** A harsh evaluator that scores the current plan on Clarity, Safety, and Logic.
*   **The Refiner:** Rewrites the prompt to address the Critic's complaints.
*   **Convergence:** Calculates **Cosine Similarity** between iterations to detect when the idea has stabilized.

### 3. ⚡ Cognitive Execution
Once the prompt is perfect, it is fed into **Gemini 2.5** with a reserved `thinkingBudget` of 4096 tokens. It generates:
*   The Final Answer (Markdown)
*   A Visual Artifact (Image Generation)
*   A Neural Speech Output (TTS)

---

## 🚀 Installation & Initialization

### Prerequisites
*   Node.js 18+
*   A Google Cloud Project with **Gemini API** access (Paid tier required for Thinking/Search features).

### 1. Clone the Neural Link
```bash
git clone https://github.com/your-username/recurlens.git
cd recurlens
```

### 2. Install Dependencies
```bash
npm install
```

### 3. Ignite
```bash
npm run dev
```

---

## 🎮 Operational Manual

### 🔑 The Key
You will be prompted for a **Gemini API Key** upon startup. This key is stored in memory only.
> **Note:** RecurLens uses `gemini-2.5-flash`, `gemini-2.5-flash-image`, and `gemini-2.5-flash-preview-tts`.

### 🛡️ Modes of Operation
1.  **Troubleshoot:** Upload a server log screenshot + explain the crash. RecurLens will hypothesize root causes before answering.
2.  **Creative:** Ask for a sci-fi novel intro. RecurLens will define the themes and tone before writing a single word.
3.  **Planning:** Ask for a travel itinerary. RecurLens will identify missing constraints (budget, interests) and ask you clarification questions before planning.

### 🐛 Debugging the Mind
Click the **Bug Icon** in the header to reveal the `[RAW]` logs.
*   See exactly what the **Critic** hates about your prompt.
*   Watch the **Refiner** rewrite the JSON schema in real-time.

---

## 🛠️ Tech Stack

*   **Frontend:** React 19 + TypeScript + Vite
*   **Styling:** Tailwind CSS (Glassmorphism UI)
*   **AI SDK:** `@google/genai` (Official V2 SDK)
*   **Schemas:** Strict JSON enforcement via `responseSchema`.
*   **Audio:** Native Web Audio API for PCM decoding/encoding.

---

## ⚠️ Safety Protocols

RecurLens includes a dedicated **Risk Analysis** module in the meta-prompt state.
If the requested task involves high-risk topics, the system will:
1.  Flag the risk level to `HIGH`.
2.  Inject a `mitigation` strategy into the execution plan.
3.  Prepend a Safety Advisory to the final output.

---

## 🔮 Future Roadmap

*   [ ] **Vector Memory:** Long-term storage of successful prompt patterns.
*   [ ] **Tool Use:** Allow the Executor to run Python code directly in the browser.
*   [ ] **Swarm Mode:** Multiple Critics debating via the Live API.

---

> *"The first answer is rarely the best answer."*

