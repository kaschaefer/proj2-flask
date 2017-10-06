# proj2-flask
Author: Mikaela Schaefer

Contact: kaelas@uoregon.edu

## Description
This simple web server serves a class syllabus in a table, where the table is broken into
the weeks of the term. Each entry in the table lists the week number, the beginning date of
each week, and the topics and projects that correspond to that week. It also highlights which
week is currently in session in a tomato red color.

## Software Description
Jinja templating is used to fill in the web page from data in the session state. Venv is used to package 
dependencies, which are listed in requirements.txt. The Arrow module for Flask is used to configure starting dates and
to calculate which week is the current week at any given time. The provided Makefile is configured to run venv to install
the necessary packages and to run the program.

## Installation
The provided Makefile can run the server in two ways:

### Development
`Make install` will configure the virtual environment without running the code, whereas `Make run` will first execute `Make install` and
and then run Flask's built in test server. When testing, port 5000 is used.

### Deployment
`Make start` starts a Green Unicorn (gunicorn) server; You do not need to install dependencies before running this command. The server
utilizes port 8000 in this case. `Make stop` will kill the process.
