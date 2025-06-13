# LiteLLm_agent_sdk
🤖 LiteLLM for routing to Google Gemini (and other models)

🧠 OpenAI Agent SDK for creating an LLM-powered agent

🔐 .env support for keys and configuration

✅ Your README.md File (Copy this)
markdown
Copy
Edit
# 🤖 Agentic AI with LiteLLM + Google Gemini

This project uses the **OpenAI Agent SDK** with **LiteLLM** to access **Google Gemini** via a unified interface. You can also switch between OpenAI, Claude, Mistral, and more by changing just one line.

---

## 🌟 Features

- 🔄 Route to Google Gemini using LiteLLM
- 🧠 Create intelligent agents with OpenAI Agent SDK
- ⚡ Easily swap models (Claude, GPT-4, Gemini, Mistral, etc.)
- 🔐 Secure key management with `.env`

---

## 🧠 Tech Stack

- [Python 3.8+](https://www.python.org/)
- [LiteLLM](https://docs.litellm.ai/)
- [OpenAI Agents SDK](https://github.com/openai/openai-python)
- [python-dotenv](https://pypi.org/project/python-dotenv/)

---

## ⚙️ Installation

1. **Clone the repository**

```bash
git clone https://github.com/your-username/agentic-gemini.git
cd agentic-gemini
Set up a virtual environment

bash
python -m venv venv
source venv/bin/activate  # Windows: venv\Scripts\activate
Install requirements

bash

pip install -r requirements.txt
📦 Requirements (requirements.txt)
text
Copy
Edit
litellm
python-dotenv
openai  # Needed for Agent SDK
🔐 Environment Variables (.env)
Create a .env file in the root directory with your Gemini API key:

env

LITELLM_MODEL=gemini/gemini-pro
LITELLM_API_KEY=your-google-gemini-api-key
LITELLM_API_BASE=https://generativelanguage.googleapis.com/v1beta
🚀 Usage
Example main.py:

python

import os
from openai import Assistant
from dotenv import load_dotenv
import litellm

load_dotenv()

# Set LiteLLM config
litellm.model_alias_map["default"] = os.getenv("LITELLM_MODEL")
litellm.api_base = os.getenv("LITELLM_API_BASE")
litellm.api_key = os.getenv("LITELLM_API_KEY")

# Example Agent (replace with your tool logic)
assistant = Assistant(name="Gemini Agent")

@assistant.function()
def hello(name: str) -> str:
    return f"Hello, {name}!"

if __name__ == "__main__":
    response = assistant.run("Say hello to Hiba")
    print(response)
✅ Model IDs for Google Gemini (via LiteLLM)
gemini/gemini-pro

gemini/gemini-1.5-pro-latest

Check LiteLLM model list for updates.

📄 License
MIT License

🙋‍♀️ Author
Built with 💙 by Hiba Meo
GitHub | OpenRouter | LiteLLM Docs


Would you like me to:
- Create the actual folder with all these files and send you a ZIP?
- Add support for **model selection dropdown in Streamlit**?
- Add **tools** like search or math using Agent SDK?

Just let me know 💻✨
