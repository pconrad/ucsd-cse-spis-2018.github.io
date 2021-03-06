---
topic: "Intro"
desc: "What are Web Applications all about?"
---

# UCSD CSE SPIS 2016

Projects: Web Applications (webapps) in Python using Flask


## Intro to webapps with Flask, in four parts


* Part 1: [Getting Started with Flask](/webapps/flask-getting-started/)
    * [old stuff](https://sites.google.com/a/eng.ucsd.edu/spis/home/2015_academicprogram/foundations/week-3-resources/web-apps-intro-notes-week-3)
    
* Part 2: [Input from URL/pass to function, creating your Heroku Account](https://sites.google.com/a/eng.ucsd.edu/spis/home/2015_AcademicProgram/foundations/week-3-resources/web-apps-intro-part-2)
* Part 3: [Deploying Code on Heroku](https://sites.google.com/a/eng.ucsd.edu/spis/home/2015_AcademicProgram/foundations/week-3-resources/web-apps-intro-part-3)
* Part 4: [Using Templates with your Flask App](https://sites.google.com/a/eng.ucsd.edu/spis/home/2015_AcademicProgram/foundations/week-3-resources/web-apps-intro-part-4)


## Learning More about HTML

Some useful example webapps:

| Description | Link |
|-------------|------|
| basic templates for pages, CSS, and navigation |  <https://github.com/pconrad/flask-practice-web-app> |
| using sessions |  <https://github.com/ucsd-cse-spis-2015/flask-webapp-session-example> |
| uploading files | <https://github.com/pconrad/heroku-try-file-upload> |

## Steps to making an app from scratch—the summary (details elsewhere)
* Make a github repo
* Make subdirectories for templates and static
* Create layout.html, home.html, page1.html and page2.html using patterns on this page: <http://flask.pocoo.org/docs/0.10/patterns/templateinheritance/> or this example repo: <https://github.com/pconrad/flask-practice-web-app>
* Set up `static/style.css`
* Create the `hello.py` file that runs it all
* Run and test locally with `python hello.py`

Example: <https://github.com/pconrad/flask-practice-web-app>

## To run on Heroku:

* First, you should have a heroku account (create one at heroku.com)
* Add and commit a `Procfile` and a `requirements.txt` file to github repo:
* Procfile consists of one line that tells heroku what to do with the repo: 
`web: gunicorn hello:app --log-file=-`
* requirements.txt lists needed Python modules and is created with one command:
`pip freeze > requirements.txt`
* Inside the github repo, run: `heroku login`
* Then run:  `heroku create`
* Then do: `git push heroku master`
* The log messages will contain the URL of your app, which is now deployed.
* You can manipulate the app at the dashboard at <http://heroku.com>

## Advanced stuff 

There may or may not be time for this during SPIS.  If not, these are some topics for further study if you want to take your web app further after SPIS is concluded.

### Flask in general:

* The main Flask website: <http://flask.pocoo.org/>
* Book: Flask Web Development By: Miguel Grinberg Publisher: O'Reilly Media, Inc. Pub. Date: May 8, 2014  Print ISBN-13: 978-1-4493-7262-0
 - Full text from on campus at UCSD: <http://proquest.safaribooksonline.com/book/programming/python/9781491947586>
 - From off campus, use the VPN
* The flask Mega-tutorial  http://blog.miguelgrinberg.com/post/the-flask-mega-tutorial-part-i-hello-world

## Database stuff:


`sqlite3` is an implementation of an SQL compatible database.
* On the ACMS machines for SPIS 2015, you can run sqlite3 by running `~spis15t7/bin/sqlite3`
* NOTE: That was installed for SPIS 2015, but would have to be reinstalled for SPIS 2016.
* You can also download precompiled binaries for sqlite3 for windows, mac, linux

On Heroku, you need Postgres.   If you are testing on your own machine (Windows/Mac/Linux), it is easier to just stick with Postgres and skip sqlite altogether.
* Info is here: <https://devcenter.heroku.com/articles/heroku-postgresql>
* To bring up the cli, you type heroku db:psql

## OAuth Stuff (e.g. to login with your Google, Facebook, or Twitter account...)

* <http://blog.miguelgrinberg.com/post/oauth-authentication-with-flask>

## Web Scraping (getting data from other sites)

Web Scraping with Python By: Ryan Mitchell Publisher: O'Reilly Media, Inc. Pub. Date: July 14, 2015 Print ISBN-13: 978-1-4919-1029-0
Available to read online, on UCSD campus, for free, at:
* <http://proquest.safaribooksonline.com/book/programming/python/9781491910283>
* To read from off campus, use the VPN
