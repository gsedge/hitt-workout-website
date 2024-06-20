# HIIT up2120601

## For running the code
You will need to run the folling commands to run this wesbite
- npm init
- npm run setup
- npm start

This will run the server on port 8080

- There is a test account with the credentials: username= "test", password: "test"



## Key features

1. Importing your workouts into the create a workout page
2. The website guide
3. Drag and drop
4. Activity workout
5. Checking before leaving the create a workout

### Importing your workouts into the create a workout page
The “Create a Workout” feature is a key component of my project. Once logged in, users can navigate to the “Create a Workout” page through the top navigation bar. This page allows users to create and customize a new workout with a wide variety of activities to choose from.

One of the key features of this page is the import button. This button allows users to select a pre-existing workout, view its itinerary, and then add it to their current workout if they wish. This effectively adds the activities and times from the selected workout to the end of the workout currently being created.

This feature was developed in conjunction with another feature that prompts the user when they attempt to save a workout with a pre-existing name. If the user chooses to override the existing workout, the server will update the workout with the new details. This functionality was implemented to provide users with an easy way to modify their pre-existing workouts or create a slightly different workout based on one they already enjoy.

### The website guide
The website guide is another key feature of my project. Accessible from the homepage under the site logo, the guide page provides an overview of the site’s key features in an easy-to-understand format with pictures. This ensures that users can fully utilize the site and take advantage of all its features.

### Drag and drop
When the user is creating a new workout, the workout and times that they select appear on the right-hand side of the screen, but if you click and hold on one of the items, and drag it either up or down,
it will change the order of the workouts to where you put your selected workout. I implemented this as I believed it should be a basic need for the site for users to dynamically amend the order of their workouts after they select them.

### Activity workout
My project includes the workout page where you can create your own workouts and then do them with a timer and itiniary that the user selected. But we also have a feature that shows all the activities you can select from to create your workout, with a full description of the activity and a gif image to demonstrate how it is done, which is found in the top nav bar as "activities". As well as that you can try out all the different activites, where you can set the duration of a set, the amount of sets you would like to do, and set a cooldown time if the sets are more than one, for the activity the user has chosen. I implemented this so that the user isnt forced to create a workout with just one activity if they want to just try it out. You can access this page by clicking the "Do it" button beside each activity. 

### Checking before leaving the create a workout page
In the create a workout page, if a user starts to create a workout, by either importing one of their workouts or by adding an activity to their workouts, and then they try to go to another page, it will create a pop up which asks the user if they want to disgard their workout. I did this so that the user doesnt accidently leave the page and disgard their workout that they have been creating.
--------------------------------------------------------


## AI

### Development of the drag and drop feature
As throughout this project I was still learning javascript, the drag and drop feature was probably the hardest feature I had to learn how to create, but these promts helped me understand how it could be implemented. This can be found in the index/create-workout.html file in the script section at the bottom, it is commented to help you find it. Or on the website in the "Create a workout page" after you add an activity to the workout.

>  **Explain to me how to use element siblings such as parentNode and nextSibling in javascript?**
The response was useful as it gave me different code snippets explaining how I could access elements around an element, when I didnt have an ID/class for them, and when they are dynamically changing, like in the drag and drop feature i'm implementing.

> **How do i get an array containing all items in a list?** 
The response was really helpful to me as it gave me what i was asking for, but also their indexes, which made it alot easier for me, as i needed this list so that I can get the values of each list element, which told me what exercise, and time, was where, so that I can keep an updated index-value list of all the activties so when they save the workout it is easy to upload all the information to the server.

> **Why is my li element value saving as Object Object?**
The suggestion helped me as I tried to keep setting the value of a list item to a json object, but this taught me that it can only be a string, which helped me fix an issue that I had been stuck on for a long time.
--------------------------------------------------------

### Using time in javascript
In my site I have a recent activity page, which can be found in the top navigation bar after you login, and in there it logs all the workouts you have done and for how long, and I thought it was essential in a page of this fashion to show the time that you did the workout with, so, as I was still learning javascript, I had to learn how to use the Date() module

>  **How do I get the time in javascript?**
This was useful as it listed all the different functions such as Date.getHour() which helped me quickly implement adding time to a recent workout.

> **How do I set a Date() as another time?**
This wasnt that helpful as I used this to help me with the homepage as there is a feature which shows how many seconds this week you have worked out for, and it did help however it made the solution more difficult than I anticipated.
--------------------------------------------------------

### Learning css
Before this project I had a basic understanding of css, but quickly realised that I didnt have enough of an understanding to get this project to where I wanted it to be.

> **How can you hide an element with css?**
This was very useful as in multiple differnt pages in my project, such as the create workout and recent activity pages, I needed to create a pop up box, or just hide the start button in the workout pages, and this gave me the way to do all of that, by creating a div and then just hiding it when it shouldnt need to be shown.

> **How can I change the style of an element in javascript?**
Although the solution to this was very simple, as I am still learning javascript I just didnt understand how you could change it, but this promt gave me an easy solution which helped me create a considerably more dynamic site.

> **How can I create a circular border around text with css?**
This wasnt particulary useful as it gave me alot of css code which when I tried to implement it didnt work, so I had to search up each of the different css code it gave me to find what would actually be relavent to help me and what wasnt relevent. 
--------------------------------------------------------

### Understanding express servers
Initially when I started this project, I really struggled with getting my head around the actual implementaion of a client-server model website, however AI did help with that

> **How can I get data through a url using an express server and javascript?**
This response helped alot with the design of the website as it allowed me to create simple buttons which directs the user to the correct page, espessially when they want to go a workout page, without the need for the user to have to post something to the server, then get the server to hold it until that page fetches data. This query helped aid that by showing me how to use req.body to get data in the url.

> **How can I access the response from a post request using an express server and javascript?**
This was very helpful in my design of the create workout page feature which checks to see if a workout name is already being used by that user, and checks to see if the user wants to override that workout, as the client has to read the response from the server in order to know wether to show a pop up box, or to return to the homepage if the save was just successful.

--------------------------------------------------------

### Conclusion
After finishing this project, I can happily say that I have learnt how to create a full website with many different features with javascript and node.js.

**Outcome**
I'm happy with the features that I have implemented in this project, particulary the database structure, which I tested rigerously so that there won't be an error in any case of it being used. I am also happy with the drag and drop feature as it is the one that I found the most technically challenging.
I'm also pleased with the structure of the project, as the file layout is easily navigatable, such as the data folder which has induvidual folders for each activity, and each file in the index folder holds all the neccesary code for that page, eg. css and javascript, in the format:
- Head
- Body
- Script
- Style 

**Future improvements**
If I had more time I would definetely add more functionality to the website, such as;

> A delete activity function in the create workout page
I would do this so that the user can have complete customizability over their own workouts and not have to restart creating a workout if they decide that they don't want a certain activity in there.

> An option where the user can add their own activities to add to a workout.
I would do this so that they don't have to stick to the workouts that my site offers, which purposly doesnt include any that require any other equipment as I don't think that should be included in a HITT workout, however the user may feel differently.

**Critical analysis**
> I would say what I struggled with the most in this project was css. When I started the project I knew basic css so tried to go with what I knew but quickly realised that I would need to learn alot more for a website of this size, and for what my expectation of the project was, such as learning display settings such as flex and block, but also how to manipulate css in javascript, which I needed to do so I could show/hide different elements, and change styles dynamically so the website really felt interactive to the user. This is where I put a lot of effort into learning, so the website looked asthetically pleasing and also how I wanted it to look, while dynamically changing.

> My second point relates to this as a few of my element names don't clearly show what element it may realate to, which can decrease the maintainablity and readability of my code. It starts to get worse on the later pages I developed because they had alot more elements and so I quickly named them so that I could get on with creating the site, howver obviously this is not a good practise to do and in the future I will change this.

> Thirdly, in the create workout page, if a user tries to save a workout and it has the same name as another one of their workouts, it asks to see if they would like to override that workout, this is shown in a pop up box at the top of the page, however the only solution I could think of to implement this is to create a timer on the server from when they try save it, and if they click yes within a certain amount of time it will proceed to change the workout, however, if the timer runs out then it will not work and the server will treat it like the user is just trying to save it again. Ideally I would have came up with another solution which doesnt require the user to have to answer the question under a time limit which they dont know about.
