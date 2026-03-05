# Simple LangGraph QA Workflow

This repository contains a foundational implementation of **LangGraph**, a library for building stateful, multi-actor applications with LLMs. 



## 🚀 Overview
Unlike standard linear chains, LangGraph allows for the creation of cyclical workflows and fine-grained state management. This specific project demonstrates a basic **Linear Graph** that:
1.  **Validates State**: Uses `TypedDict` to ensure data consistency.
2.  **Processes Input**: Logs and prepares user queries.
3.  **Generates AI Responses**: Connects to OpenAI's `gpt-4o` to generate answers within the graph structure.

## 🛠️ Tech Stack
* **Framework:** [LangGraph](https://github.com/langchain-ai/langgraph)
* **LLM Orchestration:** LangChain
* **Model:** OpenAI GPT-4o
* **Environment:** Python / Google Colab

## 📖 How it Works
1.  **State:** The `QAState` object travels through the graph, holding the `question` and the eventual `answer`.
2.  **Nodes:** Python functions (`user_input_node`, `answer_node`) that act on the state.
3.  **Edges:** Define the path. Here: `Start -> get_input -> llm_response -> End`.

