# Stock Inquiry

Flask stock query website for Taiwan listed stocks.

## Features

- Homepage link to the stock query page.
- Uses Python `requests` to call the Taiwan Stock Exchange `STOCK_DAY` API.
- Allows users to enter a stock number.
- Shows the highest and lowest closing prices from the latest month returned by the API.
- Shows the open and closing prices for the most recent 10 trading days.
- Displays a warning message when the stock number is invalid or no data is returned.

## Local Run

```powershell
pip install -r requirements.txt
python app.py
```

Open `http://127.0.0.1:5000`.

## Render Free Deployment

Create a Render Web Service from this GitHub repository.

```text
Runtime: Python
Instance Type: Free
Build Command: pip install -r requirements.txt
Start Command: gunicorn app:app --bind 0.0.0.0:$PORT
```

The included `render.yaml` uses the same free Python web service settings.
