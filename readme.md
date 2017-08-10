# docker-compose postgres and django example

This was the result of following the demo located in the [docker documentation](https://docs.docker.com/compose/django/#connect-the-database)

Create the app by running `docker-compose run web django-admin.py startproject <your_project_name_here> .`

Once youve created it, update the <your_project_name_here>\settings.py file, replacing `DATABASES=` 
with `DATABASES = {
    'default': {
        'ENGINE': 'django.db.backends.postgresql',
        'NAME': 'postgres',
        'USER': 'postgres',
        'HOST': 'db',
        'PORT': 5432,
    }
}` 

To run the app, run `docker-compose up`
To run the app in daemon mode, use the `-d` flag

The site will be browsable at localhost:8000