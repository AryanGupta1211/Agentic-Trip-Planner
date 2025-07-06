# 🌍 AI Travel Planner: Your Intelligent Trip Architect

[![Python Version](https://img.shields.io/badge/Python-3.12%2B-blue.svg)](https://www.python.org/downloads/)
[![Streamlit](https://img.shields.io/badge/Frontend-Streamlit-ff69b4.svg)](https://streamlit.io)
[![FastAPI](https://img.shields.io/badge/Backend-FastAPI-009688.svg)](https://fastapi.tiangolo.com/)
[![Code Style: Black](https://img.shields.io/badge/code%20style-black-000000.svg)](https://github.com/psf/black)
[![Powered by: LangChain](https://img.shields.io/badge/Powered%20by-LangChain-blue.svg)](https://www.langchain.com/)

**AI Travel Planner** is a state-of-the-art application designed to craft personalized, real-time, and comprehensive travel itineraries. This isn't just another travel app; it's an intelligent agent that acts as your personal trip architect, leveraging cutting-edge AI and real-time data to plan every detail of your journey.

From a simple prompt, the application generates a complete, day-by-day travel plan, including real-time hotel prices, weather forecasts, currency exchange rates, and a detailed expense breakdown. Built with a modular architecture and powered by a sophisticated agentic workflow, this project represents a significant leap in automated, intelligent travel planning.

---

## ✨ Core Features

- **Interactive Frontend:** A beautiful and intuitive user interface built with **Streamlit** that makes trip planning a breeze.
- **High-Performance Backend:** A robust and scalable backend powered by **FastAPI**, ensuring swift communication and data processing.
- **Dual LLM Power:**
    - **Groq:** Utilized for its incredible speed, providing near-instant responses for quick planning stages.
    - **ChatGPT (GPT-4):** Employed for its powerful reasoning and generation capabilities, ensuring high-quality, nuanced travel plans.
- **Real-Time Data Integration:** The agent is equipped with a suite of live tools:
    - **🌦️ Real-Time Weather:** Get current weather forecasts for your destination.
    - **🏨 Real-Time Hotel Prices:** Find up-to-date hotel pricing and availability.
    - **💵 Live Currency Exchange:** Access the latest currency conversion rates.
    - **📍 Real-Time Place Information:** Discover attractions, restaurants, and points of interest.
- **Comprehensive Financial Planning:**
    - **💰 Full Trip Expense Report:** Get a detailed estimate of the total trip cost.
    - **📅 Day-wise Expense Breakdown:** Understand your expected spending for each day of your trip.
- **Sophisticated Agentic Workflow:** At its core, the system uses **LangChain** and **LangGraph** to create a multi-agent system that can reason, delegate tasks, and use tools to build the perfect itinerary.
- **Modern Development Environment:**
    - **UV:** Uses the lightning-fast `uv` package manager for dependency management.
    - **Modular Codebase:** A clean, organized, and scalable project structure that promotes maintainability and collaboration.

---

## 🏛️ Architecture Overview

The application operates on a decoupled frontend-backend architecture. The Streamlit UI captures user input and communicates with the FastAPI backend, which orchestrates the AI agent workflow.

```
+----------------------+      +------------------------+
|   Streamlit Frontend |      |    FastAPI Backend     |
| (User Interface)     |      | (API & Agent Logic)    |
+----------------------+      +------------------------+
        |                             |
        | (HTTP Requests)             | (Orchestration)
        |                             |
        v                             v
+---------------------------------------------------------+
|                     LangGraph Agentic Workflow          |
|                                                         |
|+-----------------+  +-----------------+  +-----------+  |
|| Planning Agent  |  |Tool-Using Agent |  |  LLMs     |  |
|+-----------------+  +-----------------+  +-----------+  |
|         |                    |                 ^ |      |
|         | (Delegates)        | (Executes)      | v      |
|         |                    v                 | |      |
|         |      +----------------------------+  | |      |
|         +------>   Real-Time Tools          |  | |      |
|                | - Weather API              |--+ |      |
|                | - Hotel Pricing API        |----+      |
|                | - Currency Exchange API    |--+ |      |
|                | - Places API               |----+      |
|                +----------------------------+           |
+---------------------------------------------------------+
```

---

## 🛠️ Tech Stack

- **Frontend:** Streamlit
- **Backend:** FastAPI
- **AI Orchestration:** LangChain, LangGraph
- **LLMs:** Groq, OpenAI (ChatGPT)
- **Package Management:** UV
- **Core Language:** Python
- **Environment Management:** python-dotenv

---

## 📂 Project Structure

The project follows a clean, modular structure to separate concerns and enhance scalability.

## 🚀 Getting Started

### Prerequisites

- Python 3.12+
- `uv` installed (`pip install uv`)
- API keys for:
    - Groq
    - OpenAI
    - Any other real-time data providers you integrate

### Installation & Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/AryanGupta1211/Agentic-Trip-Planner
    cd Agentic-Trip-Planner
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    uv venv
    source .venv/bin/activate  # On Windows use `.venv\Scripts\activate`
    ```

3.  **Install dependencies using uv:**
    ```bash
    uv pip install -r requirements.txt
    ```

4.  **Configure your environment:**
    Create a `.env` file in the root directory:
    ```bash
     .env
    ```
    Now, edit the `.env` file and add your API keys:
    ```
    GROQ_API_KEY=
    GOOGLE_API_KEY=
    GPLACES_API_KEY=
    FOURSQUARE_API_KEY=
    TAVIALY_API_KEY=
    OPENWEATHERMAP_API_KEY=
    EXANGE_RATE_API_KEY=
    LANGCHAIN_API_KEY=
    ALPHAVANTAGE_API_KEY=
    ```

### Usage

1.  **Run the application:**
    The application is launched through the main Streamlit entry point.
    ```bash
    streamlit run streamlit_app.py
    ```

1.  **Run the application:**
    Also start the FastAPI backend in the background.
    ```bash
    uvicorn main:app --reload --port 8000
    ```


3.  **Open your browser:**
    Navigate to `http://localhost:8501` to start planning your trip!

---

## 🤝 Contributing

This project was a significant learning journey, and I welcome collaboration to make it even better. Contributions, issues, and feature requests are welcome!

1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 🙏 Acknowledgments

A huge thank you to the teams and communities behind these incredible open-source projects that made this application possible:
- [Streamlit](https://streamlit.io/)
- [FastAPI](https://fastapi.tiangolo.com/)
- [LangChain](https://www.langchain.com/)
- [Groq](https://console.groq.com/)
- [OpenAI](https://openai.com/)

