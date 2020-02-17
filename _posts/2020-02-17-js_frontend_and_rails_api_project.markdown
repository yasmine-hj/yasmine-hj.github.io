---
layout: post
title:      "JS Frontend & Rails API Project "
date:       2020-02-17 14:30:23 +0000
permalink:  js_frontend_and_rails_api_project
---

For my Javascript Frontend and Rails API backend project I decided to create a therapy cards game where the user picks a topic and will get a random card with a therapy question from a collection of cards from that topic and have a response card where they can type in and log their responses. At first I found JS quite difficult to get used to in comparison to Ruby, but I decided to identify the similarities instead of the differences as advised, and that mindset made this project a whole lot easier and more enjoyable for me.

Inputting scripts into your index.html page and the order in which you do so is super important here. Here are the scripts which I used for my project:

```
<script src="./src/components/Topic.js"></script>
 <script src="./src/components/Card.js"></script>
 <script src="./src/components/Response.js"></script>
 <script src="./src/components/Topics.js"></script>
 <script src="./src/adapters/TopicsAdapter.js"></script>
 <script src="./src/components/App.js"></script>
 <script src="./src/index.js"></script>
```

An awesome and important feature of JS is the ability to send network requests to the Rails server and load new data whenever needed. This is done through HTTP requests which are achieved through `fetch`. The topics adapter is where I had all my fetch requests. I used the following code to get my responses from the Rails API:

```
  getResponses(){
        return fetch(`http://localhost:3000/responses`)
        .then(res => res.json())
    }
```

And here's  an example of a fetch request I used to create a response is:

```
createResponse(response){
       return fetch(`http://localhost:3000/responses`, {
           method: 'POST',
           headers: {
               'content-type': 'application/json'
           },
           body: JSON.stringify({response})
       })
       .then(res => res.json())
   }  
 
```
And to delete a response:

```
deleteResponse(id) {
       return fetch(`http://localhost:3000/responses/${id}`, {
           method: 'DELETE',
           headers: {
               'content-type': 'application/json'
           }
       })
   }
```

I had so much fun with this project that I'm actually kinda sad to be finishing and submitting it. I will definetely be going back and adding even more features to it the more I learn!



