# AI Equity Trader - Model Context Protocol (MCP)

## 🧠 Overview

This project implements an **AI-powered equity trading system** using **Anthropic's Model Context Protocol (MCP)**. It demonstrates how autonomous AI agents can interact with financial markets, analyze data, execute trades, and manage portfolios by integrating with real-time market data and external tools through the MCP framework.

---

## 🚀 Key Features

- **🤖 AI-Powered Trading Agents**: Autonomous agents capable of analyzing market data and executing trades.
- **🔌 MCP Integration**: Connects AI models to external systems (market data, portfolios) through Anthropic’s Model Context Protocol.
- **💼 Portfolio Management**: Tracks holdings, balances, and profit/loss per trader.
- **📈 Real-Time Market Data**: Pulls real-time or simulated stock prices via Polygon.io or in-built simulator.
- **🌐 Gradio User Interface**: Web-based UI for monitoring trader performance, portfolios, and transactions.
- **🧱 Modular Architecture**: Well-structured codebase for scalability and maintainability.

---

## 📁 Project Structure

```
AI-Equity-Trader-MCP/
├── accounts.py             # Manages trading accounts and transactions.
├── accounts_client.py      # Client-side logic for account services.
├── accounts_server.py      # Backend server for accounts.
├── app.py                  # Gradio UI entry point.
├── database.py             # Data persistence for market data and accounts.
├── market.py               # Simulates or fetches real-time stock data.
├── market_server.py        # Server for serving market data to agents.
├── mcp_params.py           # MCP configuration and constants.
├── push_server.py          # Pushes data updates to connected clients.
├── requirements.txt        # Python dependencies list.
├── reset.py                # Script to reset simulation/account state.
├── templates.py            # Prompts/templates used by AI agents.
├── tracers.py              # Logging & debugging tools.
├── traders.py              # AI trading agents using MCP.
├── trading_floor.py        # Manages multiple agent execution.
└── util.py                 # Utility functions (e.g. UI colors).
```

---

## 🛠 Getting Started

### ✅ Prerequisites

- Python 3.8+
- `pip` (Python package installer)

### 📦 Installation

1. **Clone the repository:**
    ```bash
    git clone https://github.com/SiddhantSharma64/AI-Equity-Trader-MCP.git
    cd AI-Equity-Trader-MCP
    ```

2. **Create a virtual environment:**
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4. **Configure API keys (Optional):**  
   Create a `.env` file in the root with your API credentials:
    ```env
    POLYGON_API_KEY=YOUR_POLYGON_API_KEY
    POLYGON_PLAN=paid  # or 'free'

    DEEPSEEK_API_KEY=YOUR_DEEPSEEK_API_KEY
    GOOGLE_API_KEY=YOUR_GOOGLE_API_KEY
    GROK_API_KEY=YOUR_GROK_API_KEY
    OPENROUTER_API_KEY=YOUR_OPENROUTER_API_KEY
    ```

---

## ▶️ Running the Application

### 1. **Start Trading Agents**
Launch the agents that monitor market data and perform trades:

```bash
python trading_floor.py
```

### 2. **Start the Gradio UI**
Launch the user interface for monitoring performance:

```bash
python app.py
```

Visit `http://127.0.0.1:7860` in your browser.

---

## ⚙️ How It Works

Multiple AI agents simulate a trading environment, each with its own account and strategy. Agents fetch market data, analyze trends, and place trades using prompts defined in `templates.py`.

The **Model Context Protocol (MCP)** allows AI models (GPT, Gemini, Grok, etc.) to interact with external services like market data APIs and account servers in a standardized, modular way.

The `Gradio` UI visualizes:

- Account balances and portfolio value
- Live transactions and trading logs
- Holdings per trader

---

## 🧰 Technologies Used

- **Python** – Core backend logic
- **Gradio** – Web-based dashboard
- **MCP (Anthropic)** – AI ↔ system communication protocol
- **OpenAI Agents** – For autonomous trading logic
- **Polygon.io API** – Real-time market data
- **Plotly Express** – Interactive charts in UI
- **Pydantic** – Settings & data validation
- **SQLite** – Lightweight data storage

---

