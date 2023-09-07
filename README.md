# Django Server README

This README will guide you through the process of setting up and running the Django Server from this repository. Follow these steps to get your project up and running in no time!

## Table of Contents

- [1. Clone the Repository](#1-clone-the-repository)
- [2. Create a Virtual Environment](#2-create-a-virtual-environment)
- [3. Install Dependencies](#3-install-dependencies)
- [4. Configure Environment Variables](#4-configure-environment-variables)
- [5. Configure `settings.py`](#5-configure-settingspy-database)
- [6. Run Migrations](#6-run-migrations)
- [7. Run the Development Server](#7-run-the-development-server)

## 1. Clone the Repository

Clone this repository to your local machine using the following command:

```bash
git clone https://github.com/twilight04/django-server.git
```

## 2. Create a Virtual Environment

It's a good practice to work within a virtual environment to isolate project dependencies. Navigate to your project directory and create a virtual environment using `virtualenv` (or `venv` if you're using Python 3):

```bash
cd project_name
virtualenv venv
```

Activate the virtual environment:

- On Windows:

```bash
venv\Scripts\activate
```

- On macOS and Linux:

```bash
source venv/bin/activate
```

## 3. Install Dependencies

With your virtual environment activated, install the project dependencies using `pip`. Make sure you are in the project directory where the `requirements.txt` file is located:

```bash
pip install -r requirements.txt
```

## 4. Configure Environment Variables

Create a `.env` file in the project root directory based on the provided `.env.example` file.

Edit the `.env` file to set your environment-specific variables such as credentials and keys.

## 5. Configure `settings.py` Database

Open the `settings.py` file located in your project's directory (`server/settings.py`). Update the database settings according to your `.env` configuration.

```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.mysql',
        'NAME': 'your_db_name',
        'USER': 'root',
        'PASSWORD': '',
        'HOST': 'localhost',
        'PORT': '3306'
    }
}
```

## 6. Run Migrations

Apply the database migrations to create the database schema:

```bash
python manage.py migrate
```

## 7. Run the Development Server

You're almost there! Start the development server to run your Django server:

```bash
python manage.py runserver
```

Your Django server should now be up and running. Open a web browser and navigate to `http://127.0.0.1:8000/` to access your application.

That's it! You've successfully set up and started your Django server!
