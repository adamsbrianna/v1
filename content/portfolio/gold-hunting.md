+++
image = "img/portfolio/pollack.png"
showonlyimage = false
date = "2021-11-05T19:57:40+05:30"
title = "Gold Hunting"
draft = false
weight = 11
+++

<!--more-->

{{< rawhtml >}} 

<video controls width=100%>
    <source src="/videos/crossword.mp4"
            type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>

{{< /rawhtml >}}

{{< rawhtml >}} 
<p> &nbsp; </p>
{{< /rawhtml >}}

Far far away, behind the word mountains, far from the countries Vokalia and Consonantia, there live the blind texts. Separated they live in Bookmarksgrove right at the coast of the Semantics, a large language ocean.

A small river named Duden flows by their place and supplies it with the necessary regelialia. It is a paradisematic country, in which roasted parts of sentences fly into your mouth.

1. Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
2. Aliquam tincidunt mauris eu risus.

> The Big Oxmox advised her not to do so, because there were thousands of bad Commas, wild Question Marks and devious Semikoli, but the Little Blind Text didn't listen. She packed her seven versalia, put her initial into the belt and made herself on the way.

## Header Level 2

Even the all-powerful Pointing has no control about the blind texts it is an almost unorthographic life One day however a small line of blind text by the name of Lorem Ipsum decided to leave for the far World of Grammar.

The Big Oxmox advised her not to do so, because there were thousands of bad Commas, wild Question Marks and devious Semikoli, but the Little Blind Text didn't listen. She packed her seven versalia, put her initial into the belt and made herself on the way.

* Lorem ipsum dolor sit amet, consectetuer adipiscing elit.
* Aliquam tincidunt mauris eu risus.

When she reached the first hills of the Italic Mountains, she had a last view back on the skyline of her hometown Bookmarksgrove, the headline of Alphabet Village and the subline of her own road, the Line Lane. Pityful a rethoric question ran over her cheek, then  


in this assignment, you will help Cornell President Martha Pollack find the Orb of AI in a just-discovered
cavern under Gates Hall. You will help her scram (get out quickly) before the cavern collapses.

The assignment has two phases;

1.Finding for the Orb during the first phase

On the way to the Orb, the layout of the cavern is unknown. Pres Pollack knows only the status of the tile on which she is standing and the immediately surrounding ones. Her goal is to make it to the Orb in as few steps as possible.
This can be used greedily to optimize the find algorithm, but the greediness does not always work

2. Collecting gold during the scram phase

The stress of the moving walls has compromised the integrity of the cavern, beginning a step limit after
which the ceiling will collapse. The goal of the scram phase is to run to the exit from the cavern before it collapses

In this assignment, you will help Cornell President Martha Pollack find the Orb of AI in a just-discovered
cavern under Gates Hall.



On the way to the Orb (see Fig. 1 on the next page), the layout of the cavern is unknown. Pres Pollack
knows only the status of the tile on which she is standing and the immediately surrounding ones (and
perhaps those that she remembers). Her goal is to make it to the Orb in as few steps as possible.
This is not a blind search, however. For each tile, the distance to the Orb is known, and this can be used
to optimize the hunt somewhat.
1
Figure 1: Hunting for the Orb during the first phase
Note: In the hunt-the-Orb phase, all edges in the graph have weight 1.
You will develop the solution to this phase in method huntOrb() in class Pollack within package
app. There is no time limit for this task, but you will receive a higher score bonus multiplier for finding the
Orb in fewer steps. In order to pick up the Orb, simply return. Returning when Pres Pollack is not on the
Orb will throw an exception, halting the game.
Method huntOrb() has as parameter a HuntState object, which contains information about the envi-
ronment. Every time Pres Pollack moves, this object automatically changes to reflect her new location. This
object includes the following methods:
1. long currentLocation(): Return a unique identifier for the tile Pres Pollack is on.
2. int distanceToOrb(): Return the distance from Pres Pollack’s location to the Orb. This is the
Manhattan distance, but you don’t have to be concerned with what that term means. Look it up in
JavaHyperText if you want.
3. Collection<NodeStatus> neighbors(): Return information about the tiles to which Pres Pol-
lack can move from her current location.
4. void moveTo(long id): Move Pres Pollack to the tile with ID id. This fails if that tile is not
adjacent to her current location.
Function neighbors() returns a collection of NodeStatus objects. This object contains, for each
neighbor, the ID corresponding to that neighbor, as well as the neighbor’s distance to the Orb. You can
examine the documentation for this class for more information on how to use NodeStatus objects.
We strongly suggest that you visit JavaHyperText, click on DFS/BFS in the navigation links at the top,
and study the last video on a DFS walk. Study it carefully! You will find it easy to write huntOrb() if you
understand this video.
ONCE you have a correct implementation of huntOrb() running, then see how you could optimize
it to use the distances to the Orb of the current location’s neighbors to provide some optimization. This
should be a local optimization; the whole method need not be written.
4 Scram Phase
After picking up the Orb, the walls of the cavern shift and a new layout is generated. Additionally, piles of
gold fall onto the ground. Luckily, underneath the Orb is a map, which reveals the full cavern. However,
the stress of the moving walls has compromised the integrity of the cavern, beginning a step limit after
which the ceiling will collapse. Additionally, picking up the Orb activated the traps and puzzles of the
cavern, causing different edges of the graph to have different weights.
2
Figure 2: Collecting gold during the scram phase
The goal of the scram phase is to run to the exit from the cavern before it collapses. However, a score
component is based on two additional factors:
1. The amount of gold that Pres Pollack picks up during the scram phase, and
2. The score multiplier from the hunt-the-Orb phase.
Pres Pollack’s score will be the amount of gold picked up times the score multiplier from the hunt-the-
Orb phase. Since it is fairly straightforward to simply get out of the cavern given your Dijkstra’s implemen-
tation from A6, we expect you to spend time working to optimize your score.
You write your solution to this part in function scram() in class Pollack in package app. Method
scram() has parameter a ScramState object, which describes Pres Pollack’s environment. Every time
she makes a move, this object automatically changes to reflect her new location. We describe the methods
available in ScramState. After that, we explain a bit about the scram phase.
1. Node currentNode(): Return the Node corresponding to Pres Pollack’s location.
2. Node getExit(): Return the Node corresponding to the exit from the cavern (the destination).
3. Collection<Node> allNodes(): Return a collection of all traversable nodes in the graph.
4. int stepsLeft(): Return the number of steps Pres Pollack can take before the ceiling collapses.
5. void moveTo(Node n): Move Pres Pollack to node n. This will fail if n is not adjacent to her
location. Calling this function decrements the steps remaining by the weight of the edge from the
current location to this node.
6. void grabGold(): Gold is picked up automatically from Pres Pollack’s location. Do not call this
method.
In order to get out, return from method scram() while standing on the exit. Returning while at any
other position, or failing to return within the required number of steps, causes the application to end with
a score of 0.
The cavern ceiling will collapse after Pres Pollack has taken a number of steps given by stepsLeft().
The steps remaining is decremented by the weight of the edge traversed when making a move, regardless
of how long Pres Pollack spent deciding which move to make. You are guaranteed that Pres Pollack can get
out of the cavern if she takes the shortest path out.
Whenever there is gold on Pres Pollack’s location, it is automatically picked up. There is no need to call
method grabGold(). DO NOT CALL THIS METHOD.
3
Class Node and the corresponding class Edge has methods that you are likely familiar with from A7.
Look at the documentation or code for these classes in order to learn what additional methods are available.
A good starting point is to write an implementation that will always get out the cavern within the given
number of steps. From there, you can consider trying to pick up gold to optimize your score using more
advanced techniques. However, the most important part is always that your solution successfully gets out
of the cavern —if you improve on your solution, make sure that it never fails to escape in time.




