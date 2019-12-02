# Homework: Full Stack Games Hub App

### Learning Objectives

- Understand the relationship between client, server and database
- Be able to navigate a codebase that you haven't written

## Brief

Your boss has asked to you look over the codebase of a full-stack JavaScript application. The front-end is written in JavaScript using Vue, the back-end uses an Express server and a MongoDB database. Your task is to make yourself familiar with the codebase.

The application includes a README.md with instructions on running the application.

![Overview of the tech stack and tooling with commands](images/tech_stack_with_commands.png)

*Overview of the tech stack and tooling with commands*

## MVP

### Task

Draw a diagram showing the dataflow through the application starting with a form submission, ending with the re-rendering of the page. This will involve a multi-direction data-flow with the client posting data to the server and the server sending data back to the client with the response. Detail the client, server and database in the diagram and include the names of the files involved in the process.

### Questions

1. What is responsible for defining the routes of the `games` resource?

create_router.js

2. What do you notice about the folder structure?  Whats the client responsible for? Whats the server responsible for?

client responsible for client viewing the app
server responsible for serving the data and housing the database


3. What are the the responsibilities of server.js?

connect the database, create the app route


4. What are the responsibilities of the `gamesRouter`?

tell the server to use the gamesRouter by using the use method. The use method takes two arguments:

gamesRouter is the router object we want it to use, to tell the server use express.Router() on



5. What process does the the client (front-end) use to communicate with the server?

in GamesService.js

fetch the data from http://localhost:3000/api/games/


6. What optional second argument does the `fetch` method take? And what is it used for in this application? Hint: See [Using Fetch](https://developer.mozilla.org/en-US/docs/Web/API/Fetch_API/Using_Fetch) on the MDN docs

The fetch() method can optionally accept a second parameter, an init object that allows you to control a number of different settings.



7. Which of the games API routes does the front-end application consume (i.e. make requests to)?

post and delete


8. What are we using the [MongoDB Driver](http://mongodb.github.io/node-mongodb-native/) for?

MongoDB is a document-oriented database. Instead of having tables with columns and rows, it stores data in collections of JSON documents.

MongoDB Driver support for the shared CRUD API specification and the Server Discovery and Monitoring Specification


## Extension

Why do we need to use [`ObjectId`](https://mongodb.github.io/node-mongodb-native/api-bson-generated/objectid.html) from the MongoDB driver?

Because we want it identical

Add to your diagram the dataflow for removing a game.
