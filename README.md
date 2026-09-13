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
- Smart Insights: month-end spending forecast, trend vs. last month, unusual-expense flagging, and budget tips

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript, Chart.js |
| Backend | Django |
| Database | SQLite |
| API style | REST (`/api/expenses/`) |

## Project Structure