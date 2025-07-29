AI-Powered Stock Comparison Dashboard 📈
This project demonstrates how to build a powerful financial analysis agent using LlamaIndex and Google's Gemini model. The AI agent interprets natural language prompts to generate interactive, comparative dashboards for multiple stocks over custom time periods.

The core of this project is a single Python script that uses an agent to control a flexible data visualization tool. Instead of modifying code to change stocks or timeframes, you can simply change the prompt.

For speed and cost-efficiency, this script is configured to use Google's models/gemini-2.5-flash-lite. Its performance is excellent for the kind of structured, tool-using tasks the agent performs in this analysis.

FEATURES

Natural Language Control: Analyze multiple stocks and timeframes (e.g., "Show me a 6-month comparison of AMD and NVDA") without changing code.

Interactive Visualizations: Generates a single HTML file with linked subplots using Plotly.

Comparative Analysis: The dashboard displays comparative cumulative returns and side-by-side return distributions.

Linked Legend: A single, unified legend allows you to toggle the visibility of stocks across both charts simultaneously for easy comparison.


DEMO

Setup
Follow these steps to get the project running on your local machine.

1. Clone the Repository
Bash

git clone https://github.com/aitalksblog/AI_StockAnalysis.git
cd AI_StockAnalysis

2. Install Dependencies
This project requires a few Python libraries. You can install them all with pip:

Bash

pip install llama-index llama-index-llms-gemini yfinance pandas plotly python-dotenv

3. Set Up Your API Key
Create a file named .env in the root directory of the project and add your Google API key to it:

GOOGLE_API_KEY="your_google_api_key_here"


USAGE

To run the script, simply modify the prompt variable at the bottom of the file with your request and then execute the script from your terminal.

Python

 --- Prompt and Execution ---
 
prompt = "Show me a 3-month comparison of AMD and NVDA."

print(f"--- Running Final Agent ---")
response = agent.chat(prompt)

print("\n--- Agent Final Response ---")
print(response)

The script will generate an HTML file named final_dashboard.html in the same directory.

Example Prompts
You can try various prompts to test the agent's flexibility:

"Generate a comparative dashboard for TSLA, F, and GM over the last year."

"Show me a 30-day analysis of MSFT and AAPL."

"Create a dashboard comparing META and SNAP for the last 6 months."
