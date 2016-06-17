---
layout: post
title: More Evolution Strategies
subtitle: More super rad (read: not too boring) methods of Selection!
---
## Evolution Strategies vs. Genetic Algorithms! 

So, I promise this will be super rad. Maybe. Unless you've just stumbled upon this page and are like "Where am I? What is this place? Why do I exist?" etc. Regardless, I figured I should broaden the scope from the last post because it was super ultra narrow  in its scope. It was an incredibly quick and super rudimentary guide to [genetic algorithms](http://lanematthewj.github.io/2016-06-14-Genetic-Algorithms/). Take a gander if you haven't already. 

So, you're probably asking "Well, why does this say 'Evolution Strategies' instead of 'Genetic Algorithms Pt. 2' or maybe 'Genetic Algorithms Redux' (would've been a way cooler title). The reason as to why is because Genetic Algorithms are actually a subset of Evolutionary Algorithms (more words, huzzah!). There are a lot. I'll definitely be posting about at least one more after this (current area of research,  so that's neat, right?). Anyway, suffice it to say that you can look the whole picture as such: 
* Evolutionary Algorithm: Algorithms which learn and converge upon an optimal solution from selection, crossover, and mutation. 
  * Genetic Algorithm: "Genetic" being a key word here, the data are typically represented as a bit string (like we did in our one max).
  * Evolution Strategy: A bit more broad, the data are typically represented as an N-dimensional vector of real numbers. 
  * Genetic Programming: Why not talk about this now? (I have zero examples to show, but I'll add it here and then later if I actually write a post about it, then huzzah!). Genetic Programming is a system where a program itself is the "data" and the "genes" are actually blocks of code. The data is typically represented as a binary tree. What's super neat is that the code itself gets optimized. It gets heavy... 

Granted, aspects of each can get used in a program, which significantly blurs the lines. Robin Thicke's all about EAs. I try to be specific, but sometimes it's hard. If you catch me messing it up or just think that I'm wrong in general, please let me know!

So, now that you've read those and are now completely versed in the topic, let's venture back to the topic of the day: Evolution Strategies! Like the genetic algorithm from the previous post, the Evolution Strategies all follow a similar path (because they're all Evolutionary Algorithms!): Selection, Crossover, Mutation.  These too can get blurred... because science! It wholly depends on how your algorithm works. Some schools of thought suggest that we should only have mutation (which most definitely works, but just doesn't converge as quickly), while other schools of thought are very much about mutation and crossover. Crossover alone wouldn't be such a great idea because you'd prematurely converge on any local optima (we'll talk about that, promise!). Regardless of school of thought, we're going to be looking at for this time around are strategies which all employ mutation and crossover with differing methods of selection. 

Before we go any further, instead of having a bitstring like we did in the genetic algorithm, we'll be having a vector filled with some random real number values which correspond to our fitness function. Let's assume we have a fitness function f(x) = ∑<sub>i=1</sub><sup>3</sup> x<sup>2</sup>. Our vector will then have 3 values and, when randomly populated, look like:  
![](/img/geneticalgorithms/Vector.png)

Crossover works similary, except instead of transferring bits, we're crossing x-values. 
![](/img/geneticalgorithms/VectorCrossover.png)

Mutation for the ES vector is different from the GA. We can't just flip a bit like we did on a bitstring. So we have to have some mutation function to work with our alleles. Again, there are many ways to deal with this. We could choose a value within the bounds uniformly randomly, but that could potentially add too much noise (or at least more than we'd desire). The best way, as far as I'm concerned is to apply a take the given x-value and apply a gaussian distributed random value to it. 
![](/img/geneticalgorithms/VectorMutation.png)

## Tournament Selection 
We'll start with tournament selection. If you thumbed through the last post, you're familiar with this. We'll select N random chromosomes (typically 2 or 3) and tournament them against each other. The winner goes to the next round! 
![](/img/geneticalgorithms/TournamentN2.png)


Woops - accidentally published this before it was finished. Enjoy unfinished work, friend! I'll be back later tonight to finish it :P 



## Proportional Selection


## Ranking Selection 



