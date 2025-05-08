# 📱 Stock Price Alert & News SMS via Twilio

This project sends you stock price updates and related news alerts when the stock price rises or falls significantly. Powered by the **Alpha Vantage API**, **News API**, and **Twilio**, it delivers real-time stock updates and top news headlines straight to your phone via SMS.

---

## 🚀 Features

- Fetches **stock price data** using the [Alpha Vantage API](https://www.alphavantage.co/).
- Retrieves **top 3 latest news headlines** about the associated company using the [NewsAPI](https://newsapi.org/).
- Sends **SMS alerts** with stock updates and news using the [Twilio API](https://www.twilio.com/).
- Simple Python integration with error handling and real-time notifications.

---

## 🛠️ Technologies Used
- **Python 3.12**
- **Twilio Python SDK**
- **Requests** for HTTP requests
- APIs:
  - [Alpha Vantage API](https://www.alphavantage.co/) for stock data
  - [News API](https://newsapi.org/) for fetching news
  - [Twilio API](https://www.twilio.com/) for SMS notifications

---

## 📝 How It Works
1. Retrieves the stock price difference for the last two days.
2. Calculates the percentage change in price.
3. If the price difference exceeds the threshold (e.g., 5%), it fetches the latest 3 news articles about the company.
4. Formats the data into an SMS message.
5. Sends the SMS to a verified phone number using **Twilio**.

---

## 📦 Setup Instructions

### Prerequisites:
1. Sign up for the following services and get your API keys:
   - [Alpha Vantage Account](https://www.alphavantage.co/)
   - [NewsAPI Account](https://newsapi.org/)
   - [Twilio Account](https://www.twilio.com/console)
2. Python 3.x installed on your system.

### 1️⃣ Install the Required Libraries
```bash
pip install requests twilio
```

### 2️⃣ Clone the Repository
```bash
git clone https://github.com/<your-username>/stock-price-news-alert.git
cd stock-price-news-alert
```

### 3️⃣ Setup Your Environment Variables
Store your sensitive data (API Keys and Phone Numbers) as environment variables. Add these to a `.env` file or your terminal:
```bash
export STOCK_API_KEY="your_alpha_vantage_api_key"
export NEWS_API_KEY="your_news_api_key"
export TWILIO_SID="your_twilio_sid"
export TWILIO_AUTH_TOKEN="your_twilio_auth_token"
export VIRTUAL_TWILIO_NUMBER="your_twilio_phone_number"
export VERIFIED_NUMBER="your_verified_phone_number"
```

**OR** replace the placeholders directly in the test script for quick local testing:
```python
STOCK_API_KEY = "your_alpha_vantage_api_key"
NEWS_API_KEY = "your_news_api_key"
TWILIO_SID = "your_twilio_sid"
TWILIO_AUTH_TOKEN = "your_twilio_auth_token"
VIRTUAL_TWILIO_NUMBER = "+123456789"
VERIFIED_NUMBER = "+9876543210"
```

### 4️⃣ Run the Script
```bash
python3 test.py
```

---

## ⚙️ Example Output

- **Console Output**:
```plaintext
Stock Price Change: +5%
Fetching news articles...
Message sent successfully. SID: SMXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX
```

- **SMS Received**:
