+++
showonlyimage = false
draft = false
image = "img/portfolio/adventure.jpg"
date = "2021-11-05T19:59:22+05:30"
title = "Adventure Game"
weight = 8
+++

<!--more-->

{{< rawhtml >}} 

<video controls width=100%>
    <source src="/videos/adventure.mp4"
            type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>

{{< /rawhtml >}}

{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}


For this project, I learned about data driven game design by developing a text-based adventure game. An "adventure" begins with selecting a provided file by the player. These files could represent anything, but in my case I chose to represent different locations on campus. Users of this project get to engage by typing in commands such as "go", "score", and "inventory." The game progresses and updates with the use of these commands. It is built in a REPL environment to be able to generate error messages when invalid commands are used. Since the game is determined by the input file, this project isn't limited to exploring campus, it's really a game engine that can be utilized to create any sort of adventure. It was developed with OCaml with the following objectives.

* Design data types
* Work with lists and trees
* Use pattern matching and higher-order functions
* Read information from files, and interact with the user
* Learn about JSON