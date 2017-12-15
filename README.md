# agradient

Cube 2 Sauerbraten texture vcolor gradient generation scripts

![topimage](https://i.imgur.com/Wtjqm1a.png)

## a1dgrad 
Generates a gradient line between any two colors. Interpolates a straight line throught the RGB color space between the two specified colors

![!a1dgrad](https://i.imgur.com/EzPC0YM.gif)

## a2dgrad


Generates a gradient plane between any four specified colors

![Imgur](https://i.imgur.com/oWMiRu0.gif)


## a3dgrad

Generates the full RGB color space as a cube with specified size in colorsteps, or a rectangular cuboid when given the amount of steps in each direction.

[Imgur](https://i.imgur.com/RyiJgfX.gifv)

## Installation
  
1. Download the .cfg files and put them your sauerbraten custom content directory.

	On Linux this is ~/.sauerbraten

	On Windows 7 and 10 this is C:\Users\\\%username%\Documents\My Games\Sauerbraten

	On an Apple Mac it is most likely macHD/users/%username%/library/Application Support/sauerbraten/

2. Add the following lines to your autoexec.cfg inside your sauerbraten directory:

```text
exec a1dgradient.cfg
exec a2dgradient.cfg
exec a3dgradient.cfg
```

## Usage

you can call all three functions without input arguments to see an explanation of how to use it in the console output.

/a1dgrad
![Imgur](https://i.imgur.com/GJfMyYJ.png)

/a2dgrad
![Imgur](https://i.imgur.com/owvtlfL.png)

/a3dgrad
![Imgur](https://i.imgur.com/OYRCQMq.png)

a2dgrad and a3dgrad will both define an alias function `agradient`. Editbind this alias. (I prefer the `end` key) 

```text
/editbind end agradient
```

After you start with `/a2dgrad` or `/a3dgrad`, you use this keybind to place the lines of cubes. Since you will probably make some errors while placing the lines, it is convenient to be able to undo and continue adding the lines of the gradient you're generating. 
For this I added an alias function called `agradientundo`, which undos your last step and sets back all color values to the previous step. (I prefer to editbind this to the `home` key). 

```text
/editbind home agradientundo
```

Since both a2dgrad and a3dgrad will declare agradient and agradientundo, you only have to bind them once and can then use them for both these functions.

## Tips
- For the best results, use the white texture on page 10 of the F2 menu, `/vscroll 999999 999999` and `/vscale 0.125`

- Make sure that the row of cubes that will be generated will stay inside your view or else it will only be partially generated.
Sauerbraten only allows you to edit on the stuff thats in your direct view.

- Because this script uses vcolor, it can only be used in multiplayer if you disable nompedit: `/nompedit 0`. After using it you have to use `/sendmap` for others to see it.
