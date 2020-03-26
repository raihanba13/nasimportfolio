# nasimportfolio
Django full functional portfolio + blog web application.

Prerequisite:
1: python 3.8

Install:
Download or clone the reposatory. Goto project root folder.

C:\>git clone https://github.com/Nasim-NIMU/nasimportfolio.git

C:\>cd nasimportfolio

C:\nasimportfolio>cd djnago

C:\nasimportfolio\django>scripts\activate.bat

(django)C:\nasimportfolio\django>cd ..

(django)C:\nasimportfolio>pip install -r requirements.txt

(django)C:\nasimportfolio>python manage.py migrate

(django)C:\nasimportfolio>python manage.py runserver

It will start a local server on 'http://localhost:8000'

create a super user using,

(django)C:\nasimportfolio>python manage.py createsuperuser

then go to http://localhost:8000/admin to accesss your administrations to control your dynamic application.


It's ready to deploy in heroku.Before deploy in heroku, change the local database in settings.py according to:

You will find database settings like this.
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.sqlite3',
        'NAME': os.path.join(BASE_DIR, 'db.sqlite3'),
    }
}

You need to change it like below,
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql_psycopg2',
        'NAME': 'personal_db',
        'USER': 'your user',
        'PASSWORD': 'your password',
        'HOST': 'localhost',
        'PORT': '2000',
        
    }
}

Congrats! everything is setup. Your project ready to deploy in heroku for live your project online.
