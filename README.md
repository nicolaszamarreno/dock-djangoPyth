# Dock-DjangoPyth

_Just a little boilerplate for my futur project with Python and Django_

## Summary

- [Installation](#installation-with-docker)
- [Command useful](#command-useful)
- [Launch your rocket](#launch-your-rocket)

## Installation with docker

### Create a new Project
In the root of your project launch this command for install Django Project.

```bash
$ docker-compose run python django-admin.py startproject mynewproject .
```

### Connect your database
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

## Command useful
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
## Launch your rocket
_Your installation is ready, now, you can launch your website_
You should know your address of VM machine, it's easy: `docker-machine ip`, then launch your installation `MACHINE_IP_VM:8000`

---
__Made with <3__



