# Simple Django project structure
## About
According to [recommended django project layout](https://www.revsys.com/tidbits/recommended-django-project-layout/),
[django-environ lib](https://github.com/joke2k/django-environ) and my experience.

For your convenience here is the project structure via bash `tree` util:

```
django_example
├── app
│   ├── admin.py
│   ├── apps.py
│   ├── __init__.py
│   ├── migrations
│   │   └── __init__.py
│   ├── models.py
│   ├── static
│   │   ├── css
│   │   ├── img
│   │   └── js
│   ├── templates
│   ├── tests
│   │   ├── __init__.py
│   │   └── tests.py
│   └── views.py
├── django_example
│   ├── __init__.py
│   ├── settings
│   │   ├── base.py
│   │   ├── dev.py
│   │   ├── __init__.py
│   │   └── prod.py
│   ├── settings.py
│   ├── urls.py
│   └── wsgi.py
├── Dockerfile
├── .env
├── .gitignore
├── manage.py
├── README.md
├── requirements_dev.txt
├── requirements.txt
├── scripts
│   ├── deploy
│   │   └── script.sh
│   └── local
├── templates
│   └── base.html
└── .travis.yml
```

## Installation
Just simply run the following:
```bash
django-admin startapp --template=https://github.com/sadmonad/django_example/archive/0.0.1.zip <project_name>
cd django_example/ && virtualenv env && . env/bin/activate
pip install -r requirements_dev.txt
python manage.py runserver --settings=django_example.settings.dev
```

## Support
Contributing and issues opening are welcome! 