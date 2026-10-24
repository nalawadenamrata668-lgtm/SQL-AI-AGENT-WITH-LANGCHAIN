# 🤖 SQL Agent – AI Task Manager

An AI-powered task management application that allows users to create, view, update, and delete tasks using natural language. It integrates a Large Language Model (LLM) with SQL database tools to simplify task management through a conversational interface.

## 📌 Project Overview

The SQL Agent – AI Task Manager enables users to interact with a database using simple English instructions instead of writing SQL queries manually.

The AI agent interprets user requests, selects the appropriate database tools, performs the requested operations, and displays the results through a Streamlit chat interface.

## ✨ Key Features

- **Natural Language Interaction:** Manage tasks using everyday language.
- **CRUD Operations:** Create, read, update, and delete tasks.
- **Task Status Tracking:** Track tasks as Pending, In Progress, or Completed.
- **SQL Database Integration:** Store and retrieve task information using SQLite.
- **AI-Powered Agent:** Use an LLM and SQL tools to process task-related requests.
- **Query Guidelines:** Instruct the agent to limit SELECT results to 10 records and verify database changes after create, update, and delete operations.

## 🛠️ Tech Stack

- **Python:** Application logic
- **Streamlit:** Chat-based user interface
- **LangChain:** Agent creation and SQL database toolkit
- **LangGraph:** In-memory checkpointing
- **Groq:** Language model inference
- **GPT-OSS-20B:** Language model used by the application
- **SQLite:** Database for task storage
- **python-dotenv:** Environment variable management

## 🔄 How It Works

1. **User Input:** The user enters a request through the Streamlit chat interface.
2. **Request Interpretation:** The LLM interprets the user's instructions.
3. **Tool Selection:** The agent selects the appropriate SQL database tool.
4. **Database Operation:** The selected tool executes the requested operation on SQLite.
5. **Verification:** The agent is instructed to verify database changes after create, update, and delete operations.
6. **Response Generation:** The result is displayed in the chat interface.

## 💬 Example User Prompts

- Create a task to learn Python.
- Show all my tasks.
- Show my pending tasks.
- Mark task 1 as completed.
- Delete task 1.

## 🗄️ Database Design

**Table Name:** `tasks`

| Column | Description |
|---|---|
| `id` | Unique task identifier and primary key |
| `title` | Required task title |
| `description` | Optional task description |
| `status` | Task status: `pending`, `in_progress`, or `completed` |
| `created_at` | Timestamp of task creation |

The application creates the `tasks` table automatically if it does not already exist.

## 📁 Project Structure

```text
Gen-AI Series/
├── apps/
│   └── 5_SQL_AI_Agent_with_langchain.py
├── .env
├── .gitignore
└── README.md
