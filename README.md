# RequestCatcher
Flask REST API made with SQLAlchemy and Marshmallow.\
Supports CRUD operations via API calls.\
Made to catch requests and store the IP Address and Request Content to a sqlite database.
## Install Instructions
```
Clone the repository - git clone https://github.com/WanderingCoder-Omen/RequestCatcher 
Create a virtual environment - python -m venv env
Activate virtualenv
	Windows : env\Scripts\activate
	Mac and Ubuntu : . env/bin/activate
Install dependencies : pip install -r requirements.txt
Initialise the database
	At the terminal- (env)ubuntu@ubuntu:~/RequestCatcher$ python
	At the python prompt - >>> from main import db
			       >>> db.create_all()
			       >>> exit()
```
## Execution 
```
(env)ubuntu@ubuntu:~/RequestCatcher$ python main.py
```
\
Alternatively you can
## Deploy to Heroku

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy?template=https://github.com/WanderingCoder-Omen/RequestCatcher) <- By clicking this button

## Usage

### POST Request - 
```
$ curl http://localhost:5000/posts \
    -X POST \
    -H "Content-Type: application/json" \
    -d '{"ip":"127.0.0.1", "content":"Localhost"}'
```
### GET Request -
```
$ curl http://localhost:5000/posts/1
```
### PATCH Request -
```
$ curl http://localhost:5000/posts/1 \
    -X PATCH \
    -H "Content-Type: application/json" \
    -d '{"ip":"0.0.0.0", "content":"Updated content"}'
```
### DELETE Request -
```
$ curl http://localhost:5000/posts/1 -X DELETE -I
```
### To Do
Add security
