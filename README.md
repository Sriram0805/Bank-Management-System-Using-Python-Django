How to Run the Code
To run the Bank Management System locally, follow these steps:

Prerequisites:
Ensure the following tools and software are installed on your system:

Python >= 3.7

Redis Server

Git

pip

Virtualenv

Steps to Setup:
Install Redis Server: Follow the Redis Quick Start Guide to install Redis. Start the Redis server:

redis-server
Create a Virtual Environment: Use virtualenv to set up an isolated Python environment:

virtualenv venv
source venv/bin/activate
Or using virtualenvwrapper:

mkvirtualenv -p python3 bank_system
workon bank_system
Clone the Project: Clone the GitHub repository and navigate to the project directory:

git clone git@github.com:saadmk11/banking-system.git
cd banking-system
Install Dependencies: Install required Python packages from requirements.txt:

pip install -r requirements.txt
Apply Database Migrations: Initialize the database using Django migrations:

python manage.py migrate
Create Superuser: Create an admin account for managing the system:

python manage.py createsuperuser
Run the Development Server: Start the local Django server:

python manage.py runserver
Access the application at http://127.0.0.1:8000/.

Run Celery Workers and Scheduler: Open separate terminal windows (activate the virtual environment in each terminal):

Start the Celery worker:

celery -A banking_system worker -l info
Start the Celery scheduler:
