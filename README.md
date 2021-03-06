# Workshops

### Seattle Ruby Workshops.

Feel free to fork this repo and code away!

Session I: Game of Life (gol)
=============================

Table of Contents
-----------------

- [GOL](#gol)
- [Rules](#rules)
- [How to go about it](#how-to-go-about-it)
- [Visualization](#visualization)
- [Restrictions](#constraints)
- [Resources](#resources)

GOL
===

<p><img class="left" src="/public/images/Game_of_life_pulsar.gif" width="200" /><br/>
“Game of life pulsar” by JokeySmurf <a href="http://commons.wikimedia.org/wiki/File:Game_of_life_pulsar.gif#mediaviewer/File:Game_of_life_pulsar.gif">Licensed under Public domain via Wikimedia Commons</a></p>

bla bla bla


Rules
=====

Game of Life "exists" in an infinite two-dimensional orthogonal grid of square cells, each of which is in one of two possible states, dead or alive. Every cell interacts with its eight neighbors, which are the cells that are directly horizontally, vertically, or diagonally adjacent. At each step in time, the following transitions occur:

- Any live cell with fewer than two live neighbours dies, as if caused by underpopulation.
- Any live cell with more than three live neighbours dies, as if by overcrowding.
- Any live cell with two or three live neighbours lives on to the next generation.
- Any dead cell with exactly three live neighbours becomes a live cell.

The initial pattern constitutes the seed of the system. The first generation is created by applying the above rules simultaneously to every cell in the seed. Births and deaths happen simultaneously, and the discrete moment at which this happens is sometimes called a tick (in other words, each generation is a pure function of the one before). The rules continue to be applied repeatedly to create further generations.

Check online an [interactive example](http://pmav.eu/stuff/javascript-game-of-life-v3.1.1/)

How to go about it (testing)
============================

How do we know that our code of GOL is behaving as it should? The intuitive answer is because we can see with our own eyes how cells are created and destroyed at each moment. We see how they evolve, therefore we believe it works.

The reality is that it is not necessary to see to believe (although it surely helps!). It is all about testing. So make sure you test well! Testing is an art in itself.

For example, start by implementing an empty game, then add the simplest scenario and start adding the four rules of the game.

Check example of tests here:
  - A new game has no cells
  - A new game after a tick ... nothing changes
  - A new game, when I add a new live cell, after a tick the single cell dies alone
  - A game with 3 cells distant from each other (0,0 : 0,10 : 20,20), after a tick, they all die!!
  - A game with 3 cells in a row (0,1 : 0,2 : 0,3), rotates as the clock ticks, and 3 cells always remain!
  - A game with 3 initial cells in L formation (0,0 : 0,1 : 1,0), after a tick of the clock, we have a solid block of 4 living cells.
  - A game with a block of 4 cells (0,0 : 0,1 : 1,0 : 1,1), stays stable and does not change as the clock ticks.

To put the cherry on top, feel free to tinker with and add the visualization tool explained below.

Visualization
=============

Ryan Davis has been generous enough to add the following ...

You can find the code inside the folder ``coding_tools/gol_visualization/". Check the README file to see how to use it with your code.

Constraints
============

Once you are familiar with the Game of Life, and you have your own coding solution, the fun begins. In the workshop we will recode GoL from scratch but with additional constraints. Possible constraints are:

* **Methods cannot have more than 3 lines**.
* **No conditional statements**. Be creative and find other ways to achieve the same results (i.e. type-based polymorphism, lookup tables).
* **No primitives** across method boundaries (input or output). Cannot pass around data primitives (booleans, numbers or strings). Neither you can pass primitive data structures such as arrays, lists or Enumerables.
* **Mute ping-pong pairing**. Like what Aaron and Ryan did last month with the Gilded Rose kata. One writes the tests, the other writes the code to pass those tests. They can only communicate through tests and code. Comments not allowed.
* **No return values**. Your methods cannot return values. Instead, use message passing between objects.

* **Object Calisthenics**. You can find even more possible constraints in the document included in public/ folder: "9 steps to better software design today", by Jeff Bay:

>> 1. One level of indentation per method
2. Don’t use the ELSE keyword
3. Wrap all primitives and Strings
4. First class collections
5. One dot per line
6. Don’t abbreviate
7. Keep all entities small
8. No classes with more than two instance variables
9. No getters/setters/properties

We will summarize the best constraints in the Wheel of Misfortune for you to play with. Nevertheless, you are free to pick and choose whatever constraints you want to apply, so feel free to be creative.

Resources
=========



