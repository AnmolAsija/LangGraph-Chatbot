# 🚀 LangGraph Multi-Tool AI Chatbot

An intelligent, modular, multi-tool AI chatbot built using LangGraph, LangChain, and Streamlit, featuring persistent conversation threads, multiple tools, and a scalable tool-node architecture.

# 📌 Overview:-

This project is a production-ready AI chatbot built with LangGraph, designed to handle multi-turn conversations while dynamically using different tools such as:
🔍 DuckDuckGo Web Search
📈 Live Stock Price Fetcher
🧮 Calculator Tool
💬 Thread-based persistent conversation memory

It provides a modular, maintainable, scalable backend architecture, ideal for building advanced AI agents and automation systems.
The frontend is built in Streamlit, supporting:
Multiple chat sessions
Persistent threads
Smooth UI for interacting with all tools

# ✨ Features
🧠 1. Multi-turn AI Chat
Maintains long conversations with context using thread IDs.

🔧 2. Modular Tool-Node Architecture
Tools are added as separate nodes in LangGraph, making the system scalable.

🗂 3. Persistent Threads (SQLite)
Every chat session is stored in a local SQLite database.

🌍 4. DuckDuckGo Search Tool
Real-time web search inside the chatbot.

📉 5. Stock Price Tool
Fetches live stock prices using external APIs.

🧮 6. Calculator Tool
Performs numeric evaluations through a safe calculator function.

🎨 7. Streamlit Frontend
User-friendly UI with multi-session support.

# 🏗 Architecture

                        ┌──────────────────┐
             │   User Input      │
             └─────────┬────────┘
                       │
             ┌─────────▼───────────┐
             │   LangGraph Engine   │
             └─────────┬───────────┘
                       │
 ┌──────────────┬───────────────┬──────────────┐
 │              │               │              │
┌────▼─────┐ ┌─────▼─────┐ ┌──────▼─────┐ ┌─────▼────────┐ │ LLM Node │ │ Search Tool│ │Stock Tool │ │ Calculator │ └────▲─────┘ └─────▲─────┘ └──────▲─────┘ └─────▲────────┘ │ │ │ │

 └──────────────┴───────────────┴──────────────┘
                       │
           ┌───────────▼───────────┐
           │   Response Builder     │
           └───────────┬───────────┘
                       │
           ┌───────────▼───────────┐
           │ Streamlit Frontend UI │
           └────────────────────────┘


# 🛠 Tech Stack

Languages

Python

Core Frameworks

LangGraph

LangChain

Streamlit

Tools Used
DuckDuckGo Search API

Yahoo Finance API / Stock API

SQLite (Persistent threads)

AI Models

You can use:

Groq LLaMA

OpenAI

HuggingFace LLMs
(or any model supported by LangChain)


# 📁 Project Structure
LangGraph-Chatbot/
│
├── app.py                 # Streamlit UI

├── graph.py               # LangGraph workflow and tool-node architecture

├── tools/

│   ├── search_tool.py  

│   ├── stock_tool.py 

│   ├── calculator_tool.py 

│
├── memory/
│   └── sqlite_memory.py   # Persistent thread logic

│
├── utils/
│   └── helpers.py        

│
├── README.md              # Documentation

└── requirements.txt       

# ⚙️ Installation
1. Clone the repository
git clone https://github.com/AnmolAsija/LangGraph-Chatbot.git
cd LangGraph-Chatbot

2. Create environment
pip install -r requirements.txt

3. Run the Streamlit App
streamlit run app.py



# 🚧 Future Improvements
Add more advanced tools (weather, news, calculator improvements)

Add authentication for users

Deploy on cloud (Streamlit Cloud / Render / Vercel)

Add vector memory for long-term conversation

Add voice input/output capabilities

# 🤝 Contributing
Pull requests are welcome.

For major changes, please open an issue first to discuss what you would like to change.

# 📬 Contact
Developer: Anmol Asija

📧 Email: anmolasija243@gmail.com

🔗 LinkedIn: https://www.linkedin.com/in/anmol-asija-991748289





