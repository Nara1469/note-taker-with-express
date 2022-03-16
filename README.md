# note-taker-with-express
Bootcamp Week 11: Homework
# 11 Express.js: Note Taker

## Table of Contents 

- [About Task](#about-task)
- [User Story](#user-story)
- [Installation Guide](#installation-guide)
- [My Solution](#my-solution)
- [Samples](#samples)
- [Live](#live)
- [Questions](#questions)

## About Task

This assignment is to modify starter code to create an application called Note Taker that can be used to write and save notes. This application will use an Express.js back end and will save and retrieve note data from a JSON file. My task is to build the back end, connect the two, and then deploy the entire application to Heroku.

> **Note**: The application’s front end was done. 

## User Story

```
AS A small business owner
I WANT to be able to write and save notes
SO THAT I can organize my thoughts and keep track of tasks I need to complete
```

## Installation Guide

This application uses Express.js to build up the back end. It is required to install all necessary dependencies.

First clone the repository then run the following command at the root directory to install the dependencies:

```
npm i
```
    
The application will be invoked by using the following command:
    
```
node server.js
```

A directory structure looks like in the following way:

```
.
├── __db__/                
│   └── db.json                 // db - an array of objects saves notes
├── __helpers__/            
│   ├── fsUtils.js              // module reads, writes and appends file
│   └── uuid.js                 // module creates a random id 
├── __public__/                 // frond end
|   ├── __assets__/            
│   |      ├── css/style.css    
│   |      └── js/index.js       
│   ├── index.html              // homepage
│   └── notes.html              
├── __routes__/            
│   ├── index.js                // default route
│   └── notes.js                // end route: /api/notes 
├── .gitignore                  // indicates which folders and files Git should ignore
└── package.json   
└── README.md           
└── server.js                   // runs the application
```

## My Solution

```
GIVEN a note-taking application
WHEN I open the Note Taker
THEN I am presented with a landing page with a link to a notes page
WHEN I click on the link to the notes page
THEN I am presented with a page with existing notes listed in the left-hand column, plus empty fields to enter a new note title and the note’s text in the right-hand column
WHEN I enter a new note title and the note’s text
THEN a Save icon appears in the navigation at the top of the page
WHEN I click on the Save icon
THEN the new note I have entered is saved and appears in the left-hand column with the other existing notes
WHEN I click on an existing note in the list in the left-hand column
THEN that note appears in the right-hand column
WHEN I click on the Write icon in the navigation at the top of the page
THEN I am presented with empty fields to enter a new note title and the note’s text in the right-hand column
```

## Getting Started

On the back end, the application should include a `db.json` file that will be used to store and retrieve notes using the `fs` module.

The following HTML routes should be created:

* `GET /notes` should return the `notes.html` file.

* `GET *` should return the `index.html` file.

The following API routes should be created:

* `GET /api/notes` should read the `db.json` file and return all saved notes as JSON.

* `POST /api/notes` should receive a new note to save on the request body, add it to the `db.json` file, and then return the new note to the client. You'll need to find a way to give each note a unique id when it's saved (look into npm packages that could do this for you).


## Bonus

You haven’t learned how to handle DELETE requests, but this application offers that functionality on the front end. As a bonus, try to add the DELETE route to the application using the following guideline:

* `DELETE /api/notes/:id` should receive a query parameter that contains the id of a note to delete. To delete a note, you'll need to read all notes from the `db.json` file, remove the note with the given `id` property, and then rewrite the notes to the `db.json` file.

### Screenshots 

The following image shows the deployed HTML’s appearance: ![Heroku](./helpers/note-taker-application-heroku.png)

## Live

This application is deployed to Heroku.com. Here is a link to the deployed website. [Heroku](https://desolate-temple-31076.herokuapp.com/notes)

## Questions

If you have any questions about the repo, open an issue or contact me directly at naraamtm@gmail.com. Here is a link to this application repo on [Github](https://github.com/Nara1469/note-taker-with-express).
