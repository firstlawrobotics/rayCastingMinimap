## RayCast Minimap

Using basic raytracing functions (basically LIDAR) I added a miniMap function that identifies cleared space, dead space, and cover and implements a decay function for cleared space to force agents to reprioritize it. 

Basically, it allows an AI to know where it is in relation to other things it has seen and gives them a concept of cleared space and dead space. 

Long term plan is to combine this with a SLAM (<https://en.wikipedia.org/wiki/Simultaneous_localization_and_mapping>) algorithm and beat state of the art in any first person shooter out there.

I don't have the money to train my reinforcement learning agents so give me money please. 

## Heatmap Enabled Minimap with Decay Function Enabled

This shows a view across the screen of an uncleared obstruction in the bottom right.

Black indicates obstruction, and the colors gradient indicates how recently a space has been cleared, with darker colors being most recently. The map starts blank and is filled in as the agent looks around.

![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/start.png)


### Spin to Gain Orientation

One fast way to figure out what is going on is to spin around and determine where everything is.

![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/spin.png)


## Map After Clearing Dead Space

After that spin we have a decent idea of what the map looks like, but there is still a ton of dead space behind obstructions. 

![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/before.png)

In this example, we will go and clear the obstruction in the bottom right corner of the map.

![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/cleared.png)

After clearing the bottom right we have filled in our map and determined there is nothing else back there, but now the rest of the map isn't cleared anymore. 

This decay function can be used to shape an agent's behavior towards clearing intelligently. 

## Behind the Scenes
![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/a.JPG)

## To Do
The raycasting engine isn't great at detecting diagonal edges in this environment, so I could either rewrite the engine or go and find a better implementation. Not sure which I'd rather do. 

This concept, coupled with a basic SLAM implementation would likely be a SOTA FPS playing AI. 


### Resources
* http://www.permadi.com/tutorial/raycast/
* https://lodev.org/cgtutor/raycasting.html

PyRay is a ray casting engine (http://en.wikipedia.org/wiki/Ray_casting) written in Python using the PyGame library (http://www.pygame.org/wiki/about). Code forked from https://github.com/oscr/PyRay.




