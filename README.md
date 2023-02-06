![dpaste image](https://img.shields.io/pypi/v/dpaste.svg)
[![Python CI](https://github.com/DarrenOfficial/dpaste/actions/workflows/python.yml/badge.svg)](https://github.com/DarrenOfficial/dpaste/actions/workflows/python.yml)
[![Docker Image CI](https://github.com/DarrenOfficial/dpaste/actions/workflows/docker.yml/badge.svg)](https://hub.docker.com/r/darrenofficial/dpaste)
![Code Quality](https://api.codacy.com/project/badge/Grade/185cfbe9b4b447e59a40f816c4a5ebf4)

📖 Full documentation on [https://docs.dpaste.org](https://docs.dpaste.org)

requires at a minimum Python 3.6 and Django 3.2.


-----------------


Checklist:
----------

```
python3 -m venv .venv
source .venv/bin/activate
pip install -e .[dev]
./manage.py migrate
./manage.py runserver
```

```
sudo apt install npm
make css
sudo apt purge npm
./manage.py collectstatic
```



dpaste with docker-compose for local development
-------------


The project’s preferred way for local development is docker-compose:

$ docker-compose up

This will open the Django runserver on http://127.0.0.1:8000. Changes to the code are automatically reflected in the Docker container and the runserver will reload automatically.

Upon first run you will need to migrate the database. Do that in a separate terminal window:

$ docker-compose run --rm app ./manage.py migrate
