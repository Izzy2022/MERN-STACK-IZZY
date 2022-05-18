# MERN-STACK-IZZY
  IN THIS PROJECT I AM GOING TO IMPLEMENT A WEB SOLUTION BASED ON MERN-STACK IN AWS

**What is MERN-STACK ?
  The MERN stack is a web development framework made up of the stack of MongoDB, Express.js, React.js, and Nodejs. It is one of the several variants of the MEAN stack
  When you use MERN-STACK, you work with React to implement the presentation layer, Express and Node js are middle layers or the application layer, then MongoDB is to 
  create the database layer
###  Overview of DBMS Types 

**NOSQL DATABASE;

NoSQL DBMSs differ from SQL-based systems in their support for both structured and unstructured data. This allows NoSQL systems to collect and analyze data without requiring a rigidly defined schema. For example, NoSQL databases can process queries of database entities that have different elements, such as social media posts, images, audio and video, in addition to conventional text and numeric data.
It is mostly used for web applications 

**Relational database management system
Relational database management systems (RDBMS) are the most popular data model because of its user-friendly interface. It is based on normalizing data in the rows and columns of the tables. This is a viable option when you need a data storage system that is scalable, flexible, and able to manage lots of information.

understanding the difference between front end(**client-side and back end(server-side)

    CLIENT-SIDE(FRONT END )
  What is the client-server model?
Much of the Internet is based on the client-server model. In this model, user devices communicate via a network with centrally located servers to get the data they need, instead of communicating with each other. End user devices such as laptops, smartphones, and desktop computers are considered to be 'clients' of the servers, as if they were customers obtaining services from a company. Client devices send requests to the servers for webpages or applications, and the servers serve up responses
In web development, 'client side' refers to everything in a web application that is displayed or takes place on the client (end user device). This includes what the user sees, such as text, images, and the rest of the UI, along with any actions that an application performs within the user's browser.

  **SERVER-SIDE (BACK-END)
  Much like with client side, 'server side' means everything that happens on the server, instead of on the client. In the past, nearly all business logic ran on the server side, and this included rendering dynamic webpages, interacting with databases, identity authentication, and push notifications.

     **STEP 2 (IMPLEMETATION PHASE)**
     
     UPDATE UBUNTU 
     
        sudo apt update
     UPGARDE UBUNTU
     
        sudo apt upgarde
        
     Lets get the location of Node.js software from ubuntu repositories
     
        curl -SL https://deb.nodesource.com/setup_12.x | sudo -E bash -
        
        **INSTALL Node.js on the server**
        
              sudo apt-get install -y nodejs
              
          lets  check the version
          
          node -v 
          
        you also need to install the node npm packages 
        
         sudo apt install npm
         
         ** APPLICATION CODE SETUP **
         
         1ST CREATE A DIRECTORY
            mkdir Todo
          go in the directory
          
          cd Todo
          then after download the npm paakages by initialization
          
          npm init
          after this hit enter=== 3x when u get to description give ur description, then enter 5x, once u get to keywords give todo Application 
          author ===izzy 
          After this is goin to ask u to type yes 
          
          then do ls to check for the package created 
            
             package.json 
     ________________________________________________________________________________________
     
     ## STEP 3##
     
     INSTALLING ExpressJS
     
      IT IS THE MIDDLE LAYER OR ALSO THE APPLICATION LAYER. IT HELPS TO DEFINE ROUTES OF YOUR APPLICATION BASED ON HTTP METHODS AND URLS
      
      TO USE Express install it with npm;
      
          $ npm install express
          
       Now create a file index.js with the command below
       
          $ touch index.js
        
      Run ls to confirm that your index.js file was created 
      
        set the environment 
        
        $ npm install dotenv
        
        after this go into the file index.js 
        
       $ vim index.js   ( copy the code amd save it)
       
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
    
    
  now we need to start our server 
  
  Notice that we have specified to use port 5000 in the code. we will need this when we opening our browser
  
  $ node index.js   (this is going to start our server)
  copy ur public_ip:5000    Then you should be able to see your web application 
  
  
          
          
          
          
         
         
        
        
        
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
     
