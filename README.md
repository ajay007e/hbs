# Starting Template

Node.js Starting Template - Express - Handlebars - MongoDB

## Prerequisites
- Install [Node js](https://nodejs.org/en/download/)
- Install [Mongo DB](https://www.mongodb.com/try/download/community)



## Setup

### Step 1 - Create a Repository Folder
Create a folder in the local system in order to work with the project 
```
mkdir <folder_name>
cd <folder_name>
```

### Step 2 - Create hbs Project

```
express --hbs
npm install

```
In order to fix vulnerabilities
```
npm audit fix
```

### Step 3 - Step Up Nodemon

```
npm install nodemon

```

Change the scripts in  *package.json* to

```
"scripts": {
    "start": "nodemon ./bin/www"
  }
```

### Step 3 - Clear Default Files

- Clear the *style.css*
-
-
-

### Step 4 - Engine Setup

Install Handlebars

```
npm install express-handlebars
```

Add the code to *app.js*

```javascript
var hbs = require("express-handlebars");

app.engine(
  "hbs",
  hbs({
    extname: "hbs",
    defaultLayout: "layout",
    layoutsDir: __dirname + "/views/layout/",
    partialsDir: __dirname + "/views/partials/",
  })
);

```
Also Create *Layout* folder and *Partials* folder inside **views** :

```
cd views
mkdir layout 
mkdir partials

```

Create *layout.hbs* inside layout folder and add necessary external Files
