---
weight: 20
title: Building Issuer Applications
---

# Issuer Applications: What you Need to Know

Here is a guide for how to build a prototypical issuer application that awards Open Badges and pushes them to a recipient's backpack of choice.

## Issuer Apps step by step

* A user starts on an issuing application and earns a badge. For example, they successfully complete a quiz.
* An Open Badges Assertion is published, linked to a BadgeClass and Issuer Profile, according to the [Open Badges 2.0 Specification](https://openbadgespec.org).
* The user is offered the opportunity to claim the badge by accepting it into a backpack of their choice.
* A choice of backpacks is offered, including perhaps some suggestions known to the issuer application already as well as an advanced option to select a domain of their choice.
* If this is the first time the issuer application has encountered the backpack on the chosen domain, information about the backpack is read from the backpack's manifest file, and a server to server connection is established using Dynamic Client Registration
* The "OAuth Dance" is initiated, directing the user to the backpack for authorization.
* The user accepts the issuer app's requested permissions from within the backpack interface.
* The user is redirected back to the issuer application with a `code` in the query parameters portion of the URL.
* The issuer application exchanges the code for an access token (including a refresh token for later).
* The issuer application makes a request to the `GET /profile` endpoint to confirm that the awarded recipient identifier appears within the user's backpack profile.
* The issuer application makes a call to the `POST /assertions` endpoint to add the awarded badge to the user's backpack. The backpack responds with a successful result.
* The issuer application may now push badges to the user's backpack at any time.
* After some time, typically 1 hour, the access token expires. The next time the issuer app needs to contact the backpack on the behalf of this user, it will need to refresh its access token. At the time of its issue, the issuer application also obtained a refresh token. The refresh token is used to exchange the expired access token for a new one with an expiration date in the future.
