<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/brand/svg/monarch-api-logo-on-dark.svg">
    <img src="docs/brand/svg/monarch-api-logo-on-light.svg" alt="Monarch API" width="260">
  </picture>
</p>

<h1 align="center">Which monarch ruled in a given year? Ask the API.</h1>

<p align="center">
  Coursework from 2020: a one-route Flask API over a dataset of British monarchs.<br>
  <b>Years from 757 to today. Plain-text answers.</b>
</p>

<p align="center">
  <img alt="Flask" src="https://img.shields.io/badge/Flask-3BABC3?style=flat-square&logo=flask&logoColor=white">
  <img alt="pandas" src="https://img.shields.io/badge/pandas-150458?style=flat-square&logo=pandas&logoColor=white">
  <img alt="Python 3.7.6 pinned in runtime.txt" src="https://img.shields.io/badge/Python-3.7.6%20pinned-9C7A3C?style=flat-square">
  <img alt="66 dataset rows" src="https://img.shields.io/badge/dataset-66%20rows-2F6B4F?style=flat-square">
  <img alt="Coursework, 2020" src="https://img.shields.io/badge/project-coursework%202020-9C7A3C?style=flat-square">
  <a href="https://github.com/mertkayacs/MonarchApi-Flask-Heroku"><img alt="GitHub stars" src="https://img.shields.io/github/stars/mertkayacs/MonarchApi-Flask-Heroku?style=flat-square&logo=github&color=8A6D3B"></a>
</p>

<p align="center">
  <a href="#quick-start"><img alt="Quick start" src="https://img.shields.io/badge/Quick%20start-9C7A3C?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij48ZyBmaWxsPSJub25lIiBzdHJva2U9IiNmZmZmZmYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIyIj48cGF0aCBkPSJNMTIgMTV2NXMzLjAzLS41NSA0LTJjMS4wOC0xLjYyIDAtNSAwLTUiLz48cGF0aCBkPSJNNC41IDE2LjVjLTEuNSAxLjI2LTIgNS0yIDVzMy43NC0uNSA1LTJjLjcxLS44NC43LTIuMTMtLjA5LTIuOTFhMi4xOCAyLjE4IDAgMCAwLTIuOTEtLjA5Ii8%2BPHBhdGggZD0iTTkgMTJhMjIgMjIgMCAwIDEgMi0zLjk1QTEyLjg4IDEyLjg4IDAgMCAxIDIyIDJjMCAyLjcyLS43OCA3LjUtNiAxMWEyMi40IDIyLjQgMCAwIDEtNCAyeiIvPjxwYXRoIGQ9Ik05IDEySDRzLjU1LTMuMDMgMi00YzEuNjItMS4wOCA1IC4wNSA1IC4wNSIvPjwvZz48L3N2Zz4%3D&logoColor=white"></a>
  <a href="MonarchApi/data.csv"><img alt="Dataset" src="https://img.shields.io/badge/Dataset-1E2A38?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij48ZyBmaWxsPSJub25lIiBzdHJva2U9IiNmZmZmZmYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIyIj48ZWxsaXBzZSBjeD0iMTIiIGN5PSI1IiByeD0iOSIgcnk9IjMiLz48cGF0aCBkPSJNMyA1VjE5QTkgMyAwIDAgMCAyMSAxOVY1Ii8%2BPHBhdGggZD0iTTMgMTJBOSAzIDAgMCAwIDIxIDEyIi8%2BPC9nPjwvc3ZnPg%3D%3D&logoColor=white"></a>
  <a href="MonarchApi/app.py"><img alt="App" src="https://img.shields.io/badge/App-1E2A38?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCIgd2lkdGg9IjI0IiBoZWlnaHQ9IjI0Ij48ZyBmaWxsPSJub25lIiBzdHJva2U9IiNmZmZmZmYiIHN0cm9rZS1saW5lY2FwPSJyb3VuZCIgc3Ryb2tlLWxpbmVqb2luPSJyb3VuZCIgc3Ryb2tlLXdpZHRoPSIyIj48cGF0aCBkPSJNNiAyMmEyIDIgMCAwIDEtMi0yVjRhMiAyIDAgMCAxIDItMmg4YTIuNCAyLjQgMCAwIDEgMS43MDQuNzA2bDMuNTg4IDMuNTg4QTIuNCAyLjQgMCAwIDEgMjAgOHYxMmEyIDIgMCAwIDEtMiAyeiIvPjxwYXRoIGQ9Ik0xNCAydjVhMSAxIDAgMCAwIDEgMWg1Ii8%2BPHBhdGggZD0iTTEwIDEyLjUgOCAxNWwyIDIuNSIvPjxwYXRoIGQ9Im0xNCAxMi41IDIgMi41LTIgMi41Ii8%2BPC9nPjwvc3ZnPg%3D%3D&logoColor=white"></a>
</p>

<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="docs/assets/readme/hero-dark.webp">
    <img src="docs/assets/readme/hero-light.webp" alt="Terminal with three curl requests to the Monarch API: 1066 returns William I, 1588 returns Elizabeth I and 500 returns an invalid input message" width="960">
  </picture>
</p>

Monarch API returns the British monarch who reigned in a given year. It is a Flask app that loads a CSV of reigns into a pandas Series indexed by year, and it was built as coursework in 2020 for deployment on Heroku. One route answers a year query with the monarch name as plain text.

---

## Why Monarch API

The whole service is one route over one CSV file.

|  |  |
|---|---|
| <img src="docs/assets/readme/icons/landmark.svg" width="18" height="18" alt=""> **A year in, a monarch out** | A request to `/?year=1700` returns the monarch reigning that year. |
| <img src="docs/assets/readme/icons/database.svg" width="18" height="18" alt=""> **Dataset included** | [data.csv](MonarchApi/data.csv) holds 66 rows of start year, end year and name, from Offa in 757 to Charles III from 2022. |
| <img src="docs/assets/readme/icons/circle-check.svg" width="18" height="18" alt=""> **Clear out-of-range answer** | A year outside the data returns `Invalid Input (757 - <current year>)`. |

## A quick tour

<table>
  <tr>
    <td width="50%" valign="top">
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="docs/assets/readme/tour/run-dark.webp">
        <img src="docs/assets/readme/tour/run-light.webp" alt="Terminal output of three curl requests to the Monarch API">
      </picture>
      <h3>API in action</h3>
      Three requests: 1066 returns William I, 1588 returns Elizabeth I, and 500 is out of range.
    </td>
    <td width="50%" valign="top">
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="docs/assets/readme/tour/query-dark.webp">
        <img src="docs/assets/readme/tour/query-light.webp" alt="Code card of the Flask app that builds the year series and answers requests">
      </picture>
      <h3>The query code</h3>
      A year-indexed pandas Series is built once at start-up and each request looks up its year.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="docs/assets/readme/tour/data-dark.webp">
        <img src="docs/assets/readme/tour/data-light.webp" alt="Code card of the last rows of data.csv">
      </picture>
      <h3>The dataset</h3>
      Start year, end year and name for each reign, ending with Elizabeth II and Charles III.
    </td>
    <td width="50%" valign="top">
      <picture>
        <source media="(prefers-color-scheme: dark)" srcset="docs/assets/readme/tour/years-dark.webp">
        <img src="docs/assets/readme/tour/years-light.webp" alt="Terminal output of requests for 1952, 2021, 2022 and 2023">
      </picture>
      <h3>Boundary years</h3>
      When two reigns share a year the later monarch is returned, so 2022 gives Charles III.
    </td>
  </tr>
</table>

<p align="center"><sub>Terminal cards are real runs of the app on localhost. Code cards show the files as they are in the repository.</sub></p>

## Features

- Single GET route with a year query parameter.
- Years mapped to monarchs once at start-up.
- Heroku files included: a Procfile for gunicorn and a runtime.txt that pins Python 3.7.6.

## Quick start

```sh
cd MonarchApi
pip install "pandas<3" flask gunicorn
flask --app app run
```

Then request a year:

```sh
curl 'http://127.0.0.1:5000/?year=1588'
```

The Heroku command in the Procfile is `gunicorn app:app`.

### Requirements

- pandas below version 3. With pandas 3 the start-up loop that fills the year series raises a dtype error. I tested pandas 2.3.3 with Python 3.12 and Flask 3.1.3, where it prints a pandas FutureWarning and answers correctly.
- The project was written for Python 3.7 and pandas 1.x, as runtime.txt shows.

## FAQ

<details>
<summary><b>How do I query it?</b></summary>

Send `GET /?year=1700`. The response is the monarch name as plain text.
</details>

<details>
<summary><b>What years are covered?</b></summary>

From 757 (Offa) to the current year. Other years return the invalid input message.
</details>

<details>
<summary><b>Why does it fail on a fresh install?</b></summary>

Current pandas rejects assigning names into the float series that app.py builds. Install `pandas<3`.
</details>

<details>
<summary><b>Is it still on Heroku?</b></summary>

The repository documents no live deployment.
</details>

If Monarch API is useful to you, a ⭐ helps other people find it.

Photos behind the screenshots are credited in [docs/assets/readme/CREDITS.md](docs/assets/readme/CREDITS.md).

[![views](https://hits.sh/github.com/mertkayacs/MonarchApi-Flask-Heroku.svg?view=today-total&style=flat-square&label=views&color=9C7A3C&labelColor=1E2A38)](https://github.com/mertkayacs/MonarchApi-Flask-Heroku)
