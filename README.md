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
Step 8:Listen to the right port
write following code in app.js
```
let port = process.env.PORT;
if (port == null || port == "") {
  port = 3000;
}

app.listen(port,function(){
  console.log("Server is running");
})
```
Step 9:Use a cloud database(MongoDB atlas)

Step 10: Language specific setup(https://devcenter.heroku.com/articles/deploying-nodejs)
Specify the version of node in package.json
```
"engines": {
    "node": "13.7.0"
  }
 ```
To check the version type node --version in terminal.

Step 11: Creating .gitignore (To install npm dependencies whenever user runs the application)
```
Inside terminal write:

touch .gitignore

Write following code inside .gitignore file.

/node_modules
npm-debug.log
.DS_Store
/*.env
```
Step 12: Deploying on Heroku

```
git add .
git commit -m "added Procfile,port and gitignore"
git push heroku master
```







