# heroku-sample

This is a tiny sample of how a web application that uses the Flask framework in Python 
can be deployed to the Heroku cloud service.  It may also be of interest as a kind of 
"hello world" minimum application for Flask. 

This application is designed to run in a Python virtual environment, which is basically 
a way of installing needed Python libraries locally in a project rather than globally. 
This project requires Flask, so we create a local environment to hold Flask and the 
additional libraries that Flask requires, like this: 

python3 -m venv env     # Creates a virtual environment in a directory called 'env'
. env/bin/activate      # Activate the virtual environment (set Python paths to local installation)
pip3 -r requirements.txt   # Install the libraries listed in requirements.txt

Then (with the virtual environment still in force) we can run the application like this: 

python3 flask_main.py

or like this: 

gunicorn flask_main:app

In the second case, we are using "green unicorn" as a proxy to run the application. 

See Flask documentation ( http://flask.pocoo.org/ ) for more details, or send me a note. 
