---
layout: post
title:      "Sinatra Project"
date:       2018-01-19 01:31:41 +0000
permalink:  sinatra_project
---

With Sinatra, often the most difficult part was to figure out the relationship, set them up and migrate them correctly (I had multiple migration failures before figuring out what needs to be done to fix the problem). 

With the project, since I had to decide what type of relationships different classes have with each other, I had a day of struggling/modifying/and figuring out what actually works out the best.

Since I am interested in creating a web platform for selling services, I decided to create a basic online marketplace for this project. I tend to to make things difficult in so in the beginning I envisioned something more complex with multiple product lines, categories, and stores; but after some contemplation (and failure), I decided to do a simpler version with users, stores, and products.
1. one user can own multiple stores with multiple products
2. one store can have multiple products but one user/owner
3. one product would belong to one store and one user/owner

After setting up these relationships, I decided to create a layout that would provide a login/signout/signup option on every pages depending on the website's login status.  I also decided to create few methods that could apply across controllers, such as a method for figuring out whether someone is logged in, who the current user is, and whether that user should be given access(modify/delete) to certain stores and products.

After migrating and troubleshooting, I designed views for each classes for various functions, e.g., viewing all, viewing a particular object, creating a new object, editing an existing object. 

After another series of trouble shotting, I wrote controller actions for each line of classes, utilizing flash messages and general methods previously written.

Overall, the program is designed to (1) create a user (2) allow that user to sign in (3) allow that user to create/edit/delete his/her own stores and products and (4) allow all users to view existing stores/products.  When an unauthorized access is attempted by going straight to the url (e.g., /edit /delete), I added flash messages redirecting and logging out the current user.

