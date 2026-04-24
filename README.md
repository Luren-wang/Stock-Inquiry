# Stock Inquiry

Flask stock query practice for Taiwan listed stocks.

## Features

- Homepage link to the stock query page.
- Uses the Taiwan Stock Exchange `STOCK_DAY` API.
- Allows users to enter a stock number.
- Shows the highest and lowest closing prices from the latest month returned by the API.
- Shows the open and closing prices for the most recent 10 trading days.
- Displays a warning message when the stock number is invalid or no data is returned.

## Run

```powershell
pip install -r requirements.txt
python app.py
```

Open `http://127.0.0.1:5000`.
