# Stock Inquiry

Static stock query website for Taiwan listed stocks.
Flask stock query website for Taiwan listed stocks.

## Features

- Static website that can be deployed on Render Free.
- Uses the Taiwan Stock Exchange `STOCK_DAY` API in browser JavaScript.
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

1. Push `index.html`, `style.css`, `app.js`, and `render.yaml` to GitHub.
2. In Render, choose `New +` then `Static Site`.
3. Connect this GitHub repository.
4. Use these settings:
Create a Render Web Service from this GitHub repository.

```text
Build Command: leave empty
Publish Directory: .
Runtime: Python
Instance Type: Free
Build Command: pip install -r requirements.txt
Start Command: gunicorn app:app --bind 0.0.0.0:$PORT
```

The included `render.yaml` also describes the same static site settings.

## Local Preview

Open `index.html` in a browser.
The included `render.yaml` uses the same free Python web service settings.
