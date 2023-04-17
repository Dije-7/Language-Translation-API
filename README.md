# Project Overview

In this project, I built a translation API using deep learning. Using FastAPI, I created a web server that exposes a `/translate` route and a `/results` route. Clients will post their translation request to the `/translate` route, and get the translation results from `/results`.  The server will use a sqlite database to store the translations. On the backend, I'll use async and a pretrained deep learning language model to run the translation job.

This web server can run translation jobs quickly. This server can easily be extended to translate more languages, or add more options

**Project Steps**
* Build API routes
* Add in models to store data to database
* Create tasks to run the translation

File overview:

* `requirements.txt` - packages you'll need to install
* `main.py` - defines the web server routes
* `models.py` - defines database models
* `tasks.py` - runs our backend tasks, including the translation

## Usage

* To run the server locally, run `uvicorn main:app --reload`.

* To build the docker container * `docker build -t dlapi .`

* If you're not running on 64-bit linux, instead run `docker buildx build --platform linux/amd64 -t dlapi
