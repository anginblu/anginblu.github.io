---
layout: post
title:      "Integrating React/Redux frontend with Rails backend"
date:       2018-05-29 00:47:30 +0000
permalink:  integrating_react_redux_frontend_with_rails_backend
---


I've been learning how to code for several months now; and I am finally at the end of my coding endeavor with the Flatiron School (I know there is much more to learn still!).  

As my final project, I built a rails API backend to be used with React/Reduct frontend.  

This project is a continuation of my previous projects, which purported to build a web directory where users can view and publish profiles of service professionals.  [Here](https://github.com/anginblu/Peraide-v3) you can view the README file for my app and see its repo.

While my previous proejcts allowed many of the same features as the current app, the biggest difference is that Ruby on Rails(RoR) was used as backend API only.  All of the user interactions happened on React frontend using Redux library.  So, the biggest challenge was to restructure the backend rails to securely allow users to access database.

#Backend

I created the backend using Ruby on Rails. Because the backend is only responsible for database related queries, all of the view files became unnecessary, and I had to reorganize controllers under an Api module. 

Basic models included User, Category, Profile, and Bookmark.  I also set up relationships between categories and profiles, bookmarks and profiles, and users and profiles/bookmark.  This way, any user would be able to own one or more profiles, belonging to one more more categories, and one bookmark.  


#Frontend

I created the frontend using React and Redux.  

While most of the website structure would mirror previous projects, I wanted users to have an easier way of browsing through the database (profiles/categories).  

After setting up a store using redux thunk, I connected several actions and reducers to communicate with the RoR API.  
Then, I used react router to set up several web pages, namely: home, about, profiles (and individual pages for each profile), and categories page.  

For the home page, I used buttons representing each category, so that by clicking these buttons, users can easily navigate through profiles that they want to see.  

For the profiles page, I added a search bar that shows matching profiles based on the profiles' descriptions.

For the categories page, I added a search bar that instantaneously updates the view based on the keyword entered into the bar.




