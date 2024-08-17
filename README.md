Guide to download and run in your machine:

Python version 3.12.3

Setup of the Backend:

// Create the env file out side the backend directory

1º - python -m venv env 
    - on windows: 
        env/Scripts/activate
    - on linux/mac:
        source bin/activate

2º - put "requirements.txt" at the same directory env folder

3º - python install -r requirements.txt

//To run on localhost: go to setting.py at project root

4º - find this part of the code bellow:

        DATABASES = {
            "default": {
                "ENGINE": "django.db.backends.postgresql",
                "NAME": os.getenv("DB_NAME"),
                "USER": os.getenv("DB_USER"),
                "PASSWORD": os.getenv("DB_PWD"),
                "HOST": os.getenv("DB_HOST"),
                "PORT": os.getenv("DB_PORT"),
            }
        }

4.1 º - comment/delete it. Now copy it in place:

        DATABASES = {
            'default': {
                'ENGINE': 'django.db.backends.sqlite3',
                'NAME': BASE_DIR / 'db.sqlite3',
            }
        }

// The source code configured here is for deployment that's why need to change the setting above
// Now just run these codes

5º - python manage.py makemigrations

6º - python manage.py migrate

7º - python manage.py runserver

with the server running - create another terminal aside and setup the frontend

--------------------------------------

Frontend:

1º - npm install

2º - npm run dev

Enter Frontend App -> { "ctrl" + "click" : "at localhost: http://localhost:5173/" } 😉

// Vite app
Go to /register path

register yourself

log in... 🦅

Create notes/ Delete notes!! 🐦


Done! The App is running and working properly on localhost! 😄 🙌









