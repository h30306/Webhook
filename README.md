# Webhook
> Deploy website by Webhook methods and connect chatbot tutorial

## Flask or HTML?
If your project is based on Flask, you should create a virtual environment and freeze the package for requirements.txt, runtime.txt and create Procfile
Create requirement.txt:<br>
```
$ pip3 freeze > requirements.txt
$ vi requirements.txt
```
add a row:
```
gunicorn==19.3.0
```
Create Procfile:<br>
```
$ vi Procfile
```
write these in Profile:<br>
```
web: gunicorn wsgi:<Flask App Name, default is app> -preload
```
Create runtime.txt:<br>
```
python-3.6
```

## Deploy by Ngrok
>If you want to deploy by Ngrok, you can follow these steps!

1. Signup in [Ngrok](https://dashboard.ngrok.com/user/signup)<br>
2. Download Ngrok in dashboard and unzip it<br>
3. Copy authtoken to connect your account<br>
```
$ ./ngrok authtoken xxxxx
```
4. Start up your website in local end<br>
5. Copy the port of website<br>

```
$ ngrok http xxxx(port)
```
6. Copy the link to connection website by external<br>

## Heroku
>If you want to deploy on heroku, you can follow these steps!

1. Signup in [Heroku](https://dashboard.heroku.com)<br>
2. Install [Heroku CLI](https://devcenter.heroku.com/articles/heroku-cli)<br>
3. Build new project<br>
4. Go to terminal execute and login your account<br>
```
$ heroku login
```
5. Clone the project<br>
```
$ heroku git:clone -a <project name>
```
6. push into heroku<br>
```
$ cd <project name>
$ git add .
$ git commit -m "descriptionn"
$ git push heroku master
```
7. Monitor the status of Heroku
```
heroku logs --tail
```
8. Monitor the error of Flask
```
heroku run app.py –preload
```





