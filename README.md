# 🤖 LangGraph AI Chatbot

This tool allows you to interact with advanced AI agents powered by OpenAI and Groq LLMs. It can optionally use web search (via Tavily) to improve responses. Built using LangGraph, FastAPI, and Streamlit.



Let’s say x wants to build a smart chatbot. He can define how the chatbot should behave using a system prompt, choose from powerful LLMs, and optionally enable web search. Then simply enter a query and get a smart, friendly response from the agent.

---

## 🧱 Technical Architecture



1. **Frontend (Streamlit)**: Allows user to define the chatbot, pick model/provider, and send a query.
2. **Backend (FastAPI)**: Receives the request, configures the AI agent, and returns the AI's response.
3. **Agent Layer (LangGraph)**: Uses selected LLM and optionally Tavily search for enhanced responses.

---

## ⚙️ Set-up

1. **Create your `.env` file** and add:
    ```env
    GROQ_API_KEY=your_groq_api_key
    TAVILY_API_KEY=your_tavily_api_key
    OPENAI_API_KEY=your_openai_api_key
    ```

2. **Install dependencies**:
    ```bash
    pipenv install
    pipenv shell
    ```

    > Or use:
    > ```bash
    > pip install -r requirements.txt
    > ```

3. **Run backend**:
    ```bash
    python backend.py
    ```

4. **Run frontend** in a new terminal:
    ```bash
    streamlit run frontend.py
    ```

---

## 🛠 Features

- Select between **Groq** and **OpenAI** models
- Enable or disable **Tavily web search**
- Define custom **system prompt**
- Simple UI to interact with chatbot

---

## 🧠 Supported Models

- **Groq**: 
  - `llama-3.3-70b-versatile`
  - `mixtral-8x7b-32768`
  
- **OpenAI**: 
  - `gpt-4o-mini`

---




