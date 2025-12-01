![Bear 5](https://i.redd.it/nnbts9yndp6b1.jpg)

# FGCT4015 - Fundamentals of Games Development

## HorrorThing

Name: Conner Reece Vian

Student NO : 2500411

Date: 5/12/2025

[Repository Link](https://github.com/GingerNinjaProgramming/HorrorThing)

[Build Link]("")

### Project Outline

My project at its basics will be a 3D horror game where you as the player have to get from point A to point B without dieing to a monster / monsters. Its concept will be closely tied to common horror game elements and mechanics like poppy playtime, lethal company or even more recently R.E.P.O. The greatest challenge for this will be ensuring the game functions and has a good horror atmosphere as this is both my first proper unreal project along with being my first horror game.  

## Research

### Methodology

During my research for this project I decided to broden my research scope a bit wider between the more technical side of the project and the other parts of the project as it related to design. I made this decision as considering the project was to be made in unreal which has a lot more tool to handle basic applications of mechanics it gave me a lot more time and space to attempt some of the other facets of game dev that could not be done in something like raylib where the primary focus was to actualy make the game functional (CITATION NEEDED).

I am going to attempt to get play testing on my game once it has some form of semi-complete version to be able to improve the game further from that point along with general peer reviews over the course of development to get more ideas on the project while working on it and getting more ideas once the game has a version to be tested. I will doing it this way as due to the nature of unreal and the project itself it has a lot more value to test later in development as to test a more complete products and to be able to get a good idea of if the horror feeling is being presented correctly to the person playing it. 

### Sources

#### Mastering C++ a Beginners Guide

When doing research for this project I first looked at material on C++, as this was my first major time using C++. One such book was  __Mastering C++ a Beginners Guide__ (Bin Uzayr, 2022). I did this to help improve my C++ knowledge as at the time this was a new language to me and though familiar with programming I wanted to be sure that I don't miss any syntax differences between C++ and another language like C#.I used this source as a beginner in C++ it seemed easy to pick up and learn from along with being advised this book via word of mouth from people in my studies. I learned many things about C++ reading from this books including:

* Vectors
* Pointers 
* Data Types
* Header files
* C++ OOP techniques

This book was very useful in my early C++ journey allowing me to iron out the details and differences between C++ and any other programming languages giving me a good starting point to start coding in raylib. However, by its very nature, being a beginner guide it does not break down everything and a lot of other things still had to be learned from experience / prior knowledge so while being a good spring board for work many things still had to be learned from other means like in person lectures.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/DownwellGameplay.jpg)

Figma 2 - Frame of Downwell gameplay

#### Downwell - The Game

Along with above during my research I looked into a game called downwell to see if I could get any ideas from a preexisting work similar to what I want my own project to be like which has achieved popularity (Downwell (video game), 2025). I learned some things from doing this that would help inform my game as it went further from research to actually making including:

* Enemy Types
* Main Loop
* Techniques to make more fun
* Keep simplistic 
* General Art Direction 

This research was useful as in the space my games DNA shares a lot of similarities to this game and considering the fact that this game did this formula successfully it makes sense to take information from the best contenders in the space. A downside of the research is in hindsight it may of allowed the scope of the game to grow to a place where it did not reasonably need to be where, though I aim to make something good understanding my personal limitations is something I need to keep in mind to allow me to scope my project reasonably. Along with this researching all of this gave no actual info on how to implement these features leaving it more up to me to learn as I went though my creative journey.

#### Raylib Cheat-Sheet / Documentation

I also used the official raylib (raylib | A simple and easy-to-use library to enjoy videogames programming, s.d.) documentation and cheat sheet (raylib - cheatsheet, s.d.) as some of my sources when working on this project. This felt right as considering raylib is the framework (Raylib -- Easiest C/C++ Game Framework -- Now Even Better For Beginners!, 2024) im using for this project so by occam's razor would suggest that the offical documentation would be the best place to start when looking for infomation on raylib. On this documentation it:

* Directed me to other raylib libraries that I used **[See External Libraries]** 
* Gave me a place to see a lot of base raylib functions 
* Acted as a HUB to find other useful information and tools

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/RaylibCheatSheet.png)

Figma 3 - Showing undescript nature of the Raylib Cheat Sheet

This research was helpful in my project as it helped inform me the basic functionality of raylib and how to get something functional setup to start working on. It was also positive to the development journey of my project as it helped direct me to other tools to that would go on to help me later. A downside of this source/s is that when it came to the cheat sheet it was not very in depth on functions on what they did more just having the function signature with a brief comment leaving me to sometimes have to do testing on how the functions work more precisely or going to other places to find what these functions do to see if they can fix my problem.


## Implementation

### Process

Describe your technical and creative approach, including:

* Planning, ideation, and iteration
* Feedback received and how it was integrated
* New tools, workflows, or systems explored

here

### New Approaches

This project was my first time using C++ and it led to new discoveries about computer programming and the hidden detail behind it as is expected from a lower level language that works closer with the computers hardware unlike another language like C#. Along with this it was also my first time using raylib and compared to other tools I have used in the past like unreal and unity, raylib was a lot more a DIY programming experience with a lot of the things you take for granted in a normal engine being things you have to manually make yourself like for example collision systems which while raylib has features to allow for collision it is still something you have to build yourself. This does however allow for a lot more creative expression in your system as it is completely up to you how these systems are designed allowing you to create them to the needs of your project rather than having to mess around with pre-made systems that may not completely fit the needs of your project. One early thing i relised when doing the rendering for my project is that as computer screens draw from left to right row by row the rendering in code adhears to this rule as well making for some interesting things that needed to be accounted for in code. These being that the y value increased as you went down instead of as you move up as is typical in most game engines meaning the coord (0,0) in space actually represents the top-left of your screen rather than the bottom left as would be expected typically, then as well when it came to drawing objects on the screen it would be drawn using the x and y as the top left point of the element then drawing the width and height right and down from this point. This meant when it came to determining exact positioning of elements on the screen extra logic needed to be implemented to get the center point of anything in the screen to ensure that when it came to things like collision checking it was using the accurate positioning of the character at the time.

### User Testing

- Talk about how users felt on first test
- Show data
- Talk about second test / benchmark
- Qualitive and Quantitive 
- Guided or non guided 

When it came to user testing admittedly this is one of the weaker parts of my project but despite this I still have some user testing at the start of my project and nearer to the end of my development cycle. 

## Instructions to Install / Run

To run the project [Download Zip](Pocket-Dropper.zip)

Then run the **.exe** inside of the extracted Zip file

## Reflection 

### Research Effectiveness 

The research into downwell and C++/Raylib as a whole was very useful on the general approach to the game in the first place along with the actual programming work on raylib which aided in the early development of the game. Along with this the videos on raylib I watched proved mostly helpful in the development process. However admittedly some tutorials proved unhelpful as they were either too old to be applicable like with tutorials on the compiler (CITATION NEEDED) or the mechanics being shown/created were too spesfic to fit for the problem I had resulting in some wasted time going back and forwards though a video just to relise it was not what i needed anyway before making it myself.

### Positive analysis

On my positive reflection, functionally this fits the brief along with including a lot of different concepts along with have a generally clean code thoughout the project. The game successfully shows similar mechinanics to what it is based off along with have animations, audio and mostly functioning mechanics. Additionally thoughout my code I managed to make it in a way keeping the systems modular and easily reuseable in other projects with little / no changes needed

### Negative analysis

On my more objective negative analysis, the game while functioning was not actually as fun as I wanted it to be and was not particularly fun nor did it have much re-playability. Additionally during the project I do not believe i worked on sprites/sound as much as I could of showing how the project lacks in these two areas. I belive this may of been due to lacking user testing early on in project and in the future i need to ensure i do more testing more often to give my game better direction.

### Next time

Next time Im going to try and focus more on early prototypes when working on the game giving more time on working on the games core mechanics and allowing time to make the core of the game fun to play before deep diving on making the code efficient. This would also further help solve my other problem as being able to generate good functioning prototypes as quick as possible as early as possible further helps gives me more user feedback which can then ensure a better project once I leave the prototyping phase. Along with this I think during my future projects I am going to try and consult more of my peers during development as I took a extremely independent mindset during the project which could of been to my projects determent especially in the fun department.

As far as whats guiding my intrests for future projects I had a lot of fun building reuseable and good systems that can be used thoughout my project and possibly to be used in later projects, when working on more projects thoughout my studies I want to continue to build more systems like this and possibly at some point build full on plugins and libarys for things like raylib,unreal,etc (CITATION NEEDED)

## Declared Assets

Version Control: **Git** / **Github**

IDE - **Blueprints / UE Visual Scripting** 

Engine - **Unreal Engine 5.6.1**


### Credits && Sources

* Sewers by Elbolilloduro (s.d.) At: https://elbolilloduro.itch.io/sewers 
* Horror Sound Effects by YourPalRob (s.d.) At: https://yourpalrob.itch.io/must-have-horror-sound-effects 
* Hazard Light - https://fab.com/s/945562072e7c 
* Eyeball PSX model by Leipea (s.d.) At: https://leipea.itch.io/eyeball-psx 
* Industrial Wall Light - https://fab.com/s/364544615d02
* PSX/PS1 Flashlight – Low Poly Retro Horror Asset by Norenwind (s.d.) At: https://norenwind.itch.io/psxps1-flashlight-low-poly-retro-horror-asset 
* EMERGENCY EXIT LOW POLY - https://fab.com/s/e1468cd0b0e2
* PUT MIXAMO LINK HERE (CITATION NEEDED)


## References 

### Game Sources 



### Academic Sources 


### Documentation Sources




### Other



