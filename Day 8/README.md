# Day 8 – Ollama & MCP Student Dashboard 🚀

## 📚 Topics Covered

1. Ollama – Local Large Language Models (LLMs)
2. Model Context Protocol (MCP)
3. Building an MCP Student Dashboard using FastMCP and Prefab UI

---

## 1. Ollama – Local LLMs

### 📖 Introduction

Ollama is a platform that allows users to run Large Language Models (LLMs) locally on their own computers.

It simplifies the process of downloading, managing, and running AI models without depending entirely on cloud-based AI services.

### 🔑 Key Concepts

- **Local LLM Execution:** Run AI models directly on a local machine.
- **Model Management:** Download, manage, and switch between different language models.
- **Privacy:** Prompts and responses can be processed locally instead of being sent to an external AI service.
- **Offline Usage:** Models can be used without an internet connection after they have been downloaded.
- **Model Support:** Supports various open-weight models such as Llama, Mistral, and Gemma.
- **API Integration:** Provides an API that allows applications to communicate with locally running models.

### ⚙️ Important Ollama Commands

| Command | Description |
|---|---|
| `ollama --version` | Check Ollama version |
| `ollama list` | Display downloaded models |
| `ollama pull llama3.2` | Download a model |
| `ollama run llama3.2` | Run a model |
| `ollama serve` | Start the Ollama service |
| `ollama rm llama3.2` | Remove a downloaded model |

### 💡 Applications of Ollama

- Local AI chatbots
- Question-answering systems
- AI-powered applications
- Integration with frameworks such as LangChain and LlamaIndex
- Private AI workflows

---

## 2. Model Context Protocol (MCP)

### 📖 Introduction

Model Context Protocol (MCP) is an open protocol that enables AI applications to communicate with external tools, resources, and data sources through a standardized interface.

It helps connect AI models and applications with external capabilities.

### 🔑 Key Concepts

- **MCP Server:** Exposes tools and resources to MCP clients.
- **MCP Client:** Connects to MCP servers and communicates with them.
- **Tools:** Functions that an AI application can discover and invoke.
- **Resources:** Data that can be provided to an MCP client.
- **Prompts:** Reusable prompt templates that can be exposed by an MCP server.

---

## 3. Project – MCP Student Dashboard 🎓

### 📌 Project Overview

Developed an interactive Student Dashboard using **FastMCP** and **Prefab UI**.

The project demonstrates how to create an MCP server and expose a dashboard interface through an MCP tool.

### 🚀 Features

- Interactive Student Dashboard
- MCP tool creation using FastMCP
- User interface powered by Prefab UI
- Displays student information
- Simple and lightweight project structure

### 🛠️ Technologies Used

- Python
- FastMCP
- Prefab UI
- UV – Python package and project manager

### 💻 Dashboard Information

- **Dashboard Title:** My Student Dashboard
- **Welcome Message:** Welcome to Python and AI!
- **Total Students:** 65
- **Course:** Generative AI

### 🔗 GitHub Repository

[MCP Student Dashboard – GitHub](https://github.com/Immanuelimman123/MCP-Student-Dashboard)

---

## 🎯 Learning Outcomes

- Understood the fundamentals of Ollama and local LLM execution.
- Learned how local AI models can be managed and integrated into applications.
- Understood the architecture and purpose of Model Context Protocol.
- Explored MCP servers, clients, and tools.
- Built an interactive Student Dashboard using FastMCP and Prefab UI.

---

⭐ **Learning Generative AI – One Day at a Time!**
