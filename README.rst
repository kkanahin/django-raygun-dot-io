django-raygun-dot-io
==========================

This package provides a Django middleware class that handles errors
and will send them to the Raygun.IO service if the appropriate settings
are enabled.

Installation
------------

Install from Github:

::

    $ pip install -e git://github.com/xxbrandonoxx/django-raygun-dot-io.git#egg=django-raygun-dot-io

Add the middleware class to your ``MIDDLEWARE_CLASSES``:

::

    MIDDLEWARE_CLASSES = (
        'django.middleware.common.CommonMiddleware',
        'django.contrib.sessions.middleware.SessionMiddleware',
        'django.middleware.csrf.CsrfViewMiddleware',
        'django.contrib.auth.middleware.AuthenticationMiddleware',
        'django.contrib.messages.middleware.MessageMiddleware',
        'raygun_dot_io.middleware.RaygunDotIOMiddleware',
    )

And then add your settings.

Settings
--------

* ``RAYGUN_API_URL``: This allows you to override the default
  raygun api URL. (Default: ``https://api.raygun.io/entries``)

* ``RAYGUN_API_KEY``: This is your private Raygun.IO API Key
  for the configured application.  Please get this from
  Application Settings at https://app.raygun.io/

License
-------

BSD, short and sweet.