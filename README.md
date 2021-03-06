# HackerSchool Flask-OAuthlib Example

Demonstrate use of OAuth2 to connect to Hacker School accounts. On demo here: http://flask-oauth-hackerschool.herokuapp.com/

The Hacker School API is documented here: https://wiki.hackerschool.com/index.php/Hacker_School_API

## Setup

1. Clone this repo and use `pip install -r requirements.txt` to get the dependencies; you may wish to do this in a [virtual environment](https://docs.python.org/dev/library/venv.html)
1. Do *Create an OAuth application* on https://www.hackerschool.com/settings
   1. Find your IP with something like `$ ifconfig en1 inet`
   2. Enter the redirect URL as something like `http://[your.ip.addr]:5000/oauth_authorized`
2. Create a `keys.sh` file and put the **ID** and **Secret** values into it
   ```bash
   export CONSUMER_KEY='[your.application.id]'
   export CONSUMER_SECRET='[your.application.secret]'
   ```

3. Put those variables in your environment with `$ source keys.sh`
4. Run the dev server with `$ ./example.py`. If you have the heroku toolbelt installed, you can run the prod server with `$ foreman start`
5. Visit the server in your browser using your IP address in something like `http://[your.ip.addr]:5000/`. Localhost and 127.0.0.1 won't work with OAuth.

## Screenshot

![logged in](https://raw.github.com/plredmond/flask-oauth-hackerschool-py/master/images/loggedin.png)
