<p align="center">
  <img src="https://github.com/Honey20103/BrewMaster/blob/master/homebrew_app/project/static/images/brewmaster3.1.png" style="margin: 0;" width="300" height="200" >
</p>

# myGreenfriends

[![Build Status](https://travis-ci.com/Honey20103/mygreenfriends.svg?branch=master)](https://travis-ci.com/Honey20103/mygreenfriends)
[![Conventional Commits](https://img.shields.io/badge/Conventional%20Commits-1.0.0-yellow.svg)](https://conventionalcommits.org)


This is a place for every and all that want to be closer to the world of green. On this myGreenfriends e-commerce website I share plants, plantastic stories, info and tell one or two jokes. 
The e-commerce website is developed for the actual plants I have in my private home. The main goal of the website will provide users the ability to browse through different plants found in my home and have the ability to purchase them. This might scale into an actual plant store in the future.

The website will consist of a login page, a signup page and a main page displaying the plants available to buy. Once a product is added to the users basket, they will be able to purchase by entering delivery and payment details. User profile will allow the user to view a history of their purchases. Creating an account will allow customer to change their passwords and registered addresses. 

This website is built with Django(a high-level Python Web framework) and Stripe (a payment processing platform) to provide a fully functional e-commerce website.

If you would like to test the payment functionality of this project, please use the following payment details:

Card number: 9696 9696 9696 9696
CVC: any 3 digit number
Expiration Date: any future date
Address: any address details
To test the site as a superuser, you can use the following credentials to login:

Username: supertester
Password: Testing123123


***

### Website

<img src= "https://github.com/Honey20103/BrewMaster/blob/master/homebrew_app/project/static/images/multimockup.png" style="margin: 0;">


A live demo can be found [here](https://brewmaster-app.herokuapp.com/)

***

## Table of Contents
  * [UX](#ux)
  * [User stories](#user-stories)
    + [Strategy](#strategy)
    + [Scope](#scope)
    + [Structure](#structure)
    + [Skeleton](#skeleton)
    + [Surface](#surface)
  * [Technologies](#technologies)
    + [JavaScript Libraries](#javascript-libraries)
    + [Python & Django Plugins](#python---django-plugins)
  * [Features](#features)
    + [Features Left to Implement](#features-left-to-implement)
  * [Testing](#testing)
  * [Bugs](#bugs)
    + [CSS](#css)
    + [JavaScript](#javascript)
    + [Admin login gave a 500 error](#admin-login-gave-a-500-error)
  * [Deployment](#deployment)
    + [Deploy requirements](#deploy-requirements)
    + [Local deployment](#local-deployment)
    + [Heroku deployment](#heroku-deployment)
  * [Credits](#credits)
    + [Content](#content)
    + [Media](#media)
    + [Acknowledgements](#acknowledgements)
    
## UX

### User stories
- As an amateur homebrewer, it is important to take a record of the entire process of brew day,
to learn from my previous mistakes and help improve my future batches.

- I often record my brew day notes or logs on a physical notebook, or sometimes the closest paper I
can find, and in some cases, I lose it and there goes my brew record, no recollection of what was done.

- As a fairly confident home brewer, I need an application to store my recipes and eventually start a microbrewery or make a profit from my homemade recipes.

- I am quite new to brewing, and I often make mistakes and need to change things in my notes, my notebook ends up looking like a child's scrapbook. Having a digital notebook will help with keeping my notes neat and easily editable.

- As a user I would like to be able to see other brewer's processes, mistakes and results to improve my brewing techniques.

- Beer brewing is quite an expensive hobby, having to view other brewers recipes saves me the need to buy brew recipes from companies.

- I'd like the ability to rate the different brew recipes I make, to know which ones to repeat.

- As a user, I can view all brew recipe logs, with information such as the date of the log.

- As a user, I can search for recipes/logs.

- As a user, I can add new brew logs to the database.

- As a user, I can edit existing recipes/logs.

- As a user, I can add new ingredients not available in the database.

- As a user, I can delete recipes.

- As a user, I can create an account.

- As a user, I can log in to my account.

- As a user, I can log out.

- As a brewer, I would like to update a recipe/log by uploading a photo of the final result of my beer at the end of the process.



### Strategy
My goal in the design was to make it as easy as possible for users to log their brew day process and log the recipes, to have a clean look with no clutter or information overload by having a user-friendly and minimalistic design.

### Scope
For the users, I wanted to provide them with a functional platform to keep their brew records, lessen the burden of log keeping on physical notebooks and eventually serve as recipe storage. 

The scope has full CRUD functionality for logs.

* A landing page that acts as a brewing diary, showing all logs recorded by the user.
* A 'Log' page that displays the recipe and process of the beer they made.
* A 'Add log' page that allows the user to add new log into their brewing diary/database.
* An 'Edit log' page that allows the user to update and then saves to the database.
* Ability to Create an account and store account in database
* Functionality to login and log out of user dashboard/profile

### Structure


### Skeleton

Initial wireframes were done on paper and pen, I'll probably at a later stage add a design made in Balsamic, it was a bit challenging to figure out how I wanted the UX to be, although my idea was to maintain a clean and minimalistic look, and easy to use. The look and feel are intentionally planned for mobile and desktop.

### Wireframes

[Home Page](https://github.com/Honey20103/BrewMaster/blob/master/wireframes/homepage.png)

[Login Page](https://github.com/Honey20103/BrewMaster/blob/master/wireframes/loginpage.png)

[Brew Log Page](https://github.com/Honey20103/BrewMaster/blob/master/wireframes/logpage.png)

### Database Schema

Choose to work with both relational and non-relational databases namely SQLite3 and MongoDB. I used MongoBD for the brew data forms as its schema-less and  presents a clean document option JSON style documents. It seemed suitable for this use case of a diary log. As for the SQLite DB i chose to use it to test out working with a relational and the benefits of it being lightweight in terms of setup and database administration(no actual server or configurations required) and it fit my needs to be able to create to a database to store user info and fetch altogether, which would be advantageous when it comes to mobile devices considering the database is integrated with the app, meaning less lag(mobile first approach).

<img src="https://github.com/Honey20103/BrewMaster/blob/master/homebrew_app/project/static/images/database_schema.png" style="margin: 0;" >


### Surface
My idea for the design is to have colour relating to beer such as brown, gold, orange or essentially brown theme colour palette, this will help users associate with the act of beer brewing.

<img src="https://github.com/Honey20103/BrewMaster/blob/master/wireframes/themecolor1.png" style="margin: 0;" width="600" height="250" >




***

## Features

### Existing Features

* **User Accounts** - Signup for an account, log-in and log-out.
* **Log/Recipe page** - When a recipe or brew log is selected the user will be presented with the page for that recipe. 
* **Add Log/Recipe** - The user can go to the menu and open the add log brew day page, providing the user with a diary or digital like a notebook to log their brew day content and add them to the database.
* **Add Ingredient** - Ingredient options will be available however if an option is not found, the user can add a new ingredient to the database.
* **Edit & Delete ingredients** - Ability for the user to edit and delete ingredients.
* **Multiple users login** - Ability to have more profiles for multiple beer brewers to log their recipes.
* **View ther brewers logs** - Ability for brewers to unhide or unlock certain logs to be publicly visible to other brewers on the app.

### Future Features

- **Social sharing buttons**: Users will be able to share beer recipes to their social media channels via the social sharing buttons provided. 
- **Brew Images** Ability to add/update a log by adding an image or images of the final brew result.
- **Log order arrangement**List logs in dashboard according to date of brew and not when entered.
- **Rating system** - The ability to star rate favourite brew day recipe
- **Database per user login** -  Have separate DB for each user, prevent other users deleting or viewing logs

***

## Technologies Used

### Frontend

* [HTML](https://en.wikipedia.org/wiki/HTML)
* [CSS](https://en.wikipedia.org/wiki/Cascading_Style_Sheets)
* [Bootstrap](https://getbootstrap.com/)
* [Materialize](https://materializecss.com/)
* [Bulma](https://bulma.io/)


### Backend

* [Python](https://www.python.org/)
* [JavaScript](https://en.wikipedia.org/wiki/JavaScript)
* [MongoDB](https://www.mongodb.com/)
* [SQLite3](https://sqlite.org/)
* [Flask](https://flask.palletsprojects.com/en/1.1.x/)
* [Flask-PyMongo](https://pypi.org/project/Flask-PyMongo/)
* [SQLAlchemy](https://www.sqlalchemy.org/)

### Deployed

* [Heroku](https://www.heroku.com/)

***

## Testing

#### Code Validation

#### Devices used to Test

The BrewMaster App was test with the following devices:

MacBook Pro Laptop
HP Pavilion Laptop
Samsung Galaxy S9 Mobile
iPhone XS Max

Google Chrome
Microsoft Edge
Mozilla Firefox

Experience for mobile devices when it pertains to the homepage was not responsive to section/column of the image.(FIXED)

#### User Story Testing

The full user story testing can be found [here](https://github.com/Honey20103/BrewMaster/blob/master/wireframes/BrewMaster%20User%20Story%20Testing.pdf).

* Feedback from Users;
  - The add log form seemed to have been allowing creation of log with empty fields. (FIXED)
  - The datepicker doesn't require an entry to submit form. (Attempted to fix this with a js script however submit button becomes unfunctional, thus was unable to fix this issu, however Date field shows red if empty)

#### [Web Accessibility](https://www.webaccessibility.com/)

<img src="https://github.com/Honey20103/BrewMaster/blob/master/wireframes/webaccessibility.png" style="margin: 0;" >


#### Chrome Developer Tools and Gitpod vscode
Constantly used to ensure the app is mobile-first, and works well with all kinds of devices and provide real-time ability to identify errors in my HTML code, and helped me troubleshoot my HTML/CSS.

Gitpod terminal providing lint issues and problems when it comes to the different scripts/languages.

Further more for css testing I used this [site](http://csslint.net/) no errors found except warnings that informed that for IE6,IE7,IE8 I require fallback colors color: rgba(65, 48, 13, 0.959); I have made relevant changes to ommit this warning.

Used the DOM to detect how to properly fix issue with Fade in Overlay CSS hover effect not functioning well for mobile devices, and inserted necesarry media queries in CSS to fix the issue, the text now no longer overlaps the image background when size decreases.

[W3C CSS Validator](https://jigsaw.w3.org/) reported 14 errors.

HTML valid according to [site](https://validator.w3.org/nu/?doc=https%3A%2F%2Fbrewmaster-app.herokuapp.com%2F)

#### Random User Testing
Sent the app to boyfriend and colleagues to use, collecting their feedback for bug fixes and adjustments.

#### Python Testing
I used [PEP8online](http://pep8online.com/) together with gitpod Problem tab to observe errors and warnings. At the moment errors have been fixed, only warnings exist naming the warning "line too long"

#### JS Testing
Test any javascript errors with jslint [site](http://www.jslint.com/) no error apart from lint warning and too long empty spaces, i've removed those.

#### MongoDB Testing

Test mongoDB connection with the command 'mongod'

```brew
gitpod /workspace/BrewMaster/homebrew_app $ mongod
2020-10-02T00:26:15.526+0000 I CONTROL  [main] Automatically disabling TLS 1.0, to force-enable TLS 1.0 specify --sslDisabledProtocols 'none'
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] MongoDB starting : pid=58337 port=27017 dbpath=/data/db 64-bit host=ws-0567368c-beaf-4649-ab50-f1f1a84e5304
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] db version v4.0.20
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] git version: e2416422da84a0b63cde2397d60b521758b56d1b
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] OpenSSL version: OpenSSL 1.1.1d  10 Sep 2019
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] allocator: tcmalloc
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] modules: none
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] build environment:
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten]     distmod: ubuntu1804
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten]     distarch: x86_64
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten]     target_arch: x86_64
2020-10-02T00:26:15.543+0000 I CONTROL  [initandlisten] 11444 MB of memory available to the process out of 60395 MB total system memory
```
mongod is the primary daemon process for the MongoDB system. It handles data requests, manages data access, and performs background management operations.

#### SQLite Testing
Two ways to test that when a user signed up they were stored in the database or it worked;
  - Used a sqlite database viewer to look at the row that was added to the table
  - I also tried signing up with the same email address again, and when I got an error, I knew the first email was saved properly, also it redirected me ssuccessfuly to the login page.

#### Known Bugs


#### Expected Behavior
* Burger menu in mobile view immediately displays nav menu without clicking the burger.(FIXED)

* Logo Image and favicon image will not load. (FIXED)

* JS for datepicker functionality will not initiate from static/js/script.js file, it only successfuly initiates js code is directly in base.html file.

* Fade in Overlay CSS hover effect not functioning well for mobile devices. (FIXED).

* ENV VARIABLES - Went above and beyond to create environmental variables for my secret keys and URI's, however all my attempted where rendered unsuccessful. Kept receiving *ValueError: You must specify a URI or set the MONGO_URI Flask config variable* despite all attempts to use correct methods of setting up with env.py and also via gitpod. Reached out for help on the CodeInstitute slack channel and Tutor assistance, tutor could not help figure it out, neither the channel could help. I've exhausted all attempts to try not to submit my project with visible private info.


***

## Deployment / Project Setup 

Download
```bash
git clone https://github.com/Honey20103/BrewMaster.git
cd homebrew_app
```

Install python3
```bash
#use brew
brew install python3
```

Install pip3
```bash
#use apt-get
sudo apt install python3-pip
```

Deploy virtual environment.
```bash
#use pip3
pip3 install virtualenv
virtualenv venv
source ./venv/bin/activiate
```

Install requirements
```bash 
# install python requirements
pip3 install -r requirements.txt
```
Deploy SQLite database
```python
# python3
from app import db, create_app
db.create_all(app=create_app())
```
Deploy Mongo database
```bash 
#Setup Mongo DB account [here](https://www.mongodb.com/)
Create a mongoDB database.
Create a collection in it: logs
```
In a terminal, you can set the FLASK_APP and FLASK_DEBUG values:
```bash
# these gives instrcution to flask on how to load the app, it should point to the folder that holds the __init__.py.
# or create .flaskenv file and add the below without 'export'cmd
export FLASK_APP=project
export FLASK_DEBUG=1
```
Run app locally
```bash
flask run
```

Deploy to Heroku

* Create a free account in [Heroku](https://signup.heroku.com/)
* Once logged in Click on "Create new app", provide an app name of your choice and preffered region where the server your app will be deployed on.
* Follow instruction [here](https://devcenter.heroku.com/articles/heroku-cli) on how to install the heroku cli on your device

* Back to your CLI and project directory:

Login (provide email address and password when prompted)
```bash
heroku login -i
```

Initialize a git repository in a new or existing directory
```bash
$ cd my-project/
$ git init
$ heroku git:remote -a your-app-name-goes-here
```

Deploy your app by committing your code to the repository and deploy it to Heroku using Git.
```bash
$ git add .
$ git commit -am "write a valuable commit message here"
$ git push heroku master
```
Observe the build process in your CLI python app is set, requirements.txt and procffle are found.

### App Link
When your build is successful your app would be deployed at similar [link:https://your-app-name.herokuapp.com/](https://brewmaster-app.herokuapp.com/) to this one.


***

## Credits

### Content
The content on the site is derived from my boyfriend's self-made beer brewing log manuscript book. 

### Code
[Hover CSS effect on homepage: ](https://www.w3schools.com/howto/tryit.asp?filename=tryhow_css_image_overlay_fade) This package of CSS was used to render the behaviour of the homepage front image when hovering the image, to show the about of the app.

[Blueprints and configurations in application:](https://www.youtube.com/watch?v=Wfx4YBzg16s) This tutorial helped me use Application Factory, which allows to easily create multiple instances of the app with different configurations. The Blueprints restructuring split up my app into more manageable sections i.e Auth.py, main.py and _init_.py. 

[Authentication to App:](https://www.digitalocean.com/community/tutorials) Tutorial helped with setting up authentication to webapp.

### Media 

- The logo for the project was taken from the [pngtree](https://pngtree.com/) site. 

### Acknowledgements
- I was inspired to create this website from observing the struggles I watched my boyfriends encounter by trying to keep and maintain a manual notebook to store his brew day info or records, especially thankful for the help with testing functionality of the app. Thank you Robert Flink.

- I'd like to thank tutor Tim Nelson at CodeInstitute who helped unblock me when i was completely stuck and providing extra helpful resources.


<p align="center">
  <img src="https://github.com/Honey20103/BrewMaster/blob/master/homebrew_app/project/static/images/brewmaster2.png" style="margin: 0;" width="150" height="100">
</p>
