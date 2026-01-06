---
layout: post
title: About me! ♡
permalink: /about/
comments: true
---

## As a conversation Starter

Here is the only place I have lived at !

<style>
    /* Style looks pretty compact, 
       - grid-container and grid-item are referenced the code 
    */
    .grid-container {
        display: grid;
        grid-template-columns: repeat(auto-fill, minmax(150px, 1fr)); /* Dynamic columns */
        gap: 10px;
    }
    .grid-item {
        text-align: center;
    }
    .grid-item img {
        width: 100%;
        height: 100px; /* Fixed height for uniformity */
        object-fit: contain; /* Ensure the image fits within the fixed height */
    }
    .grid-item p {
        margin: 5px 0; /* Add some margin for spacing */
    }

    .image-gallery {
        display: flex;
        flex-wrap: nowrap;
        overflow-x: auto;
        gap: 10px;
        }

    .image-gallery img {
        max-height: 150px;
        object-fit: cover;
        border-radius: 5px;
    }
</style>

<!-- This grid_container class is used by CSS styling and the id is used by JavaScript connection -->
<div class="grid-container" id="grid_container">
    <!-- content will be added here by JavaScript -->
</div>

<script>
    // 1. Make a connection to the HTML container defined in the HTML div
    var container = document.getElementById("grid_container"); // This container connects to the HTML div

    // 2. Define a JavaScript object for our http source and our data rows for the Living in the World grid
    var http_source = "https://upload.wikimedia.org/wikipedia/commons/";
    var living_in_the_world = [
        {"house": "house.jpg", "greeting": "My Humble Home <3", "description": "House 1"}
        //{"house": "b/b9/Flag_of_Oregon.svg", "greeting": "Age 3-4", "description": "House 2"},
        //{"house": "b/be/Flag_of_England.svg", "greeting": "Age 4-6", "description": "House 3"},
        //{"house": "e/ef/Flag_of_Hawaii.svg", "greeting": "Age 4-current(14)", "description": "House 4- current house!!!"},
    ];

    // 3a. Consider how to update style count for size of container
    // The grid-template-columns has been defined as dynamic with auto-fill and minmax

    // 3b. Build grid items inside of our container for each row of data
    for (const location of living_in_the_world) {
        // Create a "div" with "class grid-item" for each row
        var gridItem = document.createElement("div");
        gridItem.className = "grid-item";  // This class name connects the gridItem to the CSS style elements
        // Add "img" HTML tag for the flag
        var img = document.createElement("img");
        img.src = "{{site.baseurl}}/images/about/" + location.house; // concatenate the source and flag
        img.alt = location.house + " House"; // add alt text for accessibility

        // Add "p" HTML tag for the description
        var description = document.createElement("p");
        description.textContent = location.description; // extract the description

        // Add "p" HTML tag for the greeting
        var greeting = document.createElement("p");
        greeting.textContent = location.greeting;  // extract the greeting

        // Append img and p HTML tags to the grid item DIV
        gridItem.appendChild(img);
        //gridItem.appendChild(description);
        gridItem.appendChild(greeting);

        // Append the grid item DIV to the container DIV
        container.appendChild(gridItem);
    }
</script>

### My journey through life

Here is what I've done in my life so far!:

- Born on August 19, 2011 ⋆.ೃ࿔*:･
- Attended Stone Ranch Elementary School from kindergarden to 5th grade ⋆.ೃ࿔*:･
- Started learning Ice Skating ⛸️
- Started learning dance 💃
- Joined Math Olympaid and Debate club 🧠📚
- Attended Oak Valley Middle School from 6th to 8th grade ⋆.ೃ࿔*:･
- Joined Sci Olympaid 🧑‍🔬
- Started tennis 🎾
- Currently in Del Norte Highschool until 2029 ⋆.ೃ࿔*:･

### Hobbies, Family, and Fun

For me, everything is all about family, sports and my hobbies.

- I do around sports 5 in total; field hockey, tennis, dance, ice skating, swimming
- My family is pretty big however most of them live in India. Me and family are the only ones who live in the US currently. Despite being the only ones, we are a small family. Me, my dad and my mom.
- The gallery of pics has some of my family, hobbies, and sports.

<comment>
Gallery of Pics, scroll to the right for more ...
</comment>

## Favorite Foods

<div class="image-gallery">
  <img src="https://upload.wikimedia.org/wikipedia/commons/3/3f/Pizza_margherita.jpg" alt="Pizza">
  <img src="https://upload.wikimedia.org/wikipedia/commons/5/5c/Tacos_al_pastor.jpg" alt="Tacos">
  <img src="https://upload.wikimedia.org/wikipedia/commons/9/9c/Spaghetti_al_Pomodoro.JPG" alt="Pasta">
</div>

<style>
.image-gallery {
  display: flex;
  flex-wrap: nowrap;
  overflow-x: auto;
  gap: 10px;
}

.image-gallery img {
  max-height: 150px;
  object-fit: cover;
  border-radius: 5px;
}
</style>
