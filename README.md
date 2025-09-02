# 🚀 Crypto Trading Guide RAG System

An intelligent crypto trading advisor powered by **Retrieval-Augmented Generation (RAG)** that provides real-time market analysis, expert insights, and actionable trading recommendations using live data from multiple sources.

![Python](https://img.shields.io/badge/python-v3.8+-blue.svg)
![LangChain](https://img.shields.io/badge/LangChain-Latest-green.svg)

## ✨ Features

### 🔴 Real-Time Data Integration
- **Live Market Data**: CoinGecko API integration for current prices, market caps, volumes
- **Technical Analysis**: RSI calculations, moving averages, volatility metrics
- **Market Sentiment**: Automated sentiment analysis based on price movements

### 📰 News & Content Aggregation
- **RSS Feed Parsing**: Real-time news from CoinTelegraph, CoinDesk, CryptoNews, Decrypt
- **Expert Insights**: Analysis from top crypto traders and analysts
- **Content Cleaning**: HTML stripping and text preprocessing for better RAG performance

### 📊 Historical Analysis
- **Price History**: yfinance integration for historical data analysis
- **Backtesting Metrics**: Sharpe ratio, maximum drawdown, performance analytics
- **Technical Indicators**: 20/50-day SMAs, RSI, volatility calculations

### 🤖 Advanced RAG System
- **Vector Search**: FAISS-powered semantic search across all data sources
- **Context-Aware Responses**: LLM generates advice based on retrieved relevant information
- **Source Citations**: Full transparency with document sources and references

## 🛠️ Technology Stack

- **LLM**: Google Gemini 1.5 Flash via LangChain
- **Vector Database**: FAISS (Facebook AI Similarity Search)
- **Data Sources**: CoinGecko API, RSS Feeds, yfinance
- **Framework**: LangChain for RAG pipeline
- **Language**: Python 3.8+

## 📋 Prerequisites

- Python 3.8 or higher
- Google AI Studio API Key ([Get it here](https://aistudio.google.com/app/apikey))
- Stable internet connection for real-time data

## 🚀 Quick Start

### 1. Clone the Repository
```bash
git clone https://github.com/yourusername/crypto-trading-advisor-using-RAG.git
cd crypto-trading-rag
```

### 2. Create Virtual Environment
```bash
python -m venv crypto_rag_env
source crypto_rag_env/bin/activate  # On Windows: crypto_rag_env\Scripts\activate
```

### 3. Install Dependencies
```bash
pip install -r requirements.txt
```

### 4. Setup Environment Variables
Create a `.env` file in the project root:
```env
GOOGLE_API_KEY=your_google_ai_studio_api_key_here
```

### 5. Run the System
```bash
python app.py
```

## 💡 Usage Examples

### Interactive Chat Interface
```
Your Question: What's the current market sentiment for Bitcoin?
```

### Special Commands
- `update` - Refresh all data sources with latest information
- `summary` - Generate comprehensive market overview
- `quit` - Exit the system

### Example Questions
- "Should I buy Ethereum now or wait for a dip?"
- "What are the key technical indicators I should watch?"
- "Explain dollar-cost averaging strategy for crypto"
- "How should I manage risk in crypto trading?"

## 🏗️ System Architecture

```
┌─────────────────┐    ┌──────────────────┐    ┌─────────────────┐
│   Data Sources  │    │   RAG Pipeline   │    │   User Interface│
│                 │    │                  │    │                 │
│ • CoinGecko API │───▶│ • Document Loader│───▶│ • Chat Interface│
│ • RSS Feeds     │    │ • Text Splitter  │    │ • Command System│
│ • yfinance      │    │ • Vector Store   │    │ • Source Citations│
│ • Expert Content│    │ • LLM Integration│    │                 │
└─────────────────┘    └──────────────────┘    └─────────────────┘
```

## 📊 Data Sources

| Source | Type | Update Frequency | Purpose |
|--------|------|-----------------|---------|
| CoinGecko | Market Data | Real-time | Prices, market caps, technical metrics |
| RSS Feeds | News | Real-time | Market news and sentiment |
| yfinance | Historical | Daily | Backtesting and trend analysis |
| Expert Analysis | Insights | Manual | Professional trading perspectives |

## ⚙️ Configuration

### Supported Cryptocurrencies
Default symbols: `["bitcoin", "ethereum", "cardano"]`

Modify in the code:
```python
market_docs = self.fetch_market_data(["bitcoin", "ethereum", "solana", "cardano"])
```

### News Sources
- CoinTelegraph RSS
- CoinDesk RSS  
- CryptoNews RSS
- Decrypt RSS

### Technical Indicators
- RSI (Relative Strength Index)
- Simple Moving Averages (20-day, 50-day)
- Volatility metrics
- Market sentiment analysis

## 🔧 Advanced Features

### Portfolio Analysis
```python
portfolio = {"BTC": 0.5, "ETH": 2.0, "ADA": 1000}
analysis = crypto_guide.get_portfolio_analysis(portfolio)
```

### Custom Market Summary
```python
summary = crypto_guide.get_market_summary()
```

### Data Updates
```python
crypto_guide.update_all_data()  # Refresh all real-time sources
```

## 🚨 Error Handling

The system uses **fail-fast** approach with no fallback data:
- API failures will raise exceptions immediately
- Clear error messages for troubleshooting
- Connection status indicators

## 🔒 Security & API Keys

- Store API keys in `.env` file (never commit to git)
- Use environment variables for sensitive data
- Rate limiting implemented for all API calls

## 📈 Performance

- **Vector Search**: Sub-second semantic search across documents
- **API Rate Limits**: Automatic rate limiting to respect API constraints
- **Memory Management**: Efficient document chunking and storage
- **Real-time Updates**: Fresh data without system restart

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

### Development Setup
```bash
pip install -e .  # Editable install for development
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## ⚠️ Disclaimer

This system is for educational and informational purposes only. **Cryptocurrency trading involves substantial risk of loss. Past performance is not indicative of future results. Always do your own research and never invest more than you can afford to lose.**

## 🔗 Links

- [Google AI Studio](https://aistudio.google.com/app/apikey) - Get your API key
- [CoinGecko API](https://www.coingecko.com/en/api) - Market data source
- [LangChain Documentation](https://docs.langchain.com/) - RAG framework
- [FAISS Documentation](https://faiss.ai/) - Vector search

---

**Built with ❤️ by arsalmairaj2k**

*Star ⭐ this repository if you find it helpful!*
