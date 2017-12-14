---
layout: post
title:      "CLI Data Gem Project: Overview"
date:       2017-12-14 19:16:17 +0000
permalink:  cli_data_gem_project_overview
---


In this project, I aimed at collecting social clips from the ALS News Today webpage, so that a user would be able to get information on existing clips and search for a clip that he/she may be interested in.

I mainly worked on the files in the library folder.  
* The bin folder was only used for an actual execution of this program.

Inside the library folder, I first created a cli controller to test out and design this program.  Inside the cli controler, I build in the call method, which would be used to run this program; and other sub methods for generating, listing and providing more options (i.e., obtain more information or search for a particular clip.
So, the cli controller was designed to have the following sub-methods:
* generate a new CLIP class from the webpage
* list each clip from the new CLIP class by entry number, so that user can easily select any clip for more information
* ask if user wants to perform additional  actions, i.e., re-listing the clips, getting more information from a particular clip, or search for a clip with any keyword
* goodbye method after user exits the program


Then, I created following files for performing more detailed steps necessary for the cli controller:
1. for scraping data from the ALS News Today webpage and 
2. for creating clip objects containing particular information from the webpage.

After examining the webpage, I decided that I want to collect the following information for each clip object: 
* date
* title
* url
* summary: since this data was relatively long, I decided to use this data as additional information any user may obtain by selecting a particular clip.
So, I designed a class Clip so that any new object would contain these information.

Next, I went to the scraper file to build a method that create an array of clips from the webpage; and went back to the cli file to create a method that builds multiple clips obtained from the website.  This particular method was designed so that each new clip would automatically obtain matching information for each data objects.  I also created a method for obtaining actual contents for keyword search from each particular clip; and a method for finding clip that matches a user's keyword input.
* While I created another method for searching by month, after giving it a thought, I did not implement this method in a final cli controller because the total number of clips was less than 15; and any user would be able to easily identify clips from any month by simply examining the list.

After test-running the program, I realized that it would be difficult to select a clip by entry number, unless that entry number was somehow associated with its clip within the Clip class.

So, instead of simply lising with index, I build in another property called "entry_number" to each clip object, which property would get assigned to all clips after they are generated.  This way, after a user selects an entry number, the program can easily identify the matching clip and its summary data.

After performing these steps, I continued re-running the program to add instructions and clean up the information the user would see. 


