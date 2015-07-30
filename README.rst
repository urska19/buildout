Heroku Buildpack
================

*Inspired by https://github.com/plone/heroku-buildpack-plone and https://github.com/heroku/heroku-buildpack-python. Thank you!*

Introduction
------------

This buildpack uses configuration files provided by `Plock Pins <https://github.com/plock/pins>`_ to make installation of Plone on Heroku seamless and easy

Installation
------------

Assuming your application source ``<App Source>`` is hosted by GitHub, you have a `Heroku account <https://devcenter.heroku.com/articles/getting-started-with-python#introduction>`_  and the `Heroku Toolbelt <https://toolbelt.heroku.com/>`_ is installed

Application
~~~~~~~~~~~

Clone your application source

::

    git clone <App Source>
    cd <App Source>

Buildpack
~~~~~~~~~

Create Heroku application ``<App Name>`` then configure this buildpack

::

    heroku create
    heroku buildpacks:set https://github.com/plock/buildpack.git

Plone
~~~~~

Install Plone with Plock and push to Heroku

::

    pip install plock
    plock .
    git push heroku
