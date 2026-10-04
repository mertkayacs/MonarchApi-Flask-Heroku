# MonarchApi-Flask-Heroku

A small Flask API that returns the British monarch reigning in a given year, built from a CSV dataset of reigns and deployed to Heroku.

## How to run

The code lives in the `MonarchApi/` directory and was built for Heroku (`Procfile`: `web: gunicorn app:app`, Python 3.7.6 in `runtime.txt`). As written it no longer starts against a current pandas: the startup loop that maps years to monarchs raises a dtype error, so it needs the 2020-era stack (Python 3.7, pandas 1.x) to run.

Historical run steps:

```
cd MonarchApi
pip install -r requirements.txt
gunicorn app:app
```

Usage: `GET /?year=1700` returns the monarch reigning that year. A year outside the dataset returns `Invalid Input (757 - <current year>)`.

## Screenshots

None in the repository.

## Tech used

- Python 3.7
- Flask
- pandas
- gunicorn
- Heroku (Procfile, runtime.txt)

## Status

Coursework, 2020.
