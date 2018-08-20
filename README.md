# Dock-DjangoPyth

_Just a little boilerplate for my futur project with Python and Django_

## Summary

- [Installation](#installation-with-docker)
- [Command useful](#command-useful)

### Installation with docker

## Create a new Project
In the root of your project launch this command for install Django Project.

```bash
$ docker-compose run python django-admin.py startproject mynewproject .
```

## Connect your database
In the `mynewproject/settings.py` you should modify the database access:
```python
DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}
```

### Command useful
__Some commands useful for the next:__

_Launch configuration in `detach Mode`_
```bash
$ docker-compose up -d
```

_Attach your CLI to Python container_
```bash
$ docker-compose exec python bash
```

_Launch a command with the container named `python`_
```bash
$ docker-compose run python [COMMAND]
```

---
__Made with <3__



