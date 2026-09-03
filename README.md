# 🤖 AI Business Assistant Chatbot

An intelligent **AI-powered Business Assistant** designed to help users interact with business data using natural language.

The system combines **Large Language Models (LLMs), Retrieval-Augmented Generation (RAG), SQL databases, and REST APIs** to provide intelligent answers to business-related questions.

---

## 📌 Project Overview

The AI Business Assistant allows users to ask questions about business operations in natural language.

Examples include:

* How many products do we have?
* What products are currently in stock?
* Show me information about our customers.
* What are the recent orders?
* Which suppliers are available?
* Provide insights based on business data.

The system processes user questions through an AI pipeline that integrates:

* 🧠 Large Language Models
* 📚 Retrieval-Augmented Generation (RAG)
* 🗄️ Business databases
* 🔎 Vector search
* 🌐 REST APIs

---

# 🚀 Features

### 🤖 AI-Powered Business Assistant

Ask business-related questions using natural language.

The assistant processes questions through an LLM and RAG pipeline to generate intelligent responses.

### 📚 Retrieval-Augmented Generation (RAG)

The project uses **ChromaDB** as a vector database to store and retrieve relevant business information.

This helps the AI provide context-aware answers.

### 🧠 Local LLM Integration

The application integrates with **Ollama** to run a local Large Language Model.

Current implementation uses:

```text
Llama 3.2
```

### 🗄️ Business Database

The backend manages multiple business entities, including:

* Customers
* Products
* Categories
* Suppliers
* Orders
* Order Items
* Payments
* Employees
* Purchase Orders
* Purchase Items
* Inventory Transactions
* Users
* Roles
* Audit Logs

### 🌐 FastAPI Backend

The project provides REST API endpoints for accessing business data and interacting with the AI assistant.

Example endpoint:

```text
POST /ask-ai
```

### 💬 Terminal Chat Interface

A terminal-based chatbot allows users to interact directly with the AI Business Assistant.

The system performs startup checks for:

* Ollama connection
* LLM availability
* ChromaDB connection
* Indexed documents
* AI business intelligence pipeline

---

# 🏗️ Project Architecture

```text
AI-Business-Assistant-ChatBot
│
├── backend/
│   ├── API
│   ├── Database Models
│   ├── AI Service
│   └── Business Logic
│
├── database/
│   ├── Database Configuration
│   └── Business Data
│
├── frontend/
│   └── User Interface
│
├── llm/
│   └── LLM Integration
│
├── rag/
│   ├── Vector Store
│   └── Retrieval Pipeline
│
├── tests/
│   └── Project Tests
│
├── chat.py
│
├── requirements.txt
│
└── README.md
```

---

# 🔄 System Workflow

```text
User Question
      │
      ▼
AI Business Assistant
      │
      ▼
RAG Context Retrieval
      │
      ▼
ChromaDB Vector Search
      │
      ▼
Business Database / Knowledge Context
      │
      ▼
LLM Processing
      │
      ▼
AI Generated Response
```

---

# 🛠️ Technologies Used

| Technology | Purpose                    |
| ---------- | -------------------------- |
| Python     | Core programming language  |
| FastAPI    | Backend REST API           |
| Streamlit  | Frontend interface         |
| SQLAlchemy | Database ORM               |
| PyMySQL    | MySQL database connection  |
| Ollama     | Local LLM integration      |
| Llama 3.2  | Large Language Model       |
| ChromaDB   | Vector database            |
| RAG        | Context-aware AI responses |
| Pandas     | Data processing            |
| Pydantic   | Data validation            |
| Faker      | Test data generation       |

---

# 📦 Installation

## 1. Clone the Repository

```bash
git clone https://github.com/Shadil-1/AI-Business-Assistant-ChatBot.git
```

Move into the project directory:

```bash
cd AI-Business-Assistant-ChatBot
```

---

## 2. Create a Virtual Environment

```bash
python -m venv venv
```

### Windows

```bash
venv\Scripts\activate
```

### Linux / macOS

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🧠 Ollama Setup

Install Ollama from the official website.

Then download the required model:

```bash
ollama pull llama3.2
```

Make sure Ollama is running before starting the application.

You can verify the installation with:

```bash
ollama list
```

---

# 🗄️ Database Setup

Configure your database connection using environment variables.

Create a `.env` file in the project directory:

```env
DB_HOST=localhost
DB_USER=your_username
DB_PASSWORD=your_password
DB_NAME=your_database
```

Update the configuration based on your database setup.

> ⚠️ Never upload your `.env` file containing passwords or API credentials to GitHub. Humanity has collectively learned this lesson approximately seventeen million times.

---

# 🚀 Running the Application

## Run the Terminal Chatbot

```bash
python chat.py
```

The application will check:

```text
✓ Ollama connected
✓ LLM model available
✓ ChromaDB connected
✓ Documents indexed
✓ AI Business Intelligence pipeline ready
```

You can then ask business questions directly.

Example:

```text
You: How many products do we have?
```

---

# 🌐 Running the FastAPI Server

Start the backend using:

```bash
uvicorn backend.main:app --reload
```

The API will run locally.

Example:

```text
http://127.0.0.1:8000
```

FastAPI automatically provides API documentation at:

```text
http://127.0.0.1:8000/docs
```

---

# 🤖 AI API

## Ask the AI Assistant

### Endpoint

```text
POST /ask-ai
```

### Request

```json
{
  "question": "How many products do we have?"
}
```

### Response

```json
{
  "question": "How many products do we have?",
  "answer": "The business currently has ..."
}
```

---

# 📡 Available API Endpoints

The backend provides endpoints for accessing business information.

```text
GET /customers
GET /products
GET /categories
GET /suppliers
GET /orders
GET /order-items
GET /payments
GET /employees
GET /purchase-orders
GET /purchase-items
GET /inventory-transactions
GET /roles
GET /users
GET /audit-logs
```

AI Assistant:

```text
POST /ask-ai
```

---

# 🧪 Example Questions

You can ask the assistant questions such as:

```text
How many products do we have?
```

```text
Show me all customers.
```

```text
What suppliers are available?
```

```text
Show recent orders.
```

```text
What is the current inventory status?
```

```text
Give me insights about the business data.
```

---

# 🔮 Future Improvements

Potential future improvements include:

* 📊 Advanced business analytics dashboard
* 📈 Data visualization
* 🔐 User authentication and authorization
* 💬 Improved conversational memory
* 🌐 Deployment to cloud platforms
* 📱 Improved responsive frontend
* 🔍 Advanced RAG retrieval
* 📊 Automated business reports
* 🧠 More advanced LLM models
* 🐳 Docker containerization

---

# 🤝 Contributing

Contributions, suggestions, and improvements are welcome.

To contribute:

1. Fork the repository.
2. Create a new branch.
3. Make your changes.
4. Commit the changes.
5. Open a Pull Request.

---

# 👨‍💻 Author

**Shadil K**

Aspiring Data Scientist and AI Developer interested in:

* Artificial Intelligence
* Machine Learning
* Large Language Models
* Retrieval-Augmented Generation
* Data Science
* Business Intelligence
* AI-Powered Applications

---

# ⭐ Support

If you find this project useful, consider giving the repository a ⭐.

It helps others discover the project and provides a small but scientifically measurable dopamine reward to the developer.

---

## 📄 License

This project is currently intended for educational and development purposes.

Consider adding an appropriate open-source license such as **MIT License** if you plan to make the project publicly reusable.
