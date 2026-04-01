# TO_DO APPLICATION

Simple, clean to‑do application built with Django and Tailwind (Create, edit, complete and delete).

### Features
- **CRUD tasks**: add, view, update, and delete
- **Due dates** with native date picker
- **Completion state** with clear badges
- **Responsive UI** using Tailwind CDN

### Tech Stack
- **Backend**: Django 5.x
- **Database**: SQLite (default)
- **Frontend**: Tailwind CSS (CDN)
- **Python**: 3.13+

### Project Structure
```text
aibos/
  manage.py
  db.sqlite3
  to_do/              # Django project settings
  user/               # App: models, forms, views, urls, templates
    templates/user/
      base.html
      task_list.html
      task_detail.html
      task_form.html
      task_confirm_delete.html
```

### Quick Start

1) Clone and enter the project directory
```bash
git clone <your-repo-url> aibos
cd aibos
```

2) Create and activate a virtual environment
```bash
python -m venv .myenv
.\.myenv\Scripts\activate  # Windows PowerShell
```

3) Install dependencies
```bash
pip install --upgrade pip
pip install django
```

4) Run migrations
```bash
python manage.py migrate
```

5) Start the development server
```bash
python manage.py runserver
```

6) Open the app
- Home (task list): `http://127.0.0.1:8000/`
- Add task: `http://127.0.0.1:8000/task/add/`
- Task detail: `http://127.0.0.1:8000/task/<id>/`
- Edit task: `http://127.0.0.1:8000/task/<id>/edit/`
- Delete task: `http://127.0.0.1:8000/task/<id>/delete/`

### App URLs (namespaced as `user`)
```text
user:task_list     -> /
user:task_add      -> /task/add/
user:task_detail   -> /task/<id>/
user:task_edit     -> /task/<id>/edit/
user:task_delete   -> /task/<id>/delete/
```

### Forms and Styling
- Inputs are styled with Tailwind classes via Django form widgets in `user/forms.py`.
- Templates extend `user/base.html` and define `title` and `content` blocks.
- Tailwind is loaded via CDN in `base.html` (good for development; consider a build pipeline for production).





