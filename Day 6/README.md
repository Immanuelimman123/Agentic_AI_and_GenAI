# ANGO MODEL:
# 🎓 EduMate AI – Multi-Agent Educational Assistant

EduMate AI is an intelligent multi-agent educational assistant built using **Agno** and **Groq LLM**. It consists of four specialized AI agents that collaborate through a central Education Manager to help students understand programming concepts, practice quizzes, generate code, and prepare study notes.

The system automatically identifies the student's request and delegates the task to the most suitable agent to provide clear, structured, and beginner-friendly responses.

## 🚀 Features

### 🤖 Specialized AI Agents

#### 1. Tutor Agent
- Explains technical concepts in simple English.
- Provides step-by-step explanations.
- Uses real-world examples to improve understanding.
- Helps students understand programming fundamentals.

#### 2. Quiz Agent
- Generates multiple-choice questions (MCQs).
- Provides four options for every question.
- Identifies correct answers with explanations.
- Adjusts question difficulty according to the student's level.

#### 3. Coding Agent
- Generates clean and beginner-friendly Python programs.
- Explains code line by line when requested.
- Identifies programming errors and suggests corrections.
- Provides practical coding examples.

#### 4. Notes Agent
- Creates structured educational study notes.
- Includes definitions, key points, and real-world examples.
- Highlights important examination topics.
- Provides short revision summaries.

### 🧠 Multi-Agent Collaboration
- Built using the Agno multi-agent framework.
- Uses an Education Manager to coordinate specialized agents.
- Delegates tasks to the appropriate agent based on the student's request.
- Generates student-friendly responses using Markdown formatting.

## 🏗️ System Architecture

```text
                 Student Input
                       |
                       v
          +---------------------------+
          |       EduMate AI          |
          |    Education Manager      |
          |     (Agno Team)           |
          +---------------------------+
                       |
          +------------+-------------+
          |            |             |
          v            v             v
     Tutor Agent   Quiz Agent   Coding Agent
          |            |             |
          +------------+-------------+
                       |
                       v
                  Notes Agent
                       |
                       v
             Groq - GPT-OSS-120B
                       |
                       v
             Student-Friendly Response
```

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Agno | AI agent and team orchestration |
| Groq | LLM inference |
| GPT-OSS-120B | Language model |
| python-dotenv | Environment variable management |

## 📂 Project Structure

```text
EduMate-AI/
│
├── app.py
├── .env              # Local environment variables (not uploaded)
├── .gitignore
└── requirements.txt
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Immanuelimman123/EduMate-AI.git
cd EduMate-AI
```

### 2. Create a Virtual Environment

```bash
python -m venv venv
```

Activate the environment:

**Windows:**
```bash
venv\Scripts\activate
```

**macOS / Linux:**
```bash
source venv/bin/activate
```

### 3. Install Dependencies

```bash
pip install -r requirements.txt
```

### 4. Configure the Groq API Key

Create a `.env` file in the project directory:

```env
GROQ_API_KEY=your_groq_api_key
```

Get your API key from [Groq Console](https://console.groq.com/keys).

**Important:** Never upload your `.env` file or expose your API key on GitHub.

### 5. Run the Application

```bash
python app.py
```

## 💡 Example Interactions

| Student Request | Responsible Agent |
|---|---|
| Explain Python functions with a simple example. | Tutor Agent |
| Create 5 beginner-level MCQs about Python lists. | Quiz Agent |
| Write a Python program to check prime numbers. | Coding Agent |
| Prepare study notes about Python OOP concepts. | Notes Agent |

## 🔄 Application Workflow

1. Student enters a question through the terminal.
2. EduMate AI receives the student's request.
3. The Education Manager processes the request.
4. The appropriate specialized agent is selected.
5. The selected agent generates a response using the configured Groq model.
6. The response is displayed to the student in the terminal.

## 🔐 Environment Variables

The application requires the following environment variable:

| Variable | Description |
|---|---|
| `GROQ_API_KEY` | API key used to access the Groq model |

## 🔮 Future Enhancements

- Streamlit-based interactive user interface.
- Support for multiple programming languages.
- PDF-based question answering.
- Personalized learning recommendations.
- Student progress tracking.
- Quiz performance evaluation.
- Integration with additional LLM providers.
- Conversation history and memory support.

## 👨‍💻 Author

**Immanuel**

AI & Python Developer | Exploring Generative AI and Multi-Agent Systems

## 🔗 GitHub Repository

[EduMate AI – Multi-Agent Educational Assistant](https://github.com/Immanuelimman123/EduMate-AI)

---

⭐ If you find this project useful, consider giving it a star!

**Happy Learning with EduMate AI! 🎓**
