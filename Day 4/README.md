# Day 4 - 1. Multi-PDF RAG Question Answering

## Project Overview

This project implements a Multi-PDF Question Answering system using Retrieval-Augmented Generation (RAG). Users can upload multiple PDF documents and ask questions based on their content.

## Technologies Used
- Python
- LangChain
- FAISS
- Hugging Face Embeddings
- OpenRouter API
- Gradio

## Key Features
- Upload multiple PDF documents.
- Extract and split PDF text into chunks.
- Generate embeddings using Hugging Face.
- Store and retrieve relevant content using FAISS.
- Generate answers using an LLM through OpenRouter.
- Display the source PDF documents.

## Practice Notebook

[**Open Multi-PDF RAG Notebook in Google Colab**](https://colab.research.google.com/drive/1t9OdI6AviAcNqDTKzJaNfCQzmSOJv7U-)

# Day 4 – 2. RAG-Based Question Answering Chatbot

## 📌 Project Overview

This project demonstrates a Retrieval-Augmented Generation (RAG) based Question Answering Chatbot built using Python, LangChain, FAISS, Hugging Face Embeddings, and Google Gemini.

The chatbot uses a CSV dataset containing questions and answers. When a user submits a question, the system retrieves the most relevant information from the dataset using semantic similarity search and generates an answer using the Gemini language model.

The chatbot is designed to answer questions based only on the retrieved context. If relevant information is unavailable, it responds with **"No relevant Q&A found."**

## 🚀 Technologies Used

- Python
- Pandas
- LangChain
- Hugging Face Sentence Transformers
- FAISS Vector Database
- Google Gemini API
- Google Colab

## ✨ Key Features

- Load question-and-answer data from a CSV file.
- Convert CSV records into LangChain documents.
- Generate text embeddings using Hugging Face.
- Store and search embeddings using FAISS.
- Retrieve the top 3 relevant documents for each question.
- Generate context-based answers using Google Gemini.
- Handle temporary Gemini API errors with retry logic.
- Interactive terminal-style chatbot.

## ⚙️ How It Works

1. **Dataset Loading:** Load the CSV file containing questions and answers using Pandas.
2. **Document Creation:** Convert each question-and-answer pair into a LangChain document.
3. **Embedding Generation:** Generate vector embeddings using `sentence-transformers/all-MiniLM-L6-v2`.
4. **Vector Database:** Store the generated embeddings in FAISS.
5. **Similarity Search:** Retrieve the top 3 relevant documents based on the user's question.
6. **Answer Generation:** Pass the retrieved context and user question to Google Gemini.
7. **Response:** Display the generated answer in the chatbot.

## 📂 Dataset Format

The CSV file should contain these columns:

| Column | Description |
|---|---|
| question | Stores the questions |
| answer | Stores the corresponding answers |

Example:

| question | answer |
|---|---|
| What is Python? | Python is a high-level programming language. |
| What is FAISS? | FAISS is a library for efficient similarity search. |

## 📦 Installation

Install the required libraries:

```python
!pip install pandas langchain langchain-community langchain-core langchain-huggingface langchain-google-genai faiss-cpu sentence-transformers
```

## 🔑 API Configuration

The project uses the Google Gemini API.

Generate an API key from Google AI Studio:

https://aistudio.google.com/apikey

The notebook securely requests the API key using:

```python
from getpass import getpass
import os

os.environ["GOOGLE_API_KEY"] = getpass("Enter Gemini API Key: ")
```

Do not upload or share your API key publicly.

## ▶️ How to Run

1. Open the notebook using Google Colab.
2. Upload the required CSV dataset.
3. Install the required Python libraries.
4. Configure your Google Gemini API key.
5. Execute the notebook cells in order.
6. Start asking questions through the chatbot.
7. Type `exit` to stop the chatbot.

## 💬 Sample Interaction

```text
RAG Chatbot is Running!
Type 'exit' to stop.

You: What is Python?

Bot: Python is a high-level, interpreted programming language.
It is popular for its simple syntax and wide range of applications.

You: What is FAISS?

Bot: FAISS is a library for efficient similarity search and clustering of dense vectors.

You: exit

Goodbye!
```

## 📚 Practice Notebook

[**Open RAG Chatbot in Google Colab**](https://colab.research.google.com/drive/1s203fIULq3kj6oq1BwKc3WCx_J2q8PDW)

## 🎯 Learning Outcomes

Through this project, I learned:

- Fundamentals of Retrieval-Augmented Generation (RAG).
- Working with LangChain document objects.
- Generating embeddings using Hugging Face.
- Creating vector databases using FAISS.
- Performing semantic similarity search.
- Integrating Google Gemini with LangChain.
- Building a context-based Question Answering chatbot.

---

**Project:** RAG-Based Question Answering Chatbot  
**Environment:** Google Colab  
**Language:** Python

# Day 4 - 3. OpenRouter LLM Integration – Python Question Answering

## 📌 Project Overview

This project demonstrates how to integrate a Large Language Model (LLM) into Python using the OpenRouter API.

It uses the OpenRouter Python SDK to connect with the `baidu/ernie-5.5-flash-preview:free` model and generate responses to user prompts.

The project demonstrates API key configuration, model invocation, response handling, and displaying AI-generated answers.

## 🚀 Technologies Used

- Python
- OpenRouter API
- OpenRouter Python SDK
- ERNIE 5.5 Flash Preview
- Google Colab

## ✨ Key Features

- Integrates Python with OpenRouter.
- Uses an API key for authentication.
- Connects to the ERNIE 5.5 Flash Preview model.
- Sends natural-language prompts to the model.
- Generates AI-powered responses.
- Handles response status and error messages.
- Displays generated text in the Python environment.

## ⚙️ How It Works

1. **Library Installation:** Install the OpenRouter Python SDK.
2. **API Configuration:** Configure the OpenRouter API key using an environment variable.
3. **Client Initialization:** Initialize the OpenRouter client.
4. **Model Selection:** Select the `baidu/ernie-5.5-flash-preview:free` model.
5. **Prompt Submission:** Send a question or instruction to the model.
6. **Response Validation:** Check whether the response status is completed.
7. **Output Generation:** Extract and display the generated text.

## 📦 Installation

Install the required package:

```python
!pip install openrouter
```

## 🔑 API Configuration

Create an API key from OpenRouter:

https://openrouter.ai/keys

Configure the API key using an environment variable:

```python
import os
from getpass import getpass

os.environ["OPENROUTER_API_KEY"] = getpass("Enter OpenRouter API Key: ")

key = os.getenv("OPENROUTER_API_KEY")

print("API Key Loaded:", key is not None)
```

**Security:** Never hardcode your API key or upload it to GitHub.

## 💻 Implementation

Import the required libraries:

```python
from openrouter import OpenRouter
import os
```

Initialize the OpenRouter client and send a prompt:

```python
with OpenRouter(api_key=os.getenv("OPENROUTER_API_KEY")) as client:
    response = client.responses.send(
        model="baidu/ernie-5.5-flash-preview:free",
        input="Explain the concept of dictionary in python?"
    )

    if response.status != "completed":
        message = response.error.message if response.error else f"Response ended as {response.status}"
        raise RuntimeError(message)

    message = next(item for item in response.output if item.type == "message")

    print(next(part.text for part in message.content if part.type == "output_text"))
```

## 💬 Sample Interaction

**Input:**

```text
Explain the concept of dictionary in python?
```

**Generated Output:**

A dictionary in Python is a built-in mutable mapping data structure that stores key-value pairs.

Example:

```python
person = {
    "name": "Alice",
    "age": 30,
    "active": True
}
```

Dictionaries store data using unique keys and their corresponding values.

## ▶️ How to Run

1. Open the notebook in Google Colab.
2. Install the OpenRouter Python package.
3. Generate an OpenRouter API key.
4. Configure the API key securely.
5. Execute the notebook cells.
6. Enter your prompt and view the generated response.

## 🎯 Learning Outcomes

Through this project, I learned:

- How to integrate Python applications with OpenRouter.
- How to configure and use API keys.
- How to initialize an OpenRouter client.
- How to select and invoke an LLM.
- How to send prompts and process model responses.
- How to handle API response status and errors.

## 📚 Practice Notebook

[**Open OpenRouter LLM Integration Notebook in Google Colab**](https://colab.research.google.com/drive/1Qh9gjWNP7aVjVtM0QVpebOUxAeVv_8Q7)

---

**Project:** OpenRouter LLM Integration  
**Model:** ERNIE 5.5 Flash Preview  
**Language:** Python  
**API Provider:** OpenRouter
