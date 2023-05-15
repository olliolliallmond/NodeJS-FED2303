## What is a server?
  A server is a software or hardware that accepts and responds to requests made over a network.
  The device that makes the request and receives the response from the server is called a client.

## What is a client? (Specifically, in the context of Web Development)
  Typically, we are refering to the browser. This is becasue the browser is the interface that a user interacts with that initiate requests to the various services/servers.

## What are servers used for?
  All sorts of applications. 'Server' is a generic term, so any time you are making a request for information that is not ohysically on your machine, you are reaching out to a server of some kind that in term performs specifc tasks to deliver what you are requesting from it.

## Can a server reach out to another server?
  Yes server to server communication is a very common thing that you will encounter in the job. It happens everywhere and at all times. Server to server communication is the backbone of what a network is. 
  
### What is a network? 
  A high level description of a network is that is a bunch of servers that communicate with each other to deliver information. 

## What is Node? 
  Node is a runtime that allows you to use JavaScript outside of the browser. Previously Javascript was designed and created for browser interactions and nothing more. So the interpreter that takes javascript from being a high level language and translate it to operations in a lower level language for your computer to execute only existed in the browser. This created a situation where web developers needed to know and work in multiple programming languages to create any meaningful application. Some of those languages are Java, C#, F#, and PHP. So an engineer (Ryan Dahl) who was tired of having to use a bunch of languages to do things ,began to work at using the V8 engine outside of the browser and creating the bindings for lower level languages that were missing. 

## What is a high- / low-level language?
  High-level :: A human-readable language that is highly abstracted away from what a computer understands. 

  Low -level :: A language that your computer understands.

  A high level language is a language that is highly abstracted away from what the computer understands. This is the language that most of yall will program in as the reasons why we have them are to make it simpler to program. No one wants to program in 0's and 1's which is what the computer understands, so we created many languages to extract those interactions. The further away , the higher the level. Typical high level languages are : java, javascript, c#, php, python, r .... Typical low level languages are: C, assembly, rust, cobalt. 

## What is a runtime?
  A piece of software that makes running an application made on a particular programming languages possible.

## What is the V8 engine?
  It’s a highly performant open source program from google that takes in Javascript and turns that into C++, which your computer can then turn into assembly language the physical hardware can run.

## If the V8 engine is built for the web, then what is plugging the holes? 
  For node to actually work, it relies on the help of other lower level libraries. Some of the major ones are libuv which provides support of the particular features of Javascript that makes it unique such as the event loop which is the backbone of Input/ Output operations to be non-blocking.
  Key terms: libuv, input/output (I/O) operations, non-blocking

## What can Node be used for?
  Pretty much anything that your mind can create. Remember node is a runtime. Its only job is to allow you to run JavaScript outside of the browser. It doesn’t care what kind of application you are making. Typical applications that are created in node are backend APIs, web scrapping bots, cron jobs, webhooks, lambda cloud functions, etc...

  ** backend APIs : 
    In web development this is a program that a client communicates with in order to get information of some kind (typically from a database). This is a predetermine set of exposed communication points that we typically call endpoints. These endpoints have only 1 way of interaction. This is known as a contract/ JSON contract. This way many programs can reach out to these endpoints and all get the expected result. 
    
    Key terms: endpoints, contracts

  ** web scrapping bots : 
    These are scripts/ programs that are designed to go to a particular site on the web and retrieve or automatically enter information to/from the site. This is how there are applications that archive sites. 
  ** cron-jobs : 
    These are scripts that do background work typically on a predefined schedule. They are set up in a way to be autonomous. 
  ** Webhooks : 
    similar to api endpoints but typically used for integrations with 3rd party systems.
  ** lambda cloud functions: 
    Severless functions that run in the cloud

## RESTful API
  RESTful APIs are server data layers that are built on a predefine architecture that implements REST principals and must employ HTTP/ HTTPS protocals. WS protocals are not required in a REST api but can also be implemented alongside. 
  
  Note: WS protocals - touch on later

## What should we know about Node as a frontend engineer?
  One of the most popular ways to deliver our production applications to the client. The other way is with an NGINX server. However in many places , they leave those for non-web applications because they are able to leverage the learned knowledge of JavaScript that a frontend engineer has in order to quickly get things out by using node. 

## What does this actually mean?
  Frontend applications are most commonly minified into what is called a production static build. This is typically found in the build or public folder of an application. It takes your pretty code and makes it gibberish to read in order to make it smaller package size. Meaning less memory usage. 
  -Its also used for moving expensive operations out of the client. These are things like file validations, authentication loops, file conversions, text-to-speech conversations ..... Etc 

## Typical authentication steps that frontend developers should know: 
  • Most applications use cookies and JWT (JSON WEB TOKEN) in order to validate if a frontend client is a valid user. The creation of this is not a concern of the frontend nor is the actual validation to know if they are a real client or not, but the stopping of accessing routes in the frontend is the concern that needs to be addressed by the frontend. 
	○  Step 1: 
    In your server you need to find the routes that you are protecting and check the headers typically for the authentication cookie or jwt, If not in the headers it typically is sent via the cookie property in the request object. 
	○  Step 2: 
    if Its expired or not there , redirect the user to the exposed endpoint that backend is going to use for authentication purposes. 
	○  Step 3 : 
    user will be redirected back to entry point after being authenticated. 
	○  Step 4 : 
    check if authenticated and serve the frontend index.html 

# Minimum Knowledge of Node :
  • Understand what is an environment property (will be similar in the frontend portion) 
	• Understand request and response interfaces 
	• Understand routing and endpoints 
	• Understand middleware 
	• Understand the importance of ending a connection 
	• Surface level understanding of authentication 
	• Typical REST api structure/architecture 

## What is GIT? 
  Git is a program that allows us to have version control on our applications. What this means, is that it creates save points for your application (known as commits) which are a snapshot of what your code is at that time. Each commit has a message associated to it that you set as a visual way to understand what that savepoint is and it generates a unique hash as an id for that endpoint.

  https://www.youtube.com/watch?v=8JJ101D3knE&t=704s
  https://university.atlassian.com/student/catalog/
  https://programmingwithmosh.com/wp-content/uploads/2020/09/Git-Cheat-Sheet.pdf
  

