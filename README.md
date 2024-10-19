# Stock Portfolio Management System - Database Final Project

This project implements a stock portfolio management system where users can track stock prices, manage their investment portfolios, and receive notifications about stock performance through a Line Bot interface. The system supports user registration, login, and interaction via a web-based front-end and a Python-Flask back-end integrated with a PostgreSQL database. 

## Team Members:
- **111550098** 楊宗儒
- **111550076** 楊子賝
- **111550124** 陳燁燁
- **111550007** 白冠宸
- **111550127** 郭穎達

## Features:
1. **Portfolio Management**:
   - Create, view, update, and delete stock portfolios.
   - View portfolio details and receive performance updates.
   
2. **Stock Subscription and Notifications**:
   - Subscribe to individual stocks and get notified of significant price changes through Line Bot.
   - Receive real-time notifications based on customizable price thresholds.
   
3. **Stock Data Management**:
   - Fetch stock data using Yahoo Finance API and automatically update the database with current stock prices.
   - Display historical and live stock prices.

4. **Data Visualization**:
   - Charts generated using Chart.js to visualize portfolio value changes over time.
   - View graphs of portfolio performance via a web interface.

5. **User Interface**:
   - Front-end developed using HTML, CSS, and JavaScript.
   - Users can register and log in to manage their investments via a clean web interface.
   - Integrated Line Bot for additional interaction and notifications.

## System Architecture:
### 1. Back-end (Flask API):
- **`app.py`**: Main Flask server that handles routes for user login, portfolio management, and subscription features. It also integrates with the Line Bot API for sending notifications to users.
  
### 2. Database:
- **PostgreSQL** database is used to store stock, user, and portfolio data. 
- **Schema** includes tables such as:
  - `Ticker`: Stores stock tickers.
  - `Price`: Historical price data for each stock.
  - `Portfolio`: User-defined investment portfolios.
  - `Subscribe`: Tracks stock subscriptions for notifications.
  
### 3. Data Management Scripts:
- **`upload_ticker.py`**: Uploads stock tickers to the database.
- **`upload_history.py`**: Fetches historical stock data and populates the database.
- **`live_price.py`**: Updates live stock prices using the Yahoo Finance API and stores them in the database.
- **`notification_stock.py`**: Sends notifications to users about significant price changes in their subscribed stocks based on thresholds.

### 4. Front-end:
- **HTML Files**:
  - `login.html`: Allows users to log in.
  - `main.html`: Displays subscribed stocks and portfolio information.
  - `show.html`: Shows portfolio value graphs using Chart.js.
  - `test.html`: Contains test features for stock price calculation and submission.

## How the Data is Updated:
The stock prices are updated in real-time using the Yahoo Finance API. A Python script runs every 5 minutes, fetching the latest stock prices and updating the PostgreSQL database with the new values. 

- **Automatic Update**: The `live_price.py` script runs periodically to fetch the latest stock prices for all subscribed stocks and stores this data in the database. This ensures that users always have up-to-date stock prices.

## Demo Video:
Watch the demo video here: [Youtube Demo](https://www.youtube.com/watch?v=sWgeiSi0Nz8)

## report link
[report link](https://github.com/David810209/database-FinalProject/blob/main/Database_Final_Project.pdf)