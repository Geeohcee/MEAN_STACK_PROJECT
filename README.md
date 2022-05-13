# MEAN_STACK_PROJECT

### What is a Tech Stack ?
**A Tech stack comprises of the many components which work together to produce an application which serves the needs of users and businesses. This comprises of** |Front-end framework|Back-end framework|Database technologiees|
1. **Front-end framework** does most of the “heavy lifting” of building a complex website or mobile app, so the developers and designers can focus on providing the specific features and fixes needed by the users and the business. **E.g React.js** 
2. **Back-end framework** does most of the “heavy lifting” of communication between the website or mobile app and the database and business logic. **E.g Express.js** 
3. **Database technologies** store and organize data, as well as provide features for searching, filtering, and reporting data. **E.g MongoDb** 


**WHAT IS A MERN STACK ?**

The MERN stack is an amalgamation of four technologies **MongoDB, Express.JS, React.JS and Node.JS** . This combination allows developers to create complete websites (back-end and front-end). With the MERN stack, we use JavaScript on the client side and Node.js on the server side. The MERN stack was created to give full stack developers the ability to develop a site from start to finish, without having to know or use another skill.
Developers can thus create a website or a web application from start to finish, and can manage both the front-end and the back-end. The MERN stack provides the possibility of mastering both the algorithmic and logical part of the backend, as well as the design, the user experience and animation components of the front end part.This translates into recruitment savings for companies that can have a single developer do work that commonly requires two.The MERN stack represents an alliance of the most powerful technologies on the market.

![Database](https://user-images.githubusercontent.com/68599226/167833544-b26a2ba1-2461-48a2-8f2b-57ff78a9346e.png)


**MEAN STACK CORE COMPONENT**

**MongoDB** – A “NoSQL” database and non-relational document-orientated database used for storing data for a back-end JavaScript application. MongoDB allows you to manage databases. It differs from SQL. MongoDB is used in the MEAN stack because the data is manipulated in JSON format. It is also really simple to transform JavaScript data into MongoDB and vice versa, thanks to libraries such as mongoose, for example. Data manipulation becomes child’s play, with efficiency and simplicity.

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

**Routes help the frontend application to interact with the backend at multiple endpoints. You can create these endpoints and wire them to a function that does a particular task.**

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
* We populate the api.js file with below code 

```
const express = require ('express');
const router = express.Router();

router.get('/todos', (req, res, next) => {

});

router.post('/todos', (req, res, next) => {

});

router.delete('/todos/:id', (req, res, next) => {

})

module.exports = router;
```

## Step 6 - CREATE MODELS
Models Provide Clean Interface to interact with your MongoDB database through moongoose library. To install mongoose , we have to be in home directory 
```
$ npm install mongoose
```
![Pasted Graphic 173](https://user-images.githubusercontent.com/68599226/168035058-562f28d4-6c27-4dfd-9276-ced289241a33.png)

* We then create a model directory 

```
$ mkdir models 
```
* Inside the model directory , we create a todo.js

```
$ touch todo.js
```
We vi into the todo.js file and paste the below command

```
const mongoose = require('mongoose');
const Schema = mongoose.Schema;

//create schema for todo
const TodoSchema = new Schema({
action: {
type: String,
required: [true, 'The todo text field is required']
}
})

//create model for todo
const Todo = mongoose.model('todo', TodoSchema);

module.exports = Todo;
```
Now we need to update our routes from the file api.js in Routes directory to make use of the new model.

In Routes directory, open api.js with vi api.js, delete the code inside with :%d and paste the code below into it then save and exit

```
$ vi api.js
```
```
const express = require ('express');
const router = express.Router();
const Todo = require('../models/todo');

router.get('/todos', (req, res, next) => {

//this will return all the data, exposing only the id and action field to the client
Todo.find({}, 'action')
.then(data => res.json(data))
.catch(next)
});

router.post('/todos', (req, res, next) => {
if(req.body.action){
Todo.create(req.body)
.then(data => res.json(data))
.catch(next)
}else {
res.json({
error: "The input field is empty"
})
}
});

router.delete('/todos/:id', (req, res, next) => {
Todo.findOneAndDelete({"_id": req.params.id})
.then(data => res.json(data))
.catch(next)
})

module.exports = router;

```
## Step 7 - SETTING UP MONGODB DATABASE

We need to set-up a database where our data can be stored. We will make use of mLab. mLab is a fully managed cloud database service that hosts MongoDB databases. mLab runs on cloud providers Amazon, Google, and Microsoft Azure, and has partnered with platform-as-a-service providers.

In order to allow the node.js to connect to the database in Mongodb, the index.js was updated so as to reflect the use of dotenv. We setup the dotenv file in our Todo directory 

```
touch .env
vi .env
```
The index.js needs to be uodated so as to reflect the use of .This will allow the  Node.js to  connect to the database. We delete the existing content in the index. js and past the below command. To delete the entire content on our editor , we input the following **:%d**. This will delete the entire content on on the index.js file .

* To do this , we  use the  vi command , we open the file with vi index.js and paste the below code 

```
const express = require('express');
const bodyParser = require('body-parser');
const mongoose = require('mongoose');
const routes = require('./routes/api');
const path = require('path');
require('dotenv').config();

const app = express();

const port = process.env.PORT || 5000;

//connect to the database
mongoose.connect(process.env.DB, { useNewUrlParser: true, useUnifiedTopology: true })
.then(() => console.log(`Database connected successfully`))
.catch(err => console.log(err));

//since mongoose promise is depreciated, we overide it with node's promise
mongoose.Promise = global.Promise;

app.use((req, res, next) => {
res.header("Access-Control-Allow-Origin", "\*");
res.header("Access-Control-Allow-Headers", "Origin, X-Requested-With, Content-Type, Accept");
next();
});

app.use(bodyParser.json());

app.use('/api', routes);

app.use((err, req, res, next) => {
console.log(err);
next();
});

app.listen(port, () => {
console.log(`Server running on port ${port}`)
});
```
* Then we restart our server 
```
node index.js
```
![image](https://user-images.githubusercontent.com/68599226/168261330-86e01827-3d4a-46aa-a31e-7b86892e7ce9.png)

## Step 8 - BACK-END TESTING USING RESTFULAPI
We have written the back-end part of our Todo apllication and completed the database. We are yet to complete the front-end UI part. We will make use of react.js to complete this task. We also need to test our back-end code using restfulapi . We will make use of an api application called **Postman**. We will use postman to test our API . 

To install Postman in Ubuntu
```
$ sudo snap install postman
```
![image](https://user-images.githubusercontent.com/68599226/168271446-7038618c-8b42-43b5-bfb0-766e124cd3a9.png)

* To open postman application  

http://ipaddress:5000/api/todos


## Step 9 - CREATING FRONT-END USING REACT.JS 

In our Todo directory , we run the below command to create a react app client file  . The react client file . This contains all the react code and dependecies  allows us create an interface for the client to interact with the api. 
```
$ npx create-react-app client
```
![image](https://user-images.githubusercontent.com/68599226/168273542-4b116d69-c772-44b1-a977-febe4bb80b0a.png)

* We then run the react application ,but before we run the appliction , we need to install some dependecies such as **concurrently**: It is used to run more than one command simultaneously from the same terminal window and **nodemon:** It is used to run and monitor the server. If there is any change in the server code, nodemon will restart it automatically and load the new changes.
```
$ npm install concurrently --save-dev

```
![image](https://user-images.githubusercontent.com/68599226/168275378-11750787-9155-431b-be4f-877d7a2c9ffa.png)

```
$ npm install nodemon --save-dev
```
![image](https://user-images.githubusercontent.com/68599226/168275443-701f3261-bdb6-4a00-ae2e-d032f76ee435.png)

In the Todo folder, open the package.json file. Change the highlighted part of the below screenshot and replace with the code below.

```
"scripts": {
"start": "node index.js",
"start-watch": "nodemon index.js",
"dev": "concurrently \"npm run start-watch\" \"cd client && npm start\""
},
```

## CONFIGURATION OF PACKAGE.JSON FILE 

From our Todo directory, we cd into or client directory , vi package.json
```
$ cd client

$ cd package.json
```
<img width="515" alt="npm concurrently" src="https://user-images.githubusercontent.com/85270361/129056821-01af0741-d626-4d7e-bcd8-5b5440471d35.PNG">


 
 
* We need to Install nodemon: It is used to run and monitor the server. If there is any change in the server code, nodemon will restart it automatically and load the new changes.
 
```
$ npm install nodemon --save-dev
```
 
<img width="472" alt="npm step 8 b" src="https://user-images.githubusercontent.com/85270361/128703906-9d6b9396-3fb1-436e-a5a0-36f1b408d570.PNG">
 
 
* In the Todo folder, open the package.json file. Change the highlighted part of the below screenshot and replace with the code below.

 
```
"scripts": {
"start": "node index.js",
"start-watch": "nodemon index.js",
"dev": "concurrently \"npm run start-watch\" \"cd client && npm start\""
},
```
 
# Step 11 - Configure Proxy in package.json
 
* Enter into the client folder from Todo directory

```
$ cd client
```
 
* Open the package.json file
 
```
$ vi package.json
```
 
* Add the key value pair in the package.json file "proxy": "http://localhost:5000".
 
<img width="476" alt="step 11" src="https://user-images.githubusercontent.com/85270361/129058009-b4eaadd2-6294-4935-adae-cc0eb073652d.PNG">
 
 
The whole purpose of adding the proxy configuration in number 3 above is to make it possible to access the application directly from the browser by simply calling the server url like http://localhost:5000 rather than always including the entire path like http://localhost:5000/api/todos
 

 
 
# Now, we will ensure that we are inside the Todo directory, and simply do:
 
 
```
$  npm run dev
```

<img width="433" alt="npm step 8 c" src="https://user-images.githubusercontent.com/85270361/128741447-c1bea91c-6e3e-42df-b76e-541be8aeb5c8.PNG">
 
 
**Your app should open and start running on localhost:3000
 
<img width="488" alt="src" src="https://user-images.githubusercontent.com/85270361/128741793-7e95cd22-9188-4844-b4a1-fa5aed82c2d1.PNG">


Important note: In order to be able to access the application from the Internet you have to open TCP port 3000 on EC2 by adding a new Security Group rule. You already know how to do it.

 
# Step 12 - Creating our React Components 
 
Creating your React Components
One of the advantages of react is that it makes use of components, which are reusable and also makes code modular. For our Todo app, there will be two stateful components and one stateless component. From your Todo directory run
 
 
```
cd client
```
 
**Move to the src directory**
 
```
cd src
```
 
**Inside your src folder create another folder called components**
 
 
```
mkdir components
```

**Move into the components directory with 

 ```
 cd components
 ```
 
Inside ‘components’ directory create three files Input.js, ListTodo.js and Todo.js.
 
**touch Input.js ListTodo.js Todo.js**
 

Open Input.js file

```
vi Input.js
```
 
**Copy and paste the following**

```
import React, { Component } from 'react';
import axios from 'axios';

class Input extends Component {

state = {
action: ""
}

addTodo = () => {
const task = {action: this.state.action}

    if(task.action && task.action.length > 0){
      axios.post('/api/todos', task)
        .then(res => {
          if(res.data){
            this.props.getTodos();
            this.setState({action: ""})
          }
        })
        .catch(err => console.log(err))
    }else {
      console.log('input field required')
    }

}

handleChange = (e) => {
this.setState({
action: e.target.value
})
}

render() {
let { action } = this.state;
return (
<div>
<input type="text" onChange={this.handleChange} value={action} />
<button onClick={this.addTodo}>add todo</button>
</div>
)
}
}

export default Input
```

 
Axios is a promise based HTTP client for the browser and node.js, you need to cd into your client from your terminal and run yarn add axios or npm install axios.
 
 
* Move to the src folder
 
```
$ cd ..
```
 
* Move to clients folder
 
```
$ cd ..
```
 
 
**Install Axios in the clients folder**
 
```
$ npm install axios
```
 

* Go to components directory
 
```
$ cd src/components
```
 
 
* After that open your ListTodo.js
 
```
$ vi ListTodo.js
```

* In the ListTodo.js copy and paste the following code
 
```
import React from 'react';

const ListTodo = ({ todos, deleteTodo }) => {

return (
<ul>
{
todos &&
todos.length > 0 ?
(
todos.map(todo => {
return (
<li key={todo._id} onClick={() => deleteTodo(todo._id)}>{todo.action}</li>
)
})
)
:
(
<li>No todo(s) left</li>
)
}
</ul>
)
}

export default ListTodo
```
 
* **Then in your Todo.js file you write the following code**
 
```
import React, {Component} from 'react';
import axios from 'axios';

import Input from './Input';
import ListTodo from './ListTodo';

class Todo extends Component {

state = {
todos: []
}

componentDidMount(){
this.getTodos();
}

getTodos = () => {
axios.get('/api/todos')
.then(res => {
if(res.data){
this.setState({
todos: res.data
})
}
})
.catch(err => console.log(err))
}

deleteTodo = (id) => {

    axios.delete(`/api/todos/${id}`)
      .then(res => {
        if(res.data){
          this.getTodos()
        }
      })
      .catch(err => console.log(err))

}

render() {
let { todos } = this.state;

    return(
      <div>
        <h1>My Todo(s)</h1>
        <Input getTodos={this.getTodos}/>
        <ListTodo todos={todos} deleteTodo={this.deleteTodo}/>
      </div>
    )

}
}

export default Todo;
```
 


**We need to make little adjustment to our react code. Delete the logo and adjust our App.js to look like this.**

* Move to the src folder

 
```
cd ..
```
 
 
* **Make sure that you are in the src folder and run**

 
```
vi App.js
```
 
 
**Copy and paste the code below into it**
 
 
``` 
import React from 'react';

import Todo from './components/Todo';
import './App.css';

const App = () => {
return (
<div className="App">
<Todo />
</div>
);
}

export default App;
```
 
 
**After pasting, exit the editor.**

* In the src directory open the App.css 
 
 
```
vi App.css
```
 
 
**Then paste the following code into App.css:**
 
 
```
.App {
text-align: center;
font-size: calc(10px + 2vmin);
width: 60%;
margin-left: auto;
margin-right: auto;
}

input {
height: 40px;
width: 50%;
border: none;
border-bottom: 2px #101113 solid;
background: none;
font-size: 1.5rem;
color: #787a80;
}

input:focus {
outline: none;
}

button {
width: 25%;
height: 45px;
border: none;
margin-left: 10px;
font-size: 25px;
background: #101113;
border-radius: 5px;
color: #787a80;
cursor: pointer;
}

button:focus {
outline: none;
}

ul {
list-style: none;
text-align: left;
padding: 15px;
background: #171a1f;
border-radius: 5px;
}

li {
padding: 15px;
font-size: 1.5rem;
margin-bottom: 15px;
background: #282c34;
border-radius: 5px;
overflow-wrap: break-word;
cursor: pointer;
}

@media only screen and (min-width: 300px) {
.App {
width: 80%;
}

input {
width: 100%
}

button {
width: 100%;
margin-top: 15px;
margin-left: 0;
}
}

@media only screen and (min-width: 640px) {
.App {
width: 60%;
}

input {
width: 50%;
}

button {
width: 30%;
margin-left: 10px;
margin-top: 0;
}
}
```
 
 
 
## Exit
 

* In the src directory open the index.css

 
```
vim index.css
```
 
 
**Copy and paste the code below:**
 
 
```
body {
margin: 0;
padding: 0;
font-family: -apple-system, BlinkMacSystemFont, "Segoe UI", "Roboto", "Oxygen",
"Ubuntu", "Cantarell", "Fira Sans", "Droid Sans", "Helvetica Neue",
sans-serif;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
box-sizing: border-box;
background-color: #282c34;
color: #787a80;
}

code {
font-family: source-code-pro, Menlo, Monaco, Consolas, "Courier New",
monospace;
}
```
 
 
**Go to the Todo directory**

 
```
cd ../..
```
 

When you are in the Todo directory run:


```
npm run dev
```
 
 
Assuming no errors when saving all these files, our To-Do app should be ready and fully functional with the functionality discussed earlier: creating a task, deleting a task and viewing all your tasks.
 
 
 
![image](https://user-images.githubusercontent.com/85270361/129060343-05d73c7c-8718-4725-8fc7-5e5353c09328.png)


