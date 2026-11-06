# StillPoint

StillPoint is my exam project: a meditation web app where users can browse guided meditations, log finished sessions, and track their progress over time. The idea is that you pick a meditation, do it, and the app logs the session so you can go back and see your streak and old sessions.

Right now it's only the backend structure (Express + routers). Data is kept in memory and resets on restart.

## API

These are the endpoints I'm planning to have.

```
POST    /api/auth/register      Create a user account
POST    /api/auth/login         Log in
POST    /api/auth/logout        Log out
GET     /api/auth/me            Get the current user

GET     /api/users/{id}         Get a user's profile
PATCH   /api/users/{id}         Update parts of the profile
DELETE  /api/users/{id}         Delete a user

GET     /api/meditations        Get all meditations (breathing, body scan, guided, timer...)
GET     /api/meditations/{id}   Get one meditation

GET     /api/sessions           Get the user's session history
GET     /api/sessions/{id}      Get one session
POST    /api/sessions           Log a finished session
DELETE  /api/sessions/{id}      Delete a session

GET     /api/stats/summary      Get totals and current streak
GET     /api/stats/streak       Get the current streak
```

## Ideas for later

A dashboard where you can see your minutes meditated per week and month, so you can tell if the habit is actually sticking.

Personal bests (longest session, longest streak) shown on the dashboard with a trophy icon.

Mood tracking before and after a session, with a simple trend view.

Favourites and a "continue where you left off" card.

Reminders (email or in-app) to build a daily habit.
