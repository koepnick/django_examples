# Boilerplate

## Python Packages

Required:
* django

Optional:
* django-extensions
* ipython
* ipdb
* pudb

## Overview

Boilerplate code is boring and gross. Thankfully, Django has our back!

From `${PROJECT_ROOT}` run:

```
$> django-admin startproject pantry_manager
```

This should create a single directory named 'pantry_manager'

For the rest of this project, `${DJANGO_ROOT}` is 'pantry_manager' 

If you really want a gold star, go ahead and add this to your `~/.bashrc` file.

### Sanity check

From `${DJANGO_ROOT}` run:

```
$> python manage.py runserver

Watching for file changes with StatReloader
Performing system checks...

System check identified no issues (0 silenced).

You have 18 unapplied migration(s). Your project may not work properly until you apply the migrations for app(s): admin, auth, contenttypes, sessions.
Run 'python manage.py migrate' to apply them.
February 04, 2021 - 02:52:13
Django version 3.1.6, using settings 'pantry_manager.settings'
Starting development server at http://127.0.0.1:8000/
Quit the server with CONTROL-C.
```

Open your web browser of choice and navigate to [http://localhost:8000](http://localhost:8000)

If you’ve made it this far, congratulations! Go ahead and add it to your résumé. You’ve earned it.

From here on out, there will be far less hello-ing of worlds.
