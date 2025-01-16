# COMPSCI 235 Starter Repository for the Games WebApp Assignments
This is a starter repository for the games webapp assignments of CompSci 235 in Semester 2, 2023.

## Description

This repository contains an implementation of the domain model from Assignment 1. It contains unit tests which can be run through pytest. It also contains a simple Flask application that renders content of a Game object instance from our domain model on a blank HTML page. 

This website has features to search for games by name, publisher and genres. You can filter games by genre using the sidebar and also an option to view all the games.

An implementation has been written to obtain data from a csv file and parse the information in such a way that the website can take advantage of the data given.

## Installation

**Installation via requirements.txt**

**Windows**
```shell
$ cd <project directory>
$ py -3 -m venv venv
$ venv\Scripts\activate
$ pip install -r requirements.txt
```

**MacOS**
```shell
$ cd <project directory>
$ python3 -m venv venv
$ source venv/bin/activate
$ pip install -r requirements.txt
```

When using PyCharm, set the virtual environment using 'File or PyCharm'->'Settings' and select your project from the left menu. Select 'Project Interpreter', click on the gearwheel button and select 'Add Interpreter'. Click the 'Existing environment' radio button to select the virtual environment. 

## Execution

**Running the application**

From the *project directory*, and within the activated virtual environment (see *venv\Scripts\activate* above):

````shell
$ flask run
```` 

## Testing

After you have configured pytest as the testing tool for PyCharm (File - Settings - Tools - Python Integrated Tools - Testing), you can then run tests from within PyCharm by right-clicking the tests folder and selecting "Run pytest in tests".

Alternatively, from a terminal in the root folder of the project, you can also call 'python -m pytest tests' to run all the tests. PyCharm also provides a built-in terminal, which uses the configured virtual environment. 

## Configuration

The *project directory/.env* file contains variable settings. They are set with appropriate values.

* `FLASK_APP`: Entry point of the application (should always be `wsgi.py`).
* `FLASK_ENV`: The environment in which to run the application (either `development` or `production`).
* `SECRET_KEY`: Secret key used to encrypt session data.
* `TESTING`: Set to False for running the application. Overridden and set to True automatically when testing the application.
* `WTF_CSRF_SECRET_KEY`: Secret key used by the WTForm library.
* `REPOSITORY`: Lets you choose between `database` or `memory`

## Data sources

The data files are modified excerpts downloaded from:

https://huggingface.co/datasets/FronkonGames/steam-games-dataset



