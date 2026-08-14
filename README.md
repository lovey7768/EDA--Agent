# EDA--Agent
Agentic EDA Pipeline: Autonomous Data Exploration &amp; Synthesis Engine
# 🤖 Agentic EDA Pipeline: Autonomous Data Exploration & Synthesis Engine

An autonomous Agentic AI system built with **LangChain**, **Meta Llama 3**, and **Python REPL** that completely automates the Exploratory Data Analysis (EDA) lifecycle. The agent ingests raw tabular datasets, inspects schemas, audits missing values, identifies statistical outliers, dynamically generates distribution charts, and produces executive insight summaries with zero human intervention.

---

## 🎯 Motivation & Core Value

Traditional Exploratory Data Analysis (EDA) requires writing repetitive boilerplate code across Pandas, Matplotlib, and Seaborn. Standard LLMs often hallucinate when calculating exact statistical metrics over thousands of rows.

This project bridges **Generative AI Reasoning** with **Deterministic Python Code Execution**:
- The **LLM (Llama 3)** acts as the cognitive planner, reasoning through statistical requirements.
- The **Python REPL Tool** executes code directly against in-memory data frames, ensuring mathematical precision, zero hallucinated numbers, and real-time visualization generation.

---

## ⚙️ System Architecture & Workflow

```text
┌─────────────────────────┐
│ Raw Dataset (.csv/.df)  │
└───────────┬─────────────┘
            │
            ▼
┌─────────────────────────┐      Reasoning Loop      ┌─────────────────────────┐
│ LangChain Agent Manager │ ◄──────────────────────► │  Meta Llama 3           │
│ (Tool-Calling Engine)   │    (ReAct Strategy)      │  (Groq LPU Acceleration)│
└───────────┬─────────────┘                          └─────────────────────────┘
            │
            ├─────────────────┬─────────────────┬─────────────────┐
            ▼                 ▼                 ▼                 ▼
   ┌────────────────┐ ┌────────────────┐ ┌────────────────┐ ┌────────────────┐
   │ Schema & Null  │ │ IQR & Z-Score  │ │ Distribution & │ │ Executive Data │
   │ Data Audit     │ │ Outlier Check  │ │ Matrix Plots   │ │ Insights Report│
   └────────────────┘ └────────────────┘ └────────────────┘ └────────────────┘
