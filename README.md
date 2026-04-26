# CSE 476 Final Project

**Team:** Jenna Skabelund, Kavish Sharma, Neil Shenoy

---

A general-purpose reasoning agent that solves arbitrary problem-solving tasks
using eight distinct inference-time techniques. The agent classifies each question
by domain and routes it through the most effective combination of techniques,
then uses LLM-as-a-Judge to select the best answer.

**Techniques implemented:**
1. Chain-of-Thought (CoT)
2. Self-Consistency
3. Best-of-N
4. Reflection
5. Step Decomposition
6. Iterative Refinement
7. LLM-as-a-Judge
8. Tool Use (Python eval for arithmetic)

---

## Prerequisites

- Python 3.8 or higher
- A valid ASU SOL API key 
- ASU VPN (Cisco AnyConnect)

---

## Setup

**1. Clone the repository**
```bash
git clone https://github.com/ksharm-67/NLP-final-project
cd NLP-final-project
```

**2. Install dependencies**
```bash
pip install -r requirements.txt
```

**3. Add your API key**

Open `agent.ipynb` and find Cell 1. Replace the placeholder with your key:
```python
API_KEY = "your-api-key-here"
```

**4. Connect to ASU VPN**

The API endpoint is only reachable from the ASU network.

**Note for Mac users:** If you see an SSL certificate error, add `verify=False` to
the `requests.post()` call in Cell 1 and add these two lines at the top of Cell 1:
```python
import urllib3
urllib3.disable_warnings(urllib3.exceptions.InsecureRequestWarning)
```

---

## Running the Agent

**1. Open the notebook**
```bash
jupyter notebook agent.ipynb
```

**2. Run all cells in order**

Go to `Kernel → Restart & Run All` or run each cell top to bottom manually.
Cell 1 must always be run first as it defines the API connection and all helper functions.

**3. Test the agent**


