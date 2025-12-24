# Personal Finance Chatbot

## Overview
The Personal Finance Chatbot is an intelligent assistant designed to provide guidance on saving, taxes, and investments. It leverages advanced AI techniques, including the LLaMA 2 model, to offer personalized financial advice and insights. The chatbot integrates with financial APIs and provides a user-friendly interface for managing personal finances.

## Features
- **Savings Guidance**: Get tips on how to save money effectively.
- **Tax Assistance**: Understand tax-saving strategies and compliance.
- **Investment Advice**: Explore investment opportunities tailored to your goals.
- **Dashboard**: Visualize your financial health with interactive charts and metrics.
- **Budgeting**: Track your expenses and compare them against predefined budgets.
- **Debt Management**: Strategize debt repayment using the Avalanche or Snowball methods.
- **Tax Estimation**: Simplified U.S. federal tax estimator for informational purposes.
- **AI Co-Pilot**: Chat with an AI assistant for personalized financial advice.

## How It Works
1. **User Interaction**: Users can ask questions or seek advice on financial topics.
2. **AI-Powered Responses**: The chatbot uses natural language processing to understand queries and provide relevant answers.
3. **Personalized Insights**: Recommendations are tailored based on user inputs.
4. **Data Visualization**: Interactive charts and graphs provide insights into financial data.
5. **Integration**: Connects with APIs like yfinance for real-time stock data.

## Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or VS Code for running `.ipynb` files
- Cloudflare Tunnel for public access
- Ollama for AI model hosting

## Installation
1. Clone the repository:
   ```bash
   git clone <repository-url>
   ```
2. Navigate to the project directory:
   ```bash
   cd personal_finance_chatbot
   ```
3. Open the `code.ipynb` file in Jupyter Notebook or VS Code.
4. Installations part of the code file
    - The required libraries directly from the notebook:
   ```python
   !pip install -q streamlit pandas plotly streamlit-option-menu yfinance openai
   ```
    - Install Ollama:
   ```bash
   curl -fsSL https://ollama.com/install.sh | sh
   ```
    - Pull the finance model:
   ```bash
   ollama pull jjansen/adapt-finance-llama2-7b
   ```

## Running the Application
1. Run all cells in the `code.ipynb` file to launch the application.
3. Create public tunnels for the services (optional):
   ```bash
   cloudflared tunnel --url http://127.0.0.1:8501
   cloudflared tunnel --url http://127.0.0.1:11434
   ```
4. Open the app in your browser at `http://localhost:8501`.

## Notes
- The chatbot requires the `ollama` server to be running in the background.
- Ensure the finance model is downloaded and available locally.
- Customize the app's appearance and functionality using the provided notebook code.