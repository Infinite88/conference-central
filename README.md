# Conference Central API Project

## About
This cloud-based API server lets you organize conferences and sessions, and currently has following functionality:

User authentication
Create, read, update conferences
Register/unregister for conferences
Create and read sessions for conferences
Add/remove sessions to user's wishlist
This project, the fourth in Udacity’s Full Stack Web Developer Nanodegree, focuses on using Google Cloud Platform to develop a scalable web app, and it's built with Google App Engine (Python), Google NDB Datastore, and Google Cloud Endpoints. 

You can view the web page at https://conference-app-1098.appspot.com

## Project Details

## Task 1: Add Sessions to a Conference

The following endpoints were added:
- `createSession`: given a conference, creates a session.
- `getConferenceSessions`: given a conference, returns all sessions.
- `getConferenceSessionsByType`: given a conference and session type, returns all applicable sessions.
- `getSessionsBySpeaker`: given a speaker, returns all sessions across all conferences.

I based these endpoints off of the Conference class since they were similar.

## Task 2: Add Sessions to User Wishlist

This was also referenced from conference registration functionality.

## Task 3: Work on indexes and queries

Instead of creating a specialized session query, i based sessions queries off of conference queries. START_TIME, TYPE_OF_SESSION, SPEAKER, and DURATION can be queried.

## Task 4: Add a Task

getFeaturedSpeaker method uses memcache to store the featured speaker.

## Setup Instructions

To deploy this API server locally, ensure that you have downloaded and installed the Google App Engine SDK for Python. Once installed, conduct the following steps:

1. Clone this repository by entering the following command 'git clone https://github.com/Infinite88/conference-central.git'
2. (Optional) Update the value of application in app.yaml to the app ID you have registered in the App Engine admin console and would like to use to host your instance of this sample.
3. (Optional) Update the values at the top of settings.py to reflect the respective client IDs you have registered in the [Developer Console][4].
4. (Optional) Update the value of CLIENT_ID in static/js/app.js to the Web client ID
5.(Optional) Mark the configuration files as unchanged as follows: $ git update-index --assume-unchanged app.yaml settings.py static/js/app.js
6. Run the app with the devserver using dev_appserver.py DIR, and ensure it's running by visiting your local server's address (by default [localhost:8080][5].)
7. (Optional) Generate your client library(ies) with [the endpoints tool][6].
8. (Optional) Deploy the application via appcfg.py update.