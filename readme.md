# Express Geocoding and Maps

## Setup

* Fork and clone this repository
* Run `npm install` to install packages
* Create a database for this app (see `config/config.json` for name of database)
* Run sequelize migrations (`sequelize db:migrate`)
* Run the app using `nodemon`
* View the site in your browser, read the code.

## Questions

You are modifying an existing application. First, you must get familiar with what the application currently does.

1. What modules/middleware does this application use? Describe what each one does.
    1. express This is a "Fast, unopinionated, minimalist web framework for node."
    2. body-parser This "Parses incoming request bodies"
    3. express-ejs-layouts "Layout support for ejs in express"
    4. db - './models' Tells sequelize to use the ./models folder contents for table definitions
    5. rowdy-logger Prints the app's methods and paths/routes to the console
    6. morgan "HTTP request logger middleware for node.js"
2. What are the routes for the website? Describe what each one does.
  * Verb + Route?
  * Interaction with database?
  * Response to browser?

  Verb: GET Route: /
  Database interaction: findall place rows in the database
  Response to browser: Renders index.ejs, which displays a form to enter a place on the database and shows each place name & map.

  Verb: POST Route: /places
  Database interaction: Creates a row in the database containing name and address entered on the form.
  Response to browser: Redirects browser back to root ('/'), which then displays the form and the database contents.

3. What does the site do right now?
  It adds rows/records to the place table in the database and displays the place name to the user.

4. What features need to be added?
  It needs to display the map of the place to the user.

## Task

See [this page](https://wdi_sea.gitbooks.io/notes/content/05-express/additional-topics/express-geocode/readme.html)

---

## Licensing
1. All content is licensed under a CC-BY-NC-SA 4.0 license.
2. All software code is licensed under GNU GPLv3. For commercial use or alternative licensing, please contact legal@ga.co.
