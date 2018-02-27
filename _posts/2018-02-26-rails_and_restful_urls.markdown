---
layout: post
title:      "Rails & RESTful URLs"
date:       2018-02-27 01:49:49 +0000
permalink:  rails_and_restful_urls
---

At first, Rails seemed magical.  It builds forms and urls for you; it creates a folder structure with one key word.  

However, as things got more complicated (especially with authentication), rails became challenging.  Also, at times, portions of the instructions have become outdated thereby requiring me to separately search for solutions online and troubleshoot.

With the final project, I wanted to build something that I can use later on for my own website.  Since I am interested in building a web directory for free job postings/searches - similar to craigslist, I decided to build a basic directory with job profiles.  

At first, I wanted only the site owner to have the authority to add categories; and link different profiles to various categories and skills.  However, due to the project requirement, I later changed the authorization for categories, so that users can use a form for categories' nested attributes under each profile.

For the authentication system, I decided to use Google since facebook has been implemented in previous projects.

At a high level, this website allows job seekers to post their profiles under various job categories; and employers to view  job profiles so that they can contact a profile owner to request his/her service.  

At a more detailed level, this website involves multiple classes, including: users, categories, profiles, skills.  Since categories and profiles have many to many relationship, there also is a joint class for them.  Once a user signs in, he/she can create profiles, which in turn allows him/her to create new categories and skills.  Each user is given certain authorizations depending on his/her signed on status and ownership of a profile.  

When creating profiles and user accounts, the website identifies whether certain requirements are met and gives an error message if one or more of those requirements are not met

From a viewer level, the website recommends certain profiles over the others depending on their availability date and hourly rate.

While working on this project, the first challenge was to design a website structure that serves my original intention and the project requirements.  This required me to tweak designs and relationships.  

Also, I encountered several obstacles along the way, including the error messages feature.  Only after some researching and study group, I realized that error messages won't show up unless I add this line in the controller: @profile.errors.full_messages.  Also, I had to resolve conflicts with the devise gem while building the authentication feature and learned that I need to rename my url paths so that my sign up/log in feature does not conflict with devise.

Overall, this was an educating experience.  This project enabled me to learn various authentication/authorization features and think through various website features/designs.
