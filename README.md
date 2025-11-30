# Smart Task Analyzer

## Quick start (local)
1. Create project folder `task-analyzer` and place files accordingly.
2. Create venv:


for running the projects use this cmd in your Device
# activate venv first (example for Windows & Unix)
# Windows:
venv\Scripts\activate
# mac/linux:
source venv/bin/activate

pip install -r requirements.txt        # or pip install django
python manage.py makemigrations
python manage.py migrate
python manage.py runserver

## sample json file to test
[
  {"id": 1, "title": "Fix critical bug", "due_date": "2025-12-01", "importance": 10, "estimated_hours": 3, "done": false},
  {"id": 2, "title": "Write README", "due_date": "2025-11-30", "importance": 6, "estimated_hours": 1, "done": false},
  {"id": 3, "title": "Setup CI", "due_date": "2025-12-10", "importance": 8, "estimated_hours": 6, "dependencies": [1], "done": false},
  {"id": 4, "title": "Old task", "due_date": "1990-01-01", "importance": 5, "estimated_hours": 2, "done": false}
]

# file strecture
task-analyzer/
├── backend/                  # django project
│   ├── settings.py
│   └── urls.py
├── tasks/
│   └── views.py              # API views already created
├── frontend/                 # add this into project root
│   ├── static/
│   │   ├── css/
│   │   │   └── styles.css
│   │   └── js/
│   │       └── script.js
│   └── templates/
│       └── index.html

