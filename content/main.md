---
weight: 10
title: Badge Connect Guide
---

# Badge Connect Guide

## A developer resource for implementers of Open Badges 2.1

Badge Connect API, released as Open Badges 2.1 brings the concept of a Federated backpack to the Open Badges ecosystem. A backpack is a service that acts as an agent for a recipient of Open Badges.

You can view code examples of each section of the guide.

This guide is sponsored by the [Badgr](https://badgr.com) Team at [Concentric Sky](https://concentricsky.com).

Editor: Nate Otto (Concentric Sky / Badgr - USA)

# Application Types

Applications in the Badge Connect-enabled Open Badges ecosystem fall into two main roles. **Host** (Backpack) and **Relying Party**. Relying Party applications typically serve functions as either an Issuer of badges, which provides recognition to recipients, or a Displayer of badges, which helps make badges meaningful or translate them back into some kind of real world value or new opportunity for their earners.

## What is a Host (Backpack)?

A Host is the official role name in the Open Badges Specification, commonly called a Backpack, which stores badge award data on behalf of recipients, making it possible for those recipients to organize and manage the badges they have earned. Backpacks may allow sharing to social media sites as a means of transmitting information about the achievements that a learner has gained.

## Examples of Issuer-role Applications

There are numerous reasons why an application would award badges. Badges can be used to recognize any achievement, large or small. Some example use cases include:

* Peer to Peer competency recognition
* [Badgebot](https://badgebot.io): award badges based on Twitter posts
* Instant quiz app like [Badgr Web Explorer](https://explore.badgr.io)
* Stack Exchange proxy issuer: get all the achievements for a user on Stack Exchange and issue them as Open Badges and push to backpack.
* Conversational systems for recognition: Define a badge collectively, as in a wiki, and trigger awards to peers.

## Examples of Displayer-role Applications

The first thing to understand about applications in the role of Displayer, is that Displayer is a clearly understood term for a vast category of applications that could make use of credentials earned by individuals, processing that credential data on behalf of badge recipients to provide them and others information about the meaning of these awards.

Examples of simple Displayer applications include:

* A credential-based Apply to Job on Seek.com API connector or profile modifier
* LinkedIn Badge Connector: Convert from Open Badges to post to LinkedIn certifications, skills, profile
* Conversational systems post-recognition: Talk pages about badgeclasses related to awards in a user's backpack

Farther-reaching Displayer applications include:

* A "collective backpack": A community pushes all their badges from individual backpacks into one common backpack to represent the achievements of a group within a single space, as opposed to only achievements earned by one individual.
* Europass Wallet Pusher: translate your OB credentials into format for visualization in Europass wallet

These examples were provided by the participants of a Badge Connect workshop at the [2019 ePIC Conference](https://epic.openrecognition.org) in Lille, France and by contributors to this guide.
