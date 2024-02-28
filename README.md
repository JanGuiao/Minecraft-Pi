# Minecraft Pi via RaspberryPi OS

Steps on how I setup Minecraft Pi via RaspberryPi OS | Executing commands via Python 

## Utilities 
- Windows PC Starter Kit
- Python 3 *use latest version* 

## Environments RaspberryPi OS

## Materials Necessary
- Raspberry Pi: Cost *$20-100* may vary
- Keyboard & Mouse
- Monitor *preferably dual*

## Getting Started 

- Install [PythonIDLE](https://www.python.org/downloads) *latest version*

- Download "Minecraft ver 1.12 Windows Starter Kit" zip file: [Windows Starter Kit](https://adventuresinminecraft.github.io/)

## Setup Process 

- Starting with the "Adventures in Minecraft-PC", make sure you extract the folder to your desktop.
- Open PythonIDLE, create a new file (file, top-right) and save the file to your "Windows Starter Kit" folder, specifically in the "MyAdventures" folder. *Inorder for your code to import itself to the server*
- Furthermore, navigate to your "AdventuresInMinecraft-PC" folder, and run "start.exe"
- Lastly, open your Minecraft Launcher (must have game purchased), switch to ver. 1.12 (compatibility),
- Start the Game
- Go to Multiplayer
- Direct Connect to localhost in **Connect to your server** 

## Video Demonstration: *can be done either Windows or with your RaspberryPi device connected to the monitor* -Demonstrated on Raspberry Pi

## "Hello World!" output in-game
Before inputting code, it is important to realize the "from mcpi.minecraft import Minecraft" and "mc = Minecraft.create()" command allows the connection between PythonIDLE and Minecraft.

- mc.postToChat("Hello World!")

https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/bf9f304b-2f56-4c75-b033-d4033210dc68

## PlayerPos & Teleport *Finding your location, coordinates separating variables, and teleport*

- "pos = mc.player.getPos()" helps to find your location.

- "x, y, z = mc.player.getPos()" alternatively, a nice way to get coordinates into seperate variables.

- "mc.player.setPos(x+25, y, z)" specifies a particular location to teleport to (also combine "x, y, z = mc.player.getPos()" beforehand).

https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/d28ac505-150a-4c7e-a527-345966e85f60

## Set Block *Placing a single block at a given set of coordinates* 

- "x, y, z = mc.player.getPos()" 
- "mc.setBlock(x+1, y, z, 1) to place a single block at a given set of coordinates.
  
https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/c770644f-19b0-459e-86c2-a71b349353bf 

## 10x10x10 Cube solid stone *As well as setting a single block with "setBlock" you can fill in a volume of space in one go with "setBlocks"*

- "stone = 1 (stone is 1 as a variable)",

- "x, y, z = mc.player.getPos()",

- "mc.setBlocks(x+1, y+1, z+1, x+11, y+11, z+11, stone)"

https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/f799c26a-4668-40eb-bfd7-d7f20ce6475a

## Dropping blocks as you walk (Flower) *Drops a flower behind you wherever you walk* 
Moving location to drop blocks when you walk.

- "from mcpi.minecraft import Minecraft"

- "from time import sleep"

- "mc = Minecraft.create()

- "flower = 38"

- "while True:"
-  "x, y, z = mc.plaer.getPos()"

- "mc.setBlock(x, y, z, flower)"

- "sleep(0.1)"

- using the command "CTRL+C" will stop the never-ending drop in flowers

![Flower](https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/4d7b9146-b424-44fb-875c-a575e943d04c)


   ## TNT *Interesting blocks like TNT; placing TNT, exploding TNT, and an exploding cube of TNT*
   
Playing with TNT by placing the block, using "left mouse-click" to explode, and creating a cube of TNT to explode and showing results.

- "tnt = 46"

- "mc.setBlock(x, y, z, tnt) or to explode with LMB(leftmousebutton) "mc.setBlock(x, y, z, tnt, 1)"

- "mc.setBlocks(x+1, y+1, z+1, x+11, y+11, z+11, tnt, 1)"
  
https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/6ae34f83-d7a5-4312-8b13-743ba5d0c31f

![TNT3](https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/06f86f59-fe04-4e98-a9e3-9af31e9c4a8b)

https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/3ff9197f-fe08-49e8-885a-31b057854f64



## Lava *Placing flowing lava* 
Placing a fluid entity or block known as "flowing lava"

- "from mcpi.minecraft import Minecraft"

- "mc = Minecraft.create()"

- "x, y, z = mc.player.getPos()"

- "lava = 10"

- "mc.setBlock(x+3, y+3, z, lava)"

https://github.com/JanGuiao/Minecraft-Pi/assets/95273542/7d86af5f-b24e-4451-9a91-6fa0dd8a7ff2



















































