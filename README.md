# EDA--Agent
Agentic EDA Pipeline: Autonomous Data Exploration & Synthesis Engine

# 🤖 Agentic EDA Pipeline: Autonomous Data Exploration & Synthesis Engine

An autonomous Agentic AI system built with **LangChain**, **Meta Llama 3**, and **Python REPL** that completely automates the Exploratory Data Analysis (EDA) lifecycle. The agent ingests raw tabular data and generates comprehensive statistical analyses, visualizations, and insights—all through autonomous code generation and execution.

---

## 📋 Prerequisites

Before cloning and running this project, ensure you have the following installed:

- **Python 3.10+** - [Download Python](https://www.python.org/downloads/)
- **Git** - [Download Git](https://git-scm.com/downloads)
- **pip** (comes with Python)

---

## 🔧 Installation & Setup

### Step 1: Clone the Repository

Choose one of the following methods to clone the repository:

#### Method 1: HTTPS (Recommended for most users)
```bash
git clone https://github.com/lovey7768/EDA--Agent.git
cd EDA--Agent
```

#### Method 2: SSH (If you have SSH keys configured)
```bash
git clone git@github.com:lovey7768/EDA--Agent.git
cd EDA--Agent
```

#### Method 3: GitHub CLI
```bash
gh repo clone lovey7768/EDA--Agent
cd EDA--Agent
```

#### Method 4: Download as ZIP
1. Visit [https://github.com/lovey7768/EDA--Agent](https://github.com/lovey7768/EDA--Agent)
2. Click the green "Code" button
3. Select "Download ZIP"
4. Extract the ZIP file and navigate to the folder

### Step 2: Create a Virtual Environment (Recommended)

Creating a virtual environment keeps dependencies isolated from your system Python.

#### On Windows:
```bash
python -m venv venv
venv\Scripts\activate
```

#### On macOS/Linux:
```bash
python3 -m venv venv
source venv/bin/activate
```

### Step 3: Install Dependencies

Install all required packages from the requirements.txt file:

```bash
pip install -r requirements.txt
```

### Step 4: Configure API Keys

Create a `.env` file in the project root directory:

```bash
# Create .env file
cat > .env << EOF
GROQ_API_KEY=your_groq_api_key_here
LLAMA_MODEL=meta-llama-3-70b-instruct
EOF
```

**Or manually create `.env` with:**
```
GROQ_API_KEY=your_groq_api_key_here
LLAMA_MODEL=meta-llama-3-70b-instruct
```

Get your free Groq API key from [Groq Console](https://console.groq.com/)

### Step 5: Run the Application

#### Option A: Use Jupyter Notebook
```bash
jupyter notebook
```
Then open the main notebook file and execute cells to start the EDA Agent.

#### Option B: Run Python Script
```bash
python main.py
```

---

## 🎯 Motivation & Core Value

Traditional Exploratory Data Analysis (EDA) requires writing repetitive boilerplate code across Pandas, Matplotlib, and Seaborn. Standard LLMs often hallucinate when calculating exact statistical metrics.

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
   ┌────────────────┐ ┌────────────────┐ ┌────────────────┐ ┌──────────────────┐
   │ Schema & Null  │ │ IQR & Z-Score  │ │ Distribution & │ │ Executive Data   │
   │ Data Audit     │ │ Outlier Check  │ │ Matrix Plots   │ │ Insights Report  │
   └────────────────┘ └────────────────┘ └────────────────┘ └──────────────────┘
            │                 │                 │                 │
            └─────────────────┴─────────────────┴─────────────────┘
                              │
                              ▼
                    ┌──────────────────────┐
                    │ Comprehensive EDA    │
                    │ Report & CSV Export  │
                    └──────────────────────┘
```

---

## 🚀 Quick Start Example

```python
from eda_agent import EDAAgentic

# Initialize the agent
eda_agent = EDAAgentic(
    csv_path="path/to/your/dataset.csv",
    llm_model="meta-llama-3-70b-instruct"
)

# Run autonomous EDA
report = eda_agent.analyze()

# Access results
print(report.summary)
print(report.statistics)
```

---

## 📁 Project Structure

```
EDA--Agent/
├── notebooks/           # Jupyter notebooks with agent implementation
├── src/                 # Source code modules
├── data/               # Sample datasets
├── results/            # Generated reports and visualizations
├── requirements.txt    # Python dependencies
├── .env.example        # Example environment variables
└── README.md          # This file
```

---

## 🔑 Key Features

✅ **Fully Autonomous** - Zero manual intervention required  
✅ **Deterministic** - Python REPL ensures accuracy  
✅ **Intelligent Reasoning** - LangChain + Llama 3 reasoning loops  
✅ **Fast Execution** - Groq LPU acceleration  
✅ **Comprehensive Output** - Statistical analysis + visualizations  

---

## 📚 Dependencies

- `langchain` - Agent orchestration framework
- `pandas` - Data manipulation
- `numpy` - Numerical computing
- `matplotlib` & `seaborn` - Visualization
- `groq` - LLM API client
- `jupyter` - Notebook environment
- `python-dotenv` - Environment variable management

---

## 🛠️ Troubleshooting

### Common Issues

**Issue: `ModuleNotFoundError` when importing libraries**
```bash
# Solution: Ensure virtual environment is activated and dependencies installed
pip install -r requirements.txt
```

**Issue: API key not recognized**
```bash
# Solution: Verify .env file is in project root and properly formatted
cat .env  # Check contents
```

**Issue: Jupyter notebook kernel issues**
```bash
# Solution: Install ipykernel and add environment to Jupyter
python -m ipykernel install --user --name=eda-agent
```

**Issue: Git clone fails with permission denied**
```bash
# Solution: Use HTTPS method instead of SSH, or configure SSH keys
git clone https://github.com/lovey7768/EDA--Agent.git
```

---

## 📝 License

This project is provided as-is for educational and research purposes.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit issues and pull requests.

---

## 📧 Support

For issues, questions, or suggestions, please open a GitHub issue in the repository.

---

**Happy Exploring! 🚀**
