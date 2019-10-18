---
weight: 30
title: Building Displayer Applications
---

# Displayer Applications: What you Need to Know

Here is a guide for how to build a prototypical displayer application that pulls badge awards from a recipient's backpack of choice and does something interesting with them. This example use case will be to display badges on a timeline to the user.

## Displayer Apps step by step

* A user starts on an badge displayer application and sees they have the opportunity to use the app by connecting their backpack. 
* A choice of backpacks is offered, including perhaps some suggestions known to the displayer application already as well as an advanced option to select a domain of their choice.
* If this is the first time the displayer application has encountered the backpack on the chosen domain, information about the backpack is read from the backpack's manifest file, and a server to server connection is established using Dynamic Client Registration
* The "OAuth Dance" is initiated, directing the user to the backpack for authorization.
* The user accepts the displayer app's requested permission scopes from within the backpack interface.
* The user is redirected back to the displayer application with a `code` in the query parameters portion of the URL.
* The displayer application exchanges the code for an access token (including a refresh token for later).
* The displayer application makes a request to the `GET /profile` endpoint to see the identifiers registered on the user's profile.
* The displayer application makes a call to the `GET /assertions` endpoint to read the badges in a user's backpack. The backpack responds with a successful result.
* The displayer application processes the badges. This may include submitting each badge to the validator for re-verification. As needed, the assertions are mapped to the recipient identifiers found in the profile.
* Badges are displayed to the user and/or become part of the user's experience on the displayer app.
* The displayer application may now pull updated badges to the user's backpack at any time.
* After some time, typically 1 hour, the access token expires. The next time the displayer app needs to contact the backpack on the behalf of this user, it will need to refresh its access token. At the time of its issue, the displayer application also obtained a refresh token. The refresh token is used to exchange the expired access token for a new one with an expiration date in the future.
