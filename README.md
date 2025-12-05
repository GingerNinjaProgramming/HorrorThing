# FGCT4015 - Fundamentals of Games Development

## Weeping Sewers

Name: Conner Reece Vian

Student NO : 2500411

Date: 5/12/2025

[Repository Link](https://github.com/GingerNinjaProgramming/HorrorThing)

[Build Link](https://gingerprogrammer.itch.io/horror-game)

### Project Outline

My project at its basics will be a 3D horror game where you as the player have to get from point A to point B without dying to a monster / monsters. Its concept will be closely tied to common horror game elements and mechanics like poppy playtime (Poppy Playtime on Steam, s.d.), lethal company (Lethal Company on Steam, s.d.) or even more recently R.E.P.O (R.E.P.O. on Steam, s.d.). The greatest challenge for this will be ensuring the game functions and has a good horror atmosphere as this is both my first proper unreal project along with being my first horror game. This game will be matching the theme of "Very important Object" by having the actual flashlight the player uses being a very important object.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/repo-game.gif)

Figma 1 - Gif of R.E.P.O character die

## Research

### Methodology

During my research for this project I decided to broaden my research scope a bit wider between the more technical side of the project and the other parts of the project as it related to design. I made this decision as considering the project was to be made in unreal which has a lot more tool to handle basic applications of mechanics it gave me a lot more time and space to attempt some of the other facets of game dev that could not be done in something like raylib where the primary focus was to actually make the game functional.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/Blueprintsexample.png)

Figma 2 - Image of an example of unreal blueprints

I am going to attempt to get play testing on my game once it has some form of semi-complete version to be able to improve the game further from that point along with general peer reviews over the course of development to get more ideas on the project while working on it and getting more ideas once the game has a version to be tested. I will doing it this way as due to the nature of unreal and the project itself it has a lot more value to test later in development as to test a more complete products and to be able to get a good idea of if the horror feeling is being presented correctly to the person playing it.

### Sources

#### Design patterns : elements of reusable object-oriented software

When doing research for this project as I wanted to push my knowledge and technical knowhow further I picked up this book on design patterns to better understand how to make my code cleaner and more organized along with understanding common development solutions to common problems in development. While being familiar with a lot of these patterns on a surface level this book really helped me understand them on a further level. These patterns included but are not limited to:

* The command pattern
* The factory pattern 
* The observer pattern
* ETC

This book was useful to understanding these high level programming patterns on a higher level along with introducing me to patterns and concepts that I had not heard of prior to this project. However one downside to this is due to the pure multitude of information in this book I may of overloaded my knowledge pool with too much some of which admittedly was less useful to my actual project than others.

#### R.E.P.O / Lethal Company - Horror/Comedies?  

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/RepoImg01.png)

Figma 3 - Image of R.E.P.O gameplay

Further examination and research for my project took me to multiplayer horror games like R.E.P.O and Lethal Company both games doing something similar mixing a horror multiplayer experience with a comedic moments with friends turning the game into a very complex blend of horror and action comedy. These kind of games peaked my curiosity in the research for this project for two reasons. One how they could mix such widely contrasting themes and make it work so well with both games doing it in a different but entirely unique way. Two how these games could have so many different AI systems running separately from each other while still having the game feel like it makes sense and understandable to the player, playing the game. This discovering pushed me to watching videos by youtube channel [**alter ego**](https://www.youtube.com/@alteregosocial) (alter ego, s.d.) who does breakdowns on the inner workings of the AI which was very interesting to watch to understand how these games work on a deeper level. From this I learnt some important facts about how they keep the systems advanced while still making sense and being manageable

* Many enemy share similar base behavior
* These systems use interfaces and base classes to allow sharing of functionality
* Most systems in these games use a combination of simple concepts to give the illusion of complex AI
* The cause and effect is very well read for the player to better understand the AI

This deep dive was very useful for this project and later projects as mainly for the context of this project it gave different ideas of enemy's that could be in the game and though in the current game there is only one enemy it helped inform how the enemy is coded and the potential future of the game if i were to walk more on it.

#### Unreal Engine Documentation

Throughout my project I also ,as is obvious when using a engine, looked though the engines documentation on how different nodes and systems work inside the engine. This was useful when I was having a problem with certain functionality in the engine and needed clarification on what something is doing for example with unreal's inbuilt timeline node which at a point in development I was struggling with though searching the documentation I found what the problem was (this being that is runs on actors and not widgets) (Timelines in Unreal Engine | Unreal Engine 5.7 Documentation | Epic Developer Community, s.d.). This documentation helped with:

* General problem solving
* More technical questions to how the systems worked
* Finding new nodes that could help solve problems
* ETC 

Using the documentation was useful for solving specific problems with nodes and functionality in the engine during development. However one main problem I found, similar to when i was working with the raylib cheat-sheet in a previous project (Vian, 2025), as the documentation is essentially a massive spread sheet for specific problems it was sometimes difficult to find what I was looking for without being directed to it from another source along with this some documentation was not a precise as I would like forcing me to find the answer though other means. However for the most part the documentation was very useful

## Implementation

### Process

When I was planning this project I wanted to push my understanding of games development while also giving me a creative outlet and viable reason to use some more of the advanced tools unreal provides

Coming into this project I had beginner level experience using unreal visual scripting blueprints therefore throughout this project rather than learning unreal on a basic level and working around that I wanted an excuse to use some other of unreal's features and this helped inform my creative approach

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/PoppyPlaytimeWP.png)

Figma 4 - Weeping Angel archetype example Poppy playtime

I began project development using the base horror template from unreal while not using majority of the things this offered it was a great help in giving me a general idea on how things should look and providing some useful pre-made assets that I used in my project.Along with this I downloaded many assets of itch.io and made a base map with them.

From there I worked on base interactable objects in the game scene and creating the code for the player to be able to interact with the objects. These two objects included a door that the player would interact with to open and a flashlight pickup which the player could interact with to gain the flashlight to use. To allow for this I created a interface (Interface (object-oriented programming), 2025) in unreal called **BPI_Interactable** with a singular function called interact. This interface was then given to both the door and light pick up with unique implementations of the function on both objects.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/BPI_Interactable.png)

Figma 5 - BPI_Interface in question

* One simply triggering a function to open/close the door

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/DoorOpenBlueprint.png)

Figma 6 - Door opening interact function

* Other to update a boolean on the player BP to represent having the light

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/LightPickupBlueprint.png)

Figma 7 - Light Pickup interact variation

This was useful as instead of looking for a specific object to interact the player in its blueprint could just cast a base line trace when the interact key was pressed and then attempt to run the interface's interact function though whatever the hit actor was this meant that due to the nature of how interface function calls are treated in unreal engine the player would attempt to call the interact function on whatever actor it hit if it actor did have a implementation of the function it would run normally or if it didn't then no errors would be thrown as unreal treats these kind of calls in the same way an event would be called.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/PlayerInteract.png)

Figma 8 - Player interaction segment.

Another of the main things I worked on for this project was an AI character and early on in the development process I decided to make an enemy AI replicated the weeping angel archetype. This being a concept originating from monsters from the doctor who series (Weeping Angel, 2025). In doctor who they are depicted as gargoyle-like human statues which can only move when the doctor is not looking at them directly. This behavior has been replicated in many games like the boos from mario by Nintendo (Boo | Mario Wiki | Fandom, s.d.) ,which would stop moving and cover their eyes if mario looks in their direction, or the endo-skeletons (Glamrock Endo, 2025) in FNAF Security Breach By SteelWool (How To Beat Endoskeletons In FNAF Security Breach | Easiest Way, 2021).

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/super-mario-world-big-boo.gif)

Figma 9 - Example Of Boo hiding on player sight

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/Endo-12-04_032324328.png)

Figma 10 - Example of Endo Paused in motion

For actually making the AI I used a the built in tools provided in unreal of the behavior tree and blackboard combo. The behavior trees managing the main logic where the blackboard acts as a global store for all functions and tasks inside of the AI, these values are stored in key value pairs. Along with this I created a character blueprint for the character in the scene and to control the actor it has a AI controller which is a child class of the base controller with extra bells and whistles for AI functionality. Most of logic for the AI is handled in the AI controller which then points to the behavior tree to tell it what to do.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/WPFiles)

Figma 11 - Files for AI Unreal

The behavior tree its self consists of a couple different states that get switched determined on external factors of the scene and how the player interacts with the AI. The AI has four main states with one sub state. These main states being wandering,chase,stop and kill the player for main with the sub state being the investigation phase inside of the wander phase which triggers if the AI is to hear something or just lost sight of the player to which it will go to where it heard the sound / last saw the player. The main phases are quite simple in theory. The wander phase has the AI randomly moving around its area defined by the navmesh till it gets some form of stimulation to move into the the sub investigation phase or gains sight of the player and begins the next phase. The next phase to happen depends on circumstances where the AI will run a player detection check to ensure that player cannot currently see the AI as this is a weeping angel if it were to play it would break the illusion.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/CheckPlayerDetection.png)

Figma 12 - Code for checking player detection of AI 

This is done by tracking if the player is looking at the enemy using vector dot comparison and if the player is looking in general direction of the enemy along with checking if the players light source is on as if it was off the player would not be able to see the enemy anyway even when the player is technically looking in its direction. If one of these is not true the branch outputs a false which outputs that the player cannot see the enemy in the form of a boolean which can then be used on the tree to allow the chase behavior to function. If the check goes true the player does a sphere overlap by actors using the players lights attenuation radius as a radius as this defines how far the players the light should be able to affect objects if its on meaning for the player it acts as a type of view radius as other than the light the scene is mostly pitch black. After this all hit actors are looped though and checked if they are the enemy. If any of these actors are the enemy, the boolean is returned to represent that the enemy is in players sight line thus player can see the enemy. However if the loop manages to complete meaning all elements in the hit array were checked and were not the player then the other boolean gets returned meaning the player cannot currently see the enemy despite looking in its general direction and having the flashlight 

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/BTWP.png)

Figma 13 - Enemy Behavior Tree

Depending on the output of this behavior one of two things happens. If the player cannot see the enemy, the enemy begins its chase behavior which just has the enemy moving the players direction at a constant motion until its close enough to the player. At this point it will wait till the player is not looking in the players direction and the tree will initiate the kill behavior and well **Game Over**.

The other behavior is relatively simple this just has the enemy stop all motion and erect a different randomly selected pose with a stinger sound played alongside to give the feeling of it suddenly stopping even if the player never would of seen it in motion but a statue just switching from one position to another.

![image](https://file.garden/aSY-yx_ZmANpQe1l/Pocket-Dropper-Ref/EnemyKillWP.png)

Figma 14 - Enemy Kill Frame

All of these behaviors come together to make a relatively believable monster in my game that will find you, hunt you and kill you without you ever seeing it truly move until its too late.

### New Approaches

This project was my first time using unreal on such a scale / my first time using unreal with the express purpose of making a functioning product because of this I had a couple different new experiences when working on this product including map creation, higher level blueprint and working with unreal behavior trees when it came to working with the AI functionality in unreal. This came with some new discoveries including the idea of a selector,sequence and decorator,all of these things I have learnt throughout my process of working on this project.

### User Testing

When it came to user testing admittedly this is one of the weaker parts of my project but despite this I still have some user testing at the start of my project and nearer to the end of my development cycle. I had a small amount of people review my project but early on my project I had a small scale guided play test with a couple of my peers and they gave useful advice that would inform later changes to game as it was further developed. This included:

* Making the scene more visible
* Making the player a bit slower as the player could blitz though the level
* Other minor bug fixes

This helped ensure my game had a good direction of progress for further development as I got this advice early in my projects lifecycle.

In my later test I did with a small group of people my game was found to be functioning with everything that was done in the game functioning as expected and the players reacted and did what I as a developer expected/wanted them to. However one of the main problems was my game in its current state does not offer much content outside what is already inside the game linking back to my examples of games like R.E.P.O or Lethal for future development my game could include:

* More enemies 
* Bigger Map
* More Unique things for a player to do

In the future I need to make user testing more a focus but for the infomation I got for this project I did help with the projects with lifecycle ensuring it could be as good as possible in the time given

## Instructions to Install / Run

To run my project:

Go to the itch.io page for this game using this [link](https://gingerprogrammer.itch.io/horror-game)

Follow the steps outlined on the itch page

## Reflection 

### Research Effectiveness 

The research I did for this project in hindsight may of been not as efficient as I would of liked due to the fact I feel as is a common for my projects my scope seems to escape me which then has me doing research on topics and ideas that do not scale to the project I am currently making. Therefore while the research I was doing would be good in theory due to my own personal scaling issue a lot of the really interesting research and information falls on death ears. However for my AI work my research was quite effective as I found a very in depth youtube tutorial ((195) Learn all About AI in Unreal Engine 5 - YouTube, s.d.) which helped explain all things I needed to know about unreal's AI systems. Along with this I found a very useful youtube channel ((195) AI and Games - YouTube, s.d.) that broke down a lot of AI systems and characters from different games in a concise and informative way.

### Positive analysis

On my positive reflection, my projects AI was well constructed and ,aside from some minor errors, functions the way I expected when I begun working on it. Along with this the general functionality of the features I attempted to implement came out close to if not more or less exactly how I wanted them to work when they were conceptualized. Along with this for the most part the code quality was kept relatively clean and readable throughout with the use of node organization and interfaces to split logic in reasonable places 

### Negative analysis

On my more objective negative analysis, my project could of done with more diversity in enemy's and a larger and better designed map as my game in its current state does not have a very complex map and the enemy in the game while well done is the only enemy in the game making it easy to abuse even with the fail safes built in. Therefore I believe with a more unique enemy to prevent some of the players behaviors it could stop the player from abusing the holes in the one enemy's ai and make for a more interesting gameplay experience for the player.

### Next time

Next time Im going to try and focus more making a lot more smaller systems and enemies in the game rather than spending all of my development time on large systems that are good on their own but as a whole in the project do not account for much. Along with this I will ensure I will use more user testing more often throughout the games development.

As far as whats guiding my interests for future projects I want to work more with the AI behaviors and systems mainly with the systems unreal allows making different more complex AI that do different things and force different gameplay behaviors in the player depending on what the game genre I am working on ensuring the AI made fits the needs of the game I am working along with in the process creating tools for allow for easier AI creation in further projects.

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
* Other models / Anims - https://www.mixamo.com/#/ 

## References 

### Game Sources 

R.E.P.O. on Steam (s.d.) At: https://store.steampowered.com/app/3241660/REPO/ (Accessed  03/12/2025).

Lethal Company on Steam (s.d.) At: https://store.steampowered.com/app/1966720/Lethal_Company/ (Accessed  03/12/2025).

Poppy Playtime on Steam (s.d.) At: https://store.steampowered.com/app/1721470/Poppy_Playtime/ (Accessed  03/12/2025).

### Academic Sources 

Perron, B. (2018) 'The World of Scary Video Games' pp.1–488.

Ulibarri, S. S. (2020) Unreal Engine C++: the ultimate developer’s handbook : learn C++ and Unreal Engine by creating a complete action game. United States? Stephen Seth Ulibarri. At: https://go.exlibris.link/k8dVkFcf (Accessed  03/12/2025).

Gamma, E., Helm, R., Johnson, R. and Vlissides, J. (2011) Design patterns : elements of reusable object-oriented software. Boston, Mass. Munich: Addison-Wesley Professional.


### Documentation Sources

Unreal Engine 5.7 Documentation | Unreal Engine 5.7 Documentation | Epic Developer Community (s.d.) At: https://dev.epicgames.com/documentation/en-us/unreal-engine/unreal-engine-5-7-documentation (Accessed  03/12/2025).

Timelines in Unreal Engine | Unreal Engine 5.7 Documentation | Epic Developer Community (s.d.) At: https://dev.epicgames.com/documentation/en-us/unreal-engine/timelines-in-unreal-engine (Accessed  03/12/2025).


Interface (object-oriented programming) (2025) In: Wikipedia. At: https://en.wikipedia.org/w/index.php?title=Interface_(object-oriented_programming)&oldid=1317009412 (Accessed  03/12/2025).


### Other

alter ego (s.d.) At: https://www.youtube.com/channel/UCpyp1kqWLfeD3cfLS6kBw5Q (Accessed  03/12/2025).

Vian, C. (2025) GingerNinjaProgramming/Pocket-Dropper. At: https://github.com/GingerNinjaProgramming/Pocket-Dropper (Accessed  03/12/2025).

(195) Learn all About AI in Unreal Engine 5 - YouTube (s.d.) At: https://youtube.com/playlist?list=PL4G2bSPE_8uklDwraUCMKHRk2ZiW29R6e&si=Uucd3HSQ4-WzFqm9 (Accessed  04/12/2025).

(195) AI and Games - YouTube (s.d.) At: https://www.youtube.com/@AIandGames (Accessed  04/12/2025).

Weeping Angel (2025) At: https://tardis.fandom.com/wiki/Weeping_Angel (Accessed  04/12/2025).

How To Beat Endoskeletons In FNAF Security Breach | Easiest Way (2021) Directed by E4F. At: https://www.youtube.com/watch?v=uxdwXyAZhH8 (Accessed  04/12/2025).

Boo | Mario Wiki | Fandom (s.d.) At: https://mario.fandom.com/wiki/Boo (Accessed  04/12/2025).

Glamrock Endo (2025) At: https://freddy-fazbears-pizza.fandom.com/wiki/Glamrock_Endo (Accessed  04/12/2025).



