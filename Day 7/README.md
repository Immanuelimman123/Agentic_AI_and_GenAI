# 🤖 Flask Gemini AI – Question Answering Web Application

Flask Gemini AI is a simple AI-powered question-answering web application built using **Python Flask** and **Google Gemini API**.

The application provides an interactive web interface where users can enter questions and receive AI-generated answers using Google's Gemini language model.

It demonstrates the integration of Flask web development with Generative AI to build a simple and interactive AI application.

## 🚀 Features

### 💬 AI Question Answering
- Allows users to enter questions through a web interface.
- Generates intelligent responses using the Google Gemini API.
- Displays AI-generated answers dynamically on the webpage.
- Supports different types of general questions.

### 🌐 Flask Web Application
- Built using the Python Flask framework.
- Uses Flask routing to handle HTTP GET and POST requests.
- Processes user input through HTML forms.
- Renders dynamic responses using Jinja2 templates.

### 🧠 Gemini AI Integration
- Integrates Google's Gemini API.
- Uses the Gemini model for content generation.
- Processes user questions and returns generated responses.

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Flask | Backend web framework |
| Google Gemini API | AI-powered response generation |
| HTML5 | Webpage structure |
| Jinja2 | Dynamic HTML rendering |
| Google Gen AI SDK | Gemini API integration |

## 📂 Project Structure

```text
Flask-Gemini-AI/
│
├── app.py
├── templates/
│   └── index.html
├── .env
├── .gitignore
└── requirements.txt
```

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone https://github.com/Immanuelimman123/Flask-Gemini-AI.git
cd Flask-Gemini-AI
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

### 4. Configure the Gemini API Key

Create a `.env` file in the project directory:

```env
GEMINI_API_KEY=your_gemini_api_key
```

Get your API key from [Google AI Studio](https://aistudio.google.com/apikey).

**Important:** Never upload your `.env` file or expose your API key on GitHub.

### 5. Run the Application

```bash
python app.py
```

Open your browser and visit:

```text
http://127.0.0.1:5000/
```

## 🔄 Application Workflow

1. User opens the Flask web application.
2. The home page displays an HTML question input form.
3. User enters a question and submits the form.
4. Flask receives the question through a POST request.
5. The question is sent to the Google Gemini API.
6. Gemini generates an AI-powered response.
7. Flask passes the generated answer to the HTML template.
8. The answer is displayed on the webpage.

## 🔐 Environment Variables

| Variable | Description |
|---|---|
| `GEMINI_API_KEY` | API key used to access Google Gemini |

## 🔮 Future Enhancements

- Chat history and conversation management.
- Improved user interface using Bootstrap.
- Support for multiple Gemini models.
- Streaming AI responses.
- User authentication and session management.
- PDF-based question answering.
- Database integration for storing conversations.
- Deployment using cloud hosting platforms.

## 👨‍💻 Author

**Immanuel**

Python Developer | Exploring Flask and Generative AI

## 🔗 GitHub Repository

[Flask Gemini AI – Question Answering Application](https://github.com/Immanuelimman123/Flask-Gemini-AI)

---

⭐ If you find this project useful, consider giving it a star!

**Explore Generative AI with Flask and Gemini! 🚀**
