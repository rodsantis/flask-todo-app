# Flask Todo App

A personal task manager built with Flask, SQLite, and Bootstrap. Users register, log in, and manage their own todo lists. The app also includes feedback forms for logged-in users and visitors.

Originally created as the final project for [CS50's Introduction to Computer Science](https://cs50.harvard.edu/x/).

## Features

- User registration and login with hashed passwords
- Per-user todo lists (add, mark done, delete)
- In-app feedback form for authenticated users
- Public feedback / help request form for visitors
- Responsive UI with Bootstrap 5

## Project structure

```
flask-todo-app/
├── app.py              # Flask routes and application config
├── helpers.py          # Login decorator and error helpers
├── requirements.txt    # Python dependencies
├── schema.sql          # Database schema (for fresh installs)
├── todolist.db         # SQLite database (included with sample data)
├── static/
│   └── styles.css
└── templates/
    ├── layout.html
    ├── index.html
    ├── todo.html
    ├── login.html
    ├── register.html
    ├── feedback.html
    ├── outerfeedback.html
    ├── thank.html
    └── apology.html
```

## Requirements

- Python 3.10 or newer
- pip

## Setup

1. Clone or download the project and enter the directory:

   ```bash
   cd flask-todo-app
   ```

2. Create and activate a virtual environment (recommended):

   ```bash
   python3 -m venv .venv
   source .venv/bin/activate   # Linux / macOS
   # .venv\Scripts\activate    # Windows
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Create a fresh database from the schema:

   ```bash
   sqlite3 todolist.db < schema.sql
   ```

5. Run the application:

   ```bash
   python app.py
   ```

6. Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

## Usage

1. **Register** a new account at `/register`.
2. **Log in** at `/login`.
3. From the home page, open **To do!** to add and manage tasks.
4. Use **Feedback** to send suggestions (available inside and outside the app).

## Environment variables

| Variable     | Description                                      | Default                          |
| ------------ | ------------------------------------------------ | -------------------------------- |
| `SECRET_KEY` | Flask session signing key (set in production)  | `dev-secret-change-in-production` |

Example:

```bash
export SECRET_KEY="your-random-secret-here"
python app.py
```

## Tech stack

- **Backend:** Python, Flask, Flask-Session
- **Database:** SQLite via the [CS50 SQL library](https://github.com/cs50/python-cs50)
- **Frontend:** HTML, Jinja2 templates, Bootstrap 5, custom CSS
- **Security:** Werkzeug password hashing, login-required route protection

## License

This project is open source and available under the [MIT License](LICENSE).

---

**Happy coding! 🚗💨**
