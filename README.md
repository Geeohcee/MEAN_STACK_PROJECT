# MEAN_STACK_PROJECT

### What is a Tech Stack ?
**A Tech stack comprises of the many components which work together to produce an application which serves the needs of users and businesses. This comprises of** |Front-end framework|Back-end framework|Database technologiees|
1. **Front-end framework** does most of the “heavy lifting” of building a complex website or mobile app, so the developers and designers can focus on providing the specific features and fixes needed by the users and the business. **E.g React.js** 
2. **Back-end framework** does most of the “heavy lifting” of communication between the website or mobile app and the database and business logic. **E.g Express.js** 
3. **Database technologies** store and organize data, as well as provide features for searching, filtering, and reporting data. **E.g MongoDb** 


**WHAT IS A MERN STACK**: MERN Stack is a Javascript Stack that is used for easier and faster deployment of full-stack web applications. MERN Stack comprises of 4 technologies namely: **MongoDB, Express.JS, React.JS and Node.JS** It is designed to make the development process smoother and easier

![Database](https://user-images.githubusercontent.com/68599226/167833544-b26a2ba1-2461-48a2-8f2b-57ff78a9346e.png)


**MEAN STACK CORE COMPONENT**

**MongoDB** – A “NoSQL” database and non-relational document-orientated database used for storing data for a back-end JavaScript application. MongoDB stores data in flexible documents using a query language based on JavaScript Object Notation(JSON). The size, number and content of document fields vary, so the data structure can be altered later on If your application has users, MongoDB is an example of a database where your user information will be kept.

**Express.JS** - A light backend framework for serving content to the web. If your backend application needs to send information across the Internet, Express provides tools for accomplishing that Express’s framework was designed to enable simple, easy construction of APIs and efficient web applications. It is loaded with plugin features and is renowned for its speed. Its minimalistic structure makes it simple for developers to pick up and start using right away.Express.js a layer built on the top of the Node js that helps manage servers and routes.

**React.Js** - Is a front-end /client-side Javascript framework.It is an open-source JavaScript library that is used for building user interfaces specifically for single-page applications. So it lets developers use a full-featured programming language to design conditional or repetitive DOM elements rather than relying on templates that automatically create repetitive DOM (Document Object Model) or HTML elements.  It is  recommend Express. js is used as a backend service

**Node.Js** - NodeJS is a cross-platform and opensource Javascript runtime environment that allows the javascript to be run on the server-side. Nodejs allows Javascript code to run outside the browser. Nodejs comes with a lot of modules and mostly used in web development.Node.JS makes use of Chrome’s V8 JavaScript engine and is intended to allow developers to build scalable network applications and execute JavaScript code outside of browsers. Node.js works by using its own module system that is based on CommonJS, meaning it does not need an enclosing HTML page to put together more than one JavaScript file

![At this point of time,](https://user-images.githubusercontent.com/68599226/167841166-7d6b6e1e-8507-4671-aeb1-9f3fe0a0bcb7.png)
 
## STEP 1

* Spin up an ubuntu server on AWS and select an AMI - Ubuntu 20.04  

![Pasted Graphic 162](https://user-images.githubusercontent.com/68599226/167843835-8ad10de5-1297-4f64-b549-76e292d9a0c9.png)

* Choose instance type

![Pasted Graphic 1](https://user-images.githubusercontent.com/68599226/167844275-26f02188-f824-4796-8341-5cff6523f820.png)

* Configure Instance Details 

![Pasted Graphic 2](https://user-images.githubusercontent.com/68599226/167844632-cb70466e-d6c2-4749-96c6-733737676a52.png)

* Add Storage 

![Pasted Graphic 163](https://user-images.githubusercontent.com/68599226/167844722-fcc62a00-0b97-499b-a0eb-d3ae97ad2ac4.png)

* Add Tags 

![Stop 5 Add Tags](https://user-images.githubusercontent.com/68599226/167844854-d0493f24-1ebc-4a7d-a0bc-6157bc6029aa.png)

* configure Security Group

![Pasted Graphic 165](https://user-images.githubusercontent.com/68599226/167845714-52fac543-4140-4f5c-8756-b7202284dd51.png)

* SSH into our server or local terminal . A link below shows us how to ssh or use our terminal to connect to our server 

## STEP 2 - BACK-END CONFIGURATION 
##### UPDATE & UPGRADE UBUNTU

```
$ sudo apt update
$ sudo apt upgrade
```
##### INSTALL NODE.JS ON THE SERVER 

```
sudo apt-get install -y nodejs
```

The above command if for the installation of node.js and npm. npm is the package manager for the Node JavaScript platform. It puts modules in place so that node can find them, and manages dependency conflicts intelligently. It is extremely configurable to support a wide variety of use cases. Most commonly, it is used to publish, discover, install, and develop node programs.

* The below command is to verify that node.js and npm has been installed 
```
$ node -v

$ npm -v 
```
![Processing triggers for man-db (2 9 1-1)](https://user-images.githubusercontent.com/68599226/167923685-e3f400a3-f97f-4524-af4c-4043e9d0d681.png)

The above is to verify node and npm has been installed 

## STEP 3 - SETTING-UP OUR APPLICATION 
##### CREATE A TODO DIRECTORY AND CD INTO THE DIRECTORY 

```
$ mkdir Todo

$ cd Todo
```
We need to initiate a package called package.json.This file will normally contain information about our app and the dependencies that it needs to run. Follow the prompts after running the command. We can hit enter to accept default values, then we accept to write out the package.json file by typing yes.

```
$ npm init
```
The command above is to initiate the package.json file 

![Pasted Graphic 168](https://user-images.githubusercontent.com/68599226/167927630-b4ab7928-b257-4d65-a739-3855fc9208f0.png)

The above should be the display result we get once we run the npm init 

* So we should have our package.json inside our Todo directory as shown below 

![Pasted Graphic 170](https://user-images.githubusercontent.com/68599226/167928274-6f434c02-58ac-48b3-8c00-8748d08333ba.png)

## STEP 4 - INSTALL EXPRESS.JS 

Express.js is a layer built on the top of the Node.js that helps manage servers and routes.Its a back-end framework for Node.js web applications . Express is a minimal and flexible Node.js web application framework that provides a robust set of features for web and mobile applications.

* Inside the Todo directory , we will install the express.js file using npm

```
$ npm install express
```
* Then we create an index.js file inside Todo directory 

```
$ touch index.js
```
Inside the todo list folder, We will Install the dotenv module

```
$ npm install dotenv
```
Once we ls , we should have the below display of information

![total 28](https://user-images.githubusercontent.com/68599226/167934276-9784d3d0-ede6-406b-b8d3-c23fde06dbf5.png)


* Then we need to populate the index.js file 

```
$ vi index.js 
```
```
const express = require('express');
require('dotenv').config();

const app = express();

const port = process.env.PORT || 5000;

app.use((req, res, next) => {
res.header("Access-Control-Allow-Origin", "\*");
res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
next();
});

app.use((req, res, next) => {
res.send('Welcome to Express');
});

app.listen(port, () => {
console.log(`Server running on port ${port}`)
});
```
* We then test if our server is running

```
node index.js
```
![Pasted Graphic 172](https://user-images.githubusercontent.com/68599226/167935300-c7e51100-f4b0-496e-9156-8598096a4be3.png)

We should have the above display 

We open up port 5000 on our security group on Ec2 ubuntu machine 

![image](https://user-images.githubusercontent.com/68599226/167940802-649db6e7-a4af-42bb-9cc6-058c7c6016af.png)

We select secuity group and edit inbound rule and set to port 5000. We should have the below display 

![image](https://user-images.githubusercontent.com/68599226/167941739-84c21057-1163-4872-9f71-1f0faae057ed.png)

* Then we browse the below Ipaddress

```
ipaddress:5000
```
Our website should look like this 

![image](https://user-images.githubusercontent.com/68599226/167942285-1f9c1165-170f-453d-a50e-ce4b681995af.png)

## Step 5 - Set Routes

**We need to create routes that will define various endpoints that the todo app will depend on.**

So let’s create a folder routes
 
 ```
 $ mkdir routes
 ```
 
Change directory into the routes folder.
 
```
$ cd routes
```

Now, create a file api.js with the command below
 
```
$ touch api.js
```

 
Open the file with the command below

 
```
vi api.js

```

