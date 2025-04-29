# 💬 LangGraph Multi-Agent Chatbot with Azure OpenAI (GPT-4o)

This project demonstrates a **multi-agent chatbot system** built using [LangGraph](https://docs.langchain.com/langgraph/), [LangChain](https://www.langchain.com/), and [Azure OpenAI GPT-4o](https://learn.microsoft.com/en-us/azure/cognitive-services/openai/overview). It enables intelligent routing of user queries to specialized agents that can handle:

- 📦 Product Q&A (e.g., laptop features, specifications)
- 📑 Order Management (e.g., order status, updates)
- 💬 Small Talk (greetings, goodbyes)

The chatbot is designed to operate inside **Google Colab**, using `userdata` for secure credential handling and modular notebooks for agent logic.

---

## 🚀 Features

- ✅ **Agent Routing with LangGraph**
- 🤖 **GPT-4o via Azure OpenAI API**
- 🛍️ Product Q&A Agent
- 📦 Order Management Agent
- 🗨️ Small Talk Handler
- 🧠 Memory Management via `thread_id`
- 📈 Visualize Agent Flow using Mermaid.js

---

## 📁 Project Structure

```text
├── product_qna_agentic_chatbot.ipynb       # Defines Product QnA agent
├── orders_chatbot_custom_agent_langgraph.ipynb  # Defines Order management agent
├── multi_agent_system_langgraph.ipynb           # Main router agent and orchestrator
├── README.md                               # You are here
```

## 🔧 Setup Instructions
### 1. Clone the Repository

```bash
git clone https://github.com/shaadclt/Multi-Agent-System-LangGraph.git
cd Multi-Agent-System-LangGraph
```
### 2. Open `multi_agent_system_langgraph.ipynb` in Google Colab

### 3. Add Azure Credentials to Colab userdata

```python
import os
from google.colab import userdata

os.environ["AZURE_OPENAI_API_KEY"] = userdata.get('AZURE_OPENAI_API_KEY')
os.environ["AZURE_OPENAI_ENDPOINT"] = userdata.get('AZURE_OPENAI_ENDPOINT')
```

### 4. Run the Notebook Cells

## 🧠 Conversation Flow Example
```text

USER : How are you doing?

AGENT : Hello! I’m here to assist you with laptop features or order updates.

USER : Please show me the details of the order ORD-7311

AGENT : Your order ORD-7311 is currently being processed and will ship soon.

USER : Tell me about the features of SpectraBook laptop

AGENT : SpectraBook features include a 13” OLED display, 16GB RAM, and a 512GB SSD.
```

## 🧱 Built With
- LangGraph

- LangChain

- Azure OpenAI

- Python 3.10+

- Google Colab

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE.txt) file for details.

## ✨ Acknowledgements
Thanks to:

- LangChain & LangGraph Teams

- Microsoft Azure OpenAI

- OpenAI GPT-4o for powering intelligent conversations
