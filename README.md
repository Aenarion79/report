Practical For Programming Principles and Algorithms
===================================================
#Report by CS16038
-------------------

##Initial thoughts


As a true beginner i started writing the code at once.It became complicated in
just a few lines. Then i decided to do this the proper way.
At first i started making a generic plan in my head on what is Gemma supposed to
do.I used abstractions to create a list of things that Gemma had to do and
addressing each problem at a time by creating various methods.

//Find and pick up Giraia
//Find and pick up the priestesses Swestia and Seastia
//Find to the temple,leave the priestesses in the correct tiles
//Find the sorcerer
//Find the blood spring
//Throw the sorcerer inside the blood spring
//Find the white cave

###Movement

First of all Gemma had to start moving,so i created a move command, but movement
is complicated,i was not supposed to design Gemma to move on a specific map,so
her movement ought to be in small steps.So i made a 1 step movement method. As
we said earlier not all maps are the same,so her movement must be as if a blind
person walks in a room,i added randomness to her movement.

###Obstacles
Maps have various obstacles,such as creatures and walls.So i had to include an
avoid obstacles method.Walls are easy to overcome with a simple method but there
 are some rules for some of the creatures.
Some of them should be picked up until a specific part of the story,so i had to
divide the creatures to the ones that were part of the story and the ones that
were not.The ones that were not part of the story i named them
"possitive creatures".This way i created a method for Gemma to avoid storyline
creatures.Until time she need to pick them up.

//Move
//Turn randomly
//Move randomly
//Avoid obstacles
//Start looking only for Giraia,once found pick her up
//Look for Swestia,Seastia and pick them up


###Finding specific tiles

As the story progresses Gemma had to find some places on the map that
represented a Temple and a Blood Spring,the way to find those was by creating a
a method that found tiles with specific colors.

/Find temple
/Drop the the priestesses to the appropriate tiles
/Find sorcerer,pick him up and drop Giraia in his place
/Find Blood Spring and drop the sorcerer in the red tiles
/Find the white cave

Finaly i created a different map to see if it works on another tile set.I also
got some maps from fellow students for even more testing.

###Various problems that emerged in the process and how i solved them

Some times as Gemma moved randomly it moved the non story creatures and it
dropped them at the Temple tiles or at the Blood Spring tiles.If there were
possitive creatures at the tiles that storyline creatures ought to go, i could
not finish the story properly .So i made a method that before dropping a
storyline creature Gemma checked if it was occupied by any other creature and if
there was one it would pick it up in the cargo.

Another method i created was to check if the temple was actually the temple and
not a similar tile set.
