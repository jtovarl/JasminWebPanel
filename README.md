# JasminWebPanel
Jasmin Sms Web Interface
Installation
Download Extract This folder

Installing

We recommend installing in a virtualenv

Install dependencies:

$ pip install -r requirements.pip

cd to jasmin_api and run:

$ ./manage.py migrate $ ./manage.py createsuperuser $ ./manage.py collectstatic

The last is only needed if you are running the production server (see below) rather than the Django dev server. It should be run again on any upgrade that changes static files. If in doubt, run it.
You can also override the default settings for the telnet connection in local_settings.py. These settings with their defaults are:

TELNET_HOST = '127.0.0.1'
TELNET_PORT = 8990
TELNET_USERNAME = 'jcliadmin'
TELNET_PW = 'jclipwd'
Running

To run for testing and development: cd JasminWebPanel;./manage.py runserver

This is slower, requires DEBUG=True, and is much less secure

To run on production:

cd JasminWebPanel;run_cherrypy.py
This requires that you run the collectstatic command (see above) and you should have DEBUG=False