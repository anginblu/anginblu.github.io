---
layout: post
title:      "Rails App with jQuery Front End"
date:       2018-04-23 03:47:10 +0000
permalink:  rails_app_with_jquery_front_end
---


The main purpose of this project was to update an existing rails app (Peraide Market) with a new review/comment functionality so that users can add and view reviews/comments to existing job profiles.

There were five main objectives:
1. Create a relationship between a Profile class and Comment class so that a profile can have many comments & any link to comments are nested under a profile url.
2. Create a relationship between a User class and Comment class so that a user can have many comments that he/she has written.  
3. Utilize jQuery and an Active Model Serialization JSON Backend so that a show and index pages for a Comment class would be in a JSON format.
4. Create a dynamic form/show buttons so that users can add/view comments to a profile via AJAX.
5. Utilize Javascript Model Objects & prototype functions for future expansions.

In the future, I want to only allow users who are logged in to add a new review & add a delete option for any existing review when its author is signed in.


