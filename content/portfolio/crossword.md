+++
image = "img/portfolio/gravity-paper.png"
showonlyimage = false
date = "2021-11-05T19:44:32+05:30"
title = "Crossword Puzzle Solver"
draft = false
weight = 2
+++

<!--more-->
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


This was a group project among three people. One of the first things we needed to consider was how to fill the graph input file. We primarily considered word-by-word instantiation rather than letter-by-letter instantiation of the grid. A letter-by-letter approach would try to fill the grid one letter at a time and would not be as efficient as filling the grid with a valid word at a time. The aim was to maximize the number of potential words remaining in the grid, so we'd have more options for filling in the grid. To tackle this is in the most constrained approach, we choose the empty word pattern which could be filled by the minimum number of words from the provided dictionary.
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}

Next, when picking the words we had to choose between words that are the same length as the empty word pattern, and those that match the current number of letters already filled into that word (if there are any). Using that information we had to determine which of those options would have the most dictionary matches. This strategy essentially leads to choosing words that will maximize the number of choices for the other words in the grid. To make searching for words more efficient, we wanted to order our dictionary by length and restrict our search to that subset of the dictionary which contains words of the same length of the pattern we are trying to match. Punctuation and case was removed/ignored.
{{< rawhtml >}} 
<br>
{{< /rawhtml >}}

Finally, to minimize the amount of backtracking and the efficiency of the program, we checked for arc consistency (i.e. made sure it's possible to fill the graph with valid words) after every word was filled in.