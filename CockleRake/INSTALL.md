# CockleRake Installation

Steps required to install CockleRake (on a Linux-based system at least)

1. Install `virtualenv`
1. Set up the virtualenv environment
 
 ```
    cd ..
    virtualenv CockleRake
 ```
 
1. Activate the virtualenv environment

 ```
    cd CockleRake
    source bin/activate
 ```

1. Now install Flask for our web server

 ```
    pip install flask
 ```

1. Configure any custom settings by editing `settings.cfg`.  The DATABASE setting must match the filename you use in the following step (for example 'cockles.db').  The most likely setting you should configure is the WORKSHOP_NAME.
1. Tell the server where to find the settings file (change `settings.cfg` to point to the correct settings file if you've changed its name or location)

 ```
    export COCKLE_SETTINGS=settings.cfg
 ```

1. Create a database to hold any registered Cockles and their readings

 ```
    sqlite3 cockles.db < schema.sql
 ```

1. Run the CockleRake server

 ```
    python cockle-rake.py
 ```
