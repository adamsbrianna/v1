+++
image = "img/portfolio/gravity-paper.png"
showonlyimage = false
date = "2021-11-05T19:44:32+05:30"
title = "Crossword Puzzle Solver"
draft = false
weight = 2
+++

<!--more-->
Fifth abundantly made Give sixth hath. Cattle creature i be don't them.
<!--more--> 

{{< rawhtml >}} 

<video controls width=100%>
    <source src="*/videos/crossword.mp4"
            type="video/mp4">
    Sorry, your browser doesn't support embedded videos.
</video>

{{< /rawhtml >}}

<!--more-->
Fifth abundantly made Give sixth hath. Cattle creature i be don't them.
<!--more-->

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

Step 1: Fill in    (Brianna)

To generate the crossword puzzle, we need to determine our algorithm for filling the graph. We want to consider word-by-word instantiation rather than letter-by-letter instantiation of the grid. A letter-by-letter approach would try to fill the grid one letter at a time and would not be as efficient as filling the grid with a valid word at a time. We utilize an english dictionary starting for now with just 5 letter words on grid.The aim is to maximize the number of potential words remaining in the grid which will maximize our ability to fill in the grid with the least amount of backtracking. To tackle this is the most constrained approach, we choose the empty word pattern which can be filled by the minimum number of words from the dictionary.

Step 2: Picking the words    (Monique)

When picking the words we choose between words that are the same length as the empty word pattern and match the current number of letters already filled into that word (if there are any) and decide between those options which have the most dictionary matches. Therefore, this strategy essentially leads to choosing words that will maximize the number of choices for the other words in the grid. 

To make searching for words more efficient, we want to order our dictionary by length and restrict our search to that subset of the dictionary which contains words of the same length of the pattern we are trying to match. Punctuation and case will be removed/ignored.

Step 3: Backtrack    (Cynthia)

To minimize the amount of times to backtrack and the efficiency of the program, we want to check for arc consistency (ie, making sure the graph is still able to be filled with valid words) after every word is filled in.

Approach: This project plans to use deep learning. We plan to train our system to rapidly generate crossword puzzles using a variety of optimization tactics which allows for faster generation of crossword puzzles. 

Plan: A qualitative approach will be used to determine the correctness of the crossword puzzle generator. We will analyze the result of the output of the program and if it is solvable.
