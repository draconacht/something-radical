---
title: miscellaneous interview questions
date: 2024-07-27T18:30:00.000Z
draft: true
---

questions for interview for SDE freshers

## OOP

### Collision Checker

there are N shapes in a 3D space. you do not know what shapes these are, but they will be either (both) Spheres or Cubes of varying edge length and radius. find all objects that do not collide with the **first object** (the full problem is a practice in graphics algorithms, not OOP).

#### story variations

* collisions in a shootemup  / platformer / bullet hell game
* find if cab drivers are in contact distance of a person to send a notification
* find if a user is in service radius of telephone towers / banks / train services

#### advanced version

* the shapes may be different. add more shapes if you feel that the equations will be simple enough. this will require an arbitrary equation solver to be provided.

#### things to look out for

* did they implement inheritance / interfacing correctly?
* did they put proper variables in the classes? are they properly scoped (this depends on the language being tested)
* did they make a proper checking function? this could be a comparator or an equality check.

### Mail Relay

firefox relay is a service that relays mails automatically from a dummy inbox to an actual inbox. design classes such that

* a dummy account cannot be logged into, but it can generate a view
* mails in a dummy account are automatically forwarded to a real account. mails in a real account have no forwarding behaviour. this behaviour can be enabled or disabled at will.
* a dummy account can only have a mozmail email, but a real account can be from any host.

#### things to look out for

* did they implement inheritance correctly?
* did they put proper variables in the classes? are they properly scoped? (this depends on the testing language)
* did they use proper design patterns? are they failing shut?

### Iterators

create iterators that allow me to iterate over other kinds of classes. explain how you would connect your iterator to a stack, a queue, and a heap. also create an iterator that return the inverse of every element. name the design patterns applied here if you can.

#### advanced version

* the inverse function should be generic and implemented by the datatype of the iterator

#### things to look out for

* did they implement composition / adapter correctly?
* can they named the used design pattern/s?

## Data Structures & Algorithms

### Dependency Manager

there are N tasks, with dependencies in pairs of (nx -> ny). each package has an init function that's run to set up the code in it. find a correct order in which the init functions must be executed to avoid dependency issues.

#### story variations

* baking a cake, or cooking in general
* hiring people in a company
* course prerequisites in a university

#### advanced versions

* find circular dependencies, and minimum number of dependency removals required for the code to work \<bridge edge algorithm>
* implement versioning validation. assume every package has a dependency of  vy >= v >= vx. verify if it is possible for the code to run.

#### things to look out for

* did they correctly structure the problem as a directed acyclic graph?
* do they know the algorithm/s that are being searched for?

### SuperKnight

a superknight is a combination of a knight and bishop. it can either move in an L shape like a regular knight, or (exactly) two squares diagonally. find the least number of turns it will take for a superknight to move from square X to square Y.

#### advanced versions

* can a superknight on square X capture a pawn on square Y before it promotes? the pawn moves one square every turn. what is the earliest that it can capture this pawn? \<modified dijkstra>
* pieces are arranged on the board as \[(S0, P0), (S1, P1), (S2, P2)...]. what is the most material that the superknight can capture in N turns? assume regular chess material values. \<knapsack>
* \[very hard] there is one enemy rook on the square S. can a regular knight traverse all squares on the board that are not under threat \<requires foreknowledge of knights tours>

#### things to look out for

* did they structure the problem correctly as a graph?
* did they know the correct algorithm / approach for the job?
* could they adapt to the new constraints?

### Currency Conversion

given a mapping of currencies' exchange rates \[(a, b, 1.5), (b, d, 3)...] find the exchange rate between currencies x and y.

#### advanced versions

* solve the same problem in O(1) time and O(N) memory. preprocessing can be done with any particular time with one run.
* rather than currencies, this problem is about distances. given roads connecting N points, find the shortest paths from any p0 to p1 in O(1) given preprocessing is allowed.

#### things to look out for

* did they structure the problem correctly as a (bidirectional) graph?
* were they able to solve the problem within memory constraints?
* were they able to grasp on the kind of advantages preprocessing would give them?
* could they at least provide naive solutions of O(n^2) memory usage?

### UTF-8

given a utf-8 bytestream known to be in english, decode it such that you get a version with the minimum number of garbage characters. each utf-8 character is two bytes. if a part of a byte is garbage, you can consider all of it to be corrupted. for the sake of simplicity, assume you can tell in O(1) if any byte pair is valid english utf-8 or not.

#### things to look out for

* did they currently identify it as a dynamic programming problem?
* did they pre-process it in blocks of two?
* were they able to identify it correctly as just (pick two non-consecutive blocks)

## OOP - Objective

* in java, object variables are private by convention. in python, they are public. what effects does it have on the code? which one do you find to be more elegant and why (you will not be judged on your opinions here, just the quality of observations)
* what is the role of the garbage collector in programming languages? how do languages without a garbage collector function and what kind of drawbacks / benefits might this have?
* if a variable is private, then how does the debugger know its value? \<segue into other questions about reflection>
* what is the role of decorator annotations in java / python? what

## DSA - Objective

* a printer needs to make sure it can print n documents from an incoming stream without dropping any entries. what data structure do you use in this situation? followup: what parameters would you need to estimate how large this queue should be?
* in a large office building (25 floors), most of the people working on higher floors use the parkings. should the elevator doors on parking floors and office floors be on the same side or opposite side when (1) the parkings are in the basement (2) the parkings are elevated?
* you are 5 TAs trying to sort answer sheets of the 2022 batch. you have 500 answer sheets (roughly evenly distributed between sections). how would you perform this quickly?
* implement a code that gives me the top 3 most frequent words in a paragraph. suggest multiple approaches and their advantages / disadvantages

## General

* talk about a conflict that you resolved during an internship with someone on your team.
* tell me what your role was in this project on your resume.
* explain to me what you did as you would to your tech lead, and as you would to your project manager.
* you think X. i am your manager who thinks Y. how would you go about correcting my misconception. this only works in the middle of some other questions.
* ask them to explain something about something that they claim to be good at. security, co, cn, toc, etc.
* how would you go about debugging a piece of faulty code? (i would love to have had actual flawed code for this but alas)
