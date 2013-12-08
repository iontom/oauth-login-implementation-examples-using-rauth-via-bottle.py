oauth-login-implementation-examples-using-rauth-via-bottle.py
=============================================================

OAuth Login Implementation Examples using rauth via Bottle.py

Prerequisites:
==============
* `pip`
* `virtualenv`
* `bottle`
* `rauth`

Installing the prerequisites:
=============================
1. Install `pip` and `virtualenv`: `sudo easy_install pip virtualenv`
2. Clone the repository: `git clone https://github.com/ejelome/oauth-login-implementation-examples-using-rauth-via-bottle.git`
3. Go to the directory: `cd oauth-login-implementation-examples-using-rauth-via-bottle`
4. Create a virtualenv: `virtualenv venv`
5. Activate virtualenv: `source venv/bin/activate`
6. Install remaining prerequisites (`bottle` and `rauth`): `pip install -r requirements.txt`

Modify the `hosts` file:
========================
In order to make the OAuth APIs work in our local machine, we need to modify the hosts file and pretend we're visiting an online URI:
* When testing Facebook and Twitter examples, make sure that the local address (`127.0.0.1`) points to `mydomain.tld`
* When testing the Google example, the `mydomain.tld` won't work since Google seem to know that it's an invalid URI
* We can solve these issues by setting 2 aliases for the `127.0.0.1` address

1. Open the hosts file: `sudo gedit /etc/hosts`
2. Add the following line: `127.0.0.1 mydomain.tld`

Running the program:
====================
1. Execute one of the following:
```
python oauth2-facebook.py # Facebook
python oauth1-twitter.py # Twitter
python oauth2-google.py # Google
```

2. Open a browser and go to: `http://localhost:8000`
3. To Login:
   * Click *Log in using xyz*, where xyz is either Facebook, Twitter, or Google
   * Or go to: `http://localhost:8000/login`

Notes:
======
* More detailed information are included in each of the executable files (there are also in the `config.py` file)
* You can change the OAuth API settings on `config.py` file
* You can change other configurations on the `config.py` file
* Coding conventions are based on PEP 8 to make sure that you're also seeing good code examples
* The examples were done as minimal as possible so you can get a better understanding of OAuth and how simple it is
* Happy coding! :)

Recent Changes:
===============
* None
