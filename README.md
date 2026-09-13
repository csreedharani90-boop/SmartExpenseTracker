# Smart Expense Tracker

A full-stack expense tracking web application built with Django (backend/REST API) and a single-page HTML/CSS/JavaScript frontend. Tracks expenses with categories, a monthly budget bar, a spending-by-category pie chart, and a Smart Insights panel that forecasts month-end spending and flags unusual expenses.

## Features

- Full CRUD (Create, Read, Update, Delete) for expenses
- Live summary cards: total spent, entry count, top category
- Monthly budget tracker with a color-coded progress bar (green / amber / red)
- Pie chart of spending by category (Chart.js)
- Search by title, filter by category, sort by date/amount
- CSV export of all expenses
- Dark mode toggle (saved across sessions)
- Smart Insights: month-end spending forecast, trend vs last month, unusual-expense flagging, and budget tips

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript, Chart.js |
| Backend | Django |
| Database | SQLite |
| API style | REST (/api/expenses/) |

## Project Structure

- expenses/ - Django app: models, views, serializers, API routes
- expensetracker/ - Django project settings and root URL config
- templates/index.html - Single-page frontend (HTML + CSS + JS)
- manage.py - Django management script
- requirements.txt - Python dependencies

## Setup and Installation

Prerequisites: Python 3.10 or higher installed.

1. Clone the repository

       git clone https://github.com/csreedharani90-boop/SmartExpenseTracker.git
       cd SmartExpenseTracker

2. Create and activate a virtual environment

       python -m venv venv
       venv\Scripts\activate

3. Install dependencies

       pip install -r requirements.txt

4. Run database migrations

       python manage.py migrate

5. Start the development server

       python manage.py runserver

6. Open the app

   Visit http://127.0.0.1:8000/ in your browser.

## API Endpoints

| Method | Endpoint | Description |
|---|---|---|
| GET | /api/expenses/ | List all expenses |
| POST | /api/expenses/ | Create a new expense |
| GET | /api/expenses/id/ | Retrieve a single expense |
| PUT | /api/expenses/id/ | Update an existing expense |
| DELETE | /api/expenses/id/ | Delete an expense |

## Notes

- The monthly budget is stored in browser localStorage, per device.
- CSV export downloads all expenses currently in the database, not just the filtered or visible ones.