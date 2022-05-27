# About this project

An URL shortener with Python and FastAPI. Below on the table, you can see what this app can do:

| Endpoint            | HTTP Verb | Request Body    | Action                                                                 |
| ------------------- | --------- | --------------- | ---------------------------------------------------------------------- |
| /                   | GET       |                 | Returns a Hello, World! string                                         |
| /url                | POST      | Your target URL | Shows the created url_key with additional info, including a secret_key |
| /{url_key}          | GET       |                 | Forwards to your target URL                                            |
| /admin/{secret_key} | GET       |                 | Shows administrative info about your shortened URL                     |
| /admin/{secret_key} | DELETE    | Your secret key | Deletes your shortened URL                                             |

# How to run

Rename .env.example to .env and store the correct values in the file.

1. [Create a virtual environment](https://docs.python.org/3/library/venv.html):

```
$ python3 -m venv venv
```

2. Active the virtual enviroment:

```bash
$ source venv/bin/activate
# or
$ . venv/bin/activate
```

3. Install all [requirements](/requirements.txt):

```
$ pip install requirements.txt
```

4. Run [up.sh](/up.sh) script:

```
$ ./up.sh
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [22544] using statreload
INFO:     Started server process [22546]
INFO:     Waiting for application startup.
INFO:     Application startup complete.
```

# References and credits

[Build a URL Shortener With FastAPI and Python](https://realpython.com/build-a-python-url-shortener-with-fastapi/?utm_source=notification_summary&utm_medium=email&utm_campaign=2022-05-18)
