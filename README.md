# socialmediaresearch
Code for extracting Facebook Data for research project - http://www.meganknight.uk/uncategorized/social-media-research-project/

This project is developing the research discussed at http://www.meganknight.uk/journalism/social-media-research-project/ and at http://www.meganknight.uk/uncategorized/facebook-and-the-news/

It is built with the Facebook Graph API, and runs on PHP, and a simple mysql database

THe code in this repo works as follows: 

1. Collects basic consent data from a user (index.php), assigns a unique id and records the consent with that ID. 

2. Asks the user to sign in to Facebook and accept the app's conditions (formresult.php).

3. Gathers the Facebook user id, checks whether it has already been recorded, and if not records it once in a table. 
    
    If it has been used, the process proceeds as normal, but the unique id is tagged as a duplicate record. 

4. Collects the most recent likes and posts by the user, and their political beliefs and birthday (to calculate age). 

5. Stores this data in tables, linked to the unique id generated in step 1. This is never linked to the Facebook ID, and there is no way to reconnect the two pieces of data.

6. Asks a brief survey of news awareness, and stores those in the database. 

