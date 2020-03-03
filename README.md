# note_taker

# Description
This is a note taking application that can be used to write, save, and delete notes. Note Taker saves to and retrieves note data from a JSON file and uses an express backend. 

The goal of this application is for users to be able to better organize their thoughts and keep track of tasks that need to be completed.

# How it Works
The application runs on a Heroku server. 

The application has a JSON file on the backend that is used to store and retrieve notes using the fs npm module. 

Utilizes GET, POST, and DELETE routing methods to save, retrieve and delete user's notes.

The GET route reads the JSON file and returns all saved notes as JSON. 

POST route receives a new note to save on the request body, add it to the JSON file, then returns the new note to the client. 
Each note is assigned a unique ID using the .forEach() method and adding 1 to the note's index in the array.

DELETE route receives a query parameter that contains the id of the note that needs to be deleted. Using the .filter() method, a new array is created that contains all the notes that do not have the "to be deleted" ID. The array is then saved to the JSON file using npm fs.writeFileSync and the response is then returned as JSON. 

# Installation
-Open server.js in terminal
-Run command: npm install
-Run command: node server.js
-Open browser 
-Type into search bar: localhost:3000

# Deployed App: 
[Deployed Application](https://secret-meadow-67711.herokuapp.com/)