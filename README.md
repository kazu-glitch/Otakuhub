# OtakuHub

OtakuHub is an anime watch party platform built for a course project. It includes a responsive frontend, Flask backend, and MySQL database for managing anime lists, watch rooms, comments, schedules, and user activity.

## Features

- Watch party rooms
- Anime list tracking
- Episode progress tracking
- Anime countdown schedules
- Comments and reviews
- Anime-themed reactions
- Favorite anime lists
- User profile section
- User registration and login
- Flask session management
- CSRF protection for API writes
- Admin dashboard
- Warm orange/yellow theme
- Flask REST API
- MySQL schema and seed data

## Tech Stack

- HTML
- CSS
- JavaScript
- Python Flask
- MySQL

## Project Folders

```text
assets/              Shared image assets
docs/                API and project documentation
otakuhub_flask/      Flask + MySQL full-stack version
index.html           Static frontend entry
styles.css           Static frontend styles
app.js               Static frontend logic
```

## Documentation

- [API Reference](docs/API_REFERENCE.md)
- [Database ERD](docs/DATABASE_ERD.md)
- [Security Architecture](docs/SECURITY_ARCHITECTURE.md)
- [Testing Notes](docs/TESTING.md)

## Run The Flask Version

```powershell
cd otakuhub_flask
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env
python init_db.py
flask run
```

Open:

```text
http://127.0.0.1:5000
```

Demo login:

```text
mika@example.com / otakuhub123
```

## Demonstration Video

Add your unlisted YouTube or Google Drive video link here before submission:

```text
TODO: paste demonstration video link
```

## Demo Anime

- Naruto
- One Piece
- Attack on Titan
- Hunter x Hunter

## Commit Progress

This repository is being developed through a structured 50-commit course workflow.
