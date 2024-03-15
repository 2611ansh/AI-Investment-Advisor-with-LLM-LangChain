# InvestAI

## Project Overview

This project is an AI-powered Investment Advisor that provides investment recommendations based on a company's current financial performance and market trends. The advisor utilizes Large Language Models (LLMs) and the LangChain library to analyze financial data, news articles, and other relevant information to generate detailed investment theses.

## Features

- **News Analysis**: The advisor retrieves and analyzes recent news articles related to the company, providing insights into current financial events.
- **Financial Statement Analysis**: The advisor fetches and analyzes the company's balance sheet, cash flow statement, and income statement for a specific time period.
- **Stock Price Analysis**: The advisor downloads and examines the company's stock price data over the past five years.
- **Investment Thesis Generation**: Based on the analysis, the advisor generates a detailed investment thesis, including insights from news, balance sheet analysis, cash flow analysis, income statement analysis, and a summary with recommendations.

## Project Structure

```
├── model.py
├── server.py
├── worker.py
├── templates
│   └── index.html
└── README.md
```

- `model.py`: Contains the LLM model configuration (not included in the provided files).
- `server.py`: Flask server file that handles the web application routes and communication with the worker module.
- `worker.py`: Contains the core logic for processing user prompts, fetching financial data, and generating investment theses using LangChain agents and tools.
- `templates/index.html`: The HTML template for the web application's user interface (not included in the provided files).
- `README.md`: This file, providing an overview and instructions for the project.

## Requirements

- Python 3.x
- Flask
- LangChain
- yfinance
- Google Serper API Key (for news search)

## Setup and Usage

1. Clone the repository: `git clone https://github.com/yourusername/AI-Investment-Advisor-with-LLM-LangChain.git`
2. Install the required dependencies: `pip install -r requirements.txt`
3. Set up the Google Serper API Key in `worker.py`:
   ```python
   os.environ["SERPER_API_KEY"] = "YOUR_SERPER_API_KEY"
   ```
4. Run the Flask server: `python server.py`
5. Access the web application at `http://localhost:8000`
6. Enter a company's ticker symbol (e.g., AAPL for Apple Inc.) in the input field.
7. The AI Investment Advisor will generate and display a detailed investment thesis based on the company's financial data and market trends.

Note: This project is for educational and research purposes only. It should not be considered as professional financial advice. Always conduct your own research and due diligence before making any investment decisions.

## Contributing

Contributions are welcome! If you find any issues or have suggestions for improvements, please open an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
