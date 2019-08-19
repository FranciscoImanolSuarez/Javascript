# Configuring Nodemon on a Node.js server

## The constant rebooting of a Node.js application manually is a very tedious and tiring job, but to avoid having to do this work over and over again, Nodemon is responsible for automatically restarting the Node.js application server in development mode.

![img](https://miro.medium.com/max/700/1*23jQ8vUo7IBC8aHMGdTmow.png)

In the following steps, I will show you how to install and configure Nodemon in your project and how to run a Node.js. server.

## Step 1

Organize the `src` source directory and start the server in a `server.js `file, the file can carry any convention that is used to start a Node.js server ( `index.js` or `app.js`)

Update the `package.json` by adding a start script

```json
{
  "name": "nodemon",
  "version": "1.0.0",
  "description": "",
  "main": "server.js",
  "scripts": {
    "start": "node src/server.js"
  },
  "keywords": [],
  "author": "Francisco Suarez <imanolsuarez98@gmail.com>",
  "license": "MIT"
}
```

## Step 2

Add `Express` this will allow us to start a minimum server to perform this test

```javascript
'use strict';

const express = require('express');
const app = express();

app.use('/', (req, res) => {
  res.status(200).send('La API funciona correctamente');
});

app.listen(3000);
```

Start a new terminal in which we will start the server executing the script `npm start`after executing it, it will return a message like the following `node src/index.js`

Open a new terminal and execute the following code `curl -X GET http://localhost:3000/` that will allow us to verify that the API works correctly.

```javascript
$ curl -X GET http://localhost:3000/
La API funciona correctamente!
```

If we return the message `La API funciona correctamente! `it means that we are doing well!

Now, if we change the response message in the `server.js` file, you will have to restart the server manually to get the desired result:

```javascript
app.use('/', (req, res) => {
  res.status(200).send('Lorem Ipsum');
});
```

Use `CTRL + C` to stop the server that is currently running and restart it using the same command before: `npm run start.`

Using the curl command again from the terminal window we obtain the desired result:

```javascript
curl -X GET http://localhost:3000/
Lorem Ipsum
```

Step 3
Add Nodemon as `devDependency` :

```javascript
$ npm i -D nodemon
```

We will review the `package.json`

```javascript
  "name": "nodemon",
  "version": "1.0.0",
  "description": "",
  "main": "server.js",
  "scripts": {
    "start": "node src/server.js"
  },
  "keywords": [],
  "author": "Francisco Suarez <imanolsuarez98@gmail.com>",
  "license": "MIT",
  "dependencies": {
    "express": "4.15.3"
  },
  "devDependencies": {
    "nodemon": "1.11.0"
  }

```

## Stage 4

Add the dev command to the `package.json` file

```javascript
  "scripts": {
    "start": "node src/server.js",
    "dev": "nodemon --watch src src/server.js"
  }
}
```

Now run `npm run dev` and request again the use of the curl command, and we will see that the message is the same as we had before:

```javascript
curl -X GET http://localhost:3000/
Lorem Ipsum
```

If I change the message in the file `server.js `again, and this time I will not have to restart the server, since Nodemon is observing the changes using the `src` directory, through its parameter `— watch` .

You will see that it is updated only without having to restart the server, to cut it press `CTRL + C`

Thanks for reading 💻

If the article you liked or you found interesting, please help me with 👏 🤓 You can follow me on Twitter or find me on GitHub by visiting my website.