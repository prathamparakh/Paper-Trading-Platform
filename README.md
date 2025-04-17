# Stock Portfolio Manager

A C++ application with Python integration that allows users to manage their stock portfolios, track stock information, and execute buy/sell transactions.

## Features

- **Real-time Stock Information**: Fetches current stock data from Google Finance
- **User Authentication**: Secure login system
- **Portfolio Management**: Buy and sell stocks with tracking of your investments
- **Fund Balance**: Automatic tracking of available funds
- **Stock Validation**: Verification of stock symbols
- **Transaction History**: Record of all buy/sell transactions

## Prerequisites

- C++ compiler (C++11 or later)
- Python 3.x
- Python packages:
  - requests
  - beautifulsoup4

## Files Structure

- **main.cpp**: Main C++ application code
- **stockdb.py**: Python script for fetching stock data
- **stock_symbols.txt**: List of stock symbols to track
- **user_db.txt**: User credentials database
- **portfolio.csv**: User's portfolio data
- **stock_info.csv**: Cached stock information

## Installation

1. Clone the repository
```bash
git clone https://github.com/yourusername/stock_portfolio.git
cd stock_portfolio
```

2. Install required Python packages
```bash
pip install requests beautifulsoup4
```

3. Compile the C++ program
```bash
g++ -o stock_portfolio main.cpp
```

## Usage

1. Run the compiled program
```bash
./stock_portfolio
```

2. Log in with your credentials
   - Default credentials: username: `jack`, password: `1234`

3. Use the menu options to:
   - Update stock information
   - View stock details
   - Check your portfolio
   - Buy stocks
   - Sell stocks

## Adding New Stocks

To add new stocks to track, simply edit the `stock_symbols.txt` file and add the stock symbols (one per line).

## User Management

The `user_db.txt` file stores user credentials in a simple format:
```
username password
```

## Implementation Details

### C++ Classes
- **Stock**: Base class for stock information management
- **Portfolio**: Inherits from Stock, manages the user's portfolio
- **User**: Inherits from Portfolio, handles user authentication and menu interactions

### Python Integration
The C++ application calls the Python script `stockdb.py` to fetch real-time stock data from Google Finance using web scraping techniques.

## Security Considerations

- The current implementation stores passwords in plaintext. In a production environment, use proper encryption.
- Input validation could be improved for robustness.
- Error handling could be enhanced for better user experience.

## Future Improvements

- Enhanced security with password hashing
- Historical price tracking and visualization
- Transaction history log
- More sophisticated portfolio analysis
- Support for multiple users with separate portfolios
- Graphical user interface

## License

[MIT License](LICENSE)

## Acknowledgments

- Google Finance for stock data
- BeautifulSoup4 for web scraping capabilities
