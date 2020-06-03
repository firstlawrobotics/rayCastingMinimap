## PyRayMinimap - Python Raycasting Engine

PyRay is a ray casting engine (http://en.wikipedia.org/wiki/Ray_casting) written in Python using the PyGame library (http://www.pygame.org/wiki/about). Code forked from https://github.com/oscr/PyRay.

I added a miniMap function that identifies cleared space, dead space, and walls and implements a decay function for cleared space to force agents to reprioritize it. I won't ever do anything with this because I don't have the money to train my toy reinforcement learning agents so either give me money or fork this. 

### Screenshots


## Heatmap Enabled Minimap with Decay Function Enabled

This shows a view across the screen of an uncleared obstruction.

![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/before.png)

## Map After Clearing Dead Space

![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/cleared.png)

## Behind the Scenes
![In game screenshot](https://raw.githubusercontent.com/firstlawrobotics/rayCastingMinimap/master/screenshots/a.JPG)


### Resources
* http://www.permadi.com/tutorial/raycast/
* https://lodev.org/cgtutor/raycasting.html


