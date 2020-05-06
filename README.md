# Deploying-node-application-on-Heroku

<strong> Step 1:</strong> Download heroku 
https://devcenter.heroku.com/articles/heroku-cli

<strong> Step 2:</strong>Create account on Heroku
https://signup.heroku.com/dc

<strong> Step 3:</strong>Install git
https://git-scm.com/book/en/v2/Getting-Started-Installing-Git

<strong> Step 4:</strong>Setting up the git for application
open terminal in your project directory and write
```
git init
git add .
git commit -m "initial commit"

```
<strong> Step 5:</strong>:Add a Heroku Git(https://devcenter.heroku.com/articles/git#creating-a-heroku-remote)
```
heroku login
heroku create
```
<strong> Step 6:</strong> Add a Procfile (This file tells Heroku which commands to run to start your app.)
```
touch Procfile
```
<strong> Step 7:</strong> Inside this Procfile write the following code:
```
web: node app.js
```
<strong> Step 8:</strong>Listen to the right port
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
<strong> Step 9:</strong>Use a cloud database(MongoDB atlas)

<strong> Step 10:</strong> Language specific setup(https://devcenter.heroku.com/articles/deploying-nodejs)
Specify the version of node in package.json
```
"engines": {
    "node": "13.7.0"
  }
 ```
To check the version type node --version in terminal.

<strong> Step 11:</strong> Creating .gitignore (To install npm dependencies whenever user runs the application)
```
Inside terminal write:

touch .gitignore

Write following code inside .gitignore file.

/node_modules
npm-debug.log
.DS_Store
/*.env
```
<strong> Step 12:</strong> Deploying on Heroku

```
git add .
git commit -m "added Procfile,port and gitignore"
git push heroku master
```
Reference Link: 
https://devcenter.heroku.com/articles/preparing-a-codebase-for-heroku-deployment
https://devcenter.heroku.com/articles/deploying-nodejs







