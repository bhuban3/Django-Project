📝 Django CRUD Project with MySQL
A simple CRUD (Create, Read, Update, Delete) web application built using Django, MySQL, and Pipenv for managing student records.

🚀 Features
Add new students

Edit existing student details

Delete student records

View list of all students

📁 Project Structure
csharp
Copy
Edit
Django/
│
├── manage.py
├── Pipfile
├── Pipfile.lock
├── db.mysql (MySQL-based DB config)
├── students/       # App folder
│   ├── migrations/
│   ├── templates/
│   ├── models.py
│   ├── views.py
│   ├── urls.py
│   └── ...
└── django_crud/     # Project folder
    ├── settings.py
    ├── urls.py
    └── ...
⚙️ Prerequisites
Python ≥ 3.8

Pipenv

MySQL Server

MySQL client (mysqlclient or connector)

🛠️ Installation Steps
1. 📦 Clone the Repository
bash
Copy
Edit
git clone <your-repo-url>
cd Django
2. 🌱 Create Virtual Environment with Pipenv
bash
Copy
Edit
pipenv install
pipenv shell
This will activate the virtual environment and install dependencies from Pipfile.

3. 🛢️ Setup MySQL Database
Open MySQL and run:

sql
Copy
Edit
CREATE DATABASE studentdb;
Update your settings.py database section:

python
Copy
Edit
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'studentdb',
        'USER': 'your_mysql_user',
        'PASSWORD': 'your_mysql_password',
        'HOST': 'localhost',
        'PORT': '3306',
    }
}
4. 🔧 Apply Migrations
bash
Copy
Edit
python manage.py makemigrations
python manage.py migrate
5. 👤 Create Superuser (optional)
bash
Copy
Edit
python manage.py createsuperuser
6. 🚴 Run Development Server
bash
Copy
Edit
python manage.py runserver
Then visit: http://127.0.0.1:8000/
