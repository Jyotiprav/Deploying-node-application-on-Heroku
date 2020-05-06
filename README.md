# Deploying-node-application-on-Heroku

Step 1: Download heroku 
https://devcenter.heroku.com/articles/heroku-cli

Step 2:Create account on Heroku
https://signup.heroku.com/dc

Step 3:Install git
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

Step 4:Setting up the git for application
open terminal in your project directory and write
```
git init
git add .
git commit -m "initial commit"

```
Step 5:Add a Heroku Git(https://devcenter.heroku.com/articles/git#creating-a-heroku-remote)
```
heroku login
heroku create
```
Step 6: Add a Procfile (This file tells Heroku which commands to run to start your app.)
```
touch Procfile

Step 7: Inside this Procfile write the following code:
```
web: node app.js
```

