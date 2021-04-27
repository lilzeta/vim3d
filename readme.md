# vim3d

Vim3D, a vi-style interface to 3D modeling and simulation built in C++ and OpenGL

Many basic building tools are available through commands much like the ones used in unix which are accessed through the vi-style command line in the lower portion of the screen. The target users for this software are developers and engineers, in particular, people with an interest in computer science, creativity, visualization, and a love of the vi editor.

## build and run

#### 1 To get started clone `vim3d` and enter `vim3d/src/`

	git clone https://github.com/pyramation/vim3d.git
	cd vim3d/src

#### 2 call `make` to build the binary

    make
    
#### 3 Run `vim3d`

You can run it locally, or copy it to your path
    
    ./vim3d

## usage

    vim3d [sceneFile]

there are some examples in the `scenes/` folder, check those out to get started.

<p align="center">
  <img src="https://user-images.githubusercontent.com/545047/116325858-06630980-a778-11eb-83ca-dea22267ad7c.gif">
</p>

<p align="center">
  <img src="https://user-images.githubusercontent.com/545047/116325535-3b229100-a777-11eb-904b-7e1953962fa1.jpg">
</p>


for an example of loading a scene file, try this one
   
    vim3d scenes/demoday


## quickstart / mini tutorial

open vim3d in the shell

	vim3d

<p align="center">
  <img src="https://user-images.githubusercontent.com/545047/116325531-38c03700-a777-11eb-9ec7-45262d1beb2a.jpg">
</p>

#### get familiar with the 2 camera hotkeys to move around!

tumble is default behavior when mouse movement occurs. 

press `x` to toggle zoom/tumble when mouse movement occurs

press `z` to toggle pan/tumble when mouse movement occurs

#### start to draw
	
hit `i` to go into insert mode
	
	i

<p align="center">
  <img src="https://user-images.githubusercontent.com/545047/116325751-bf751400-a777-11eb-907c-33477bc26573.jpg">
</p>

you can toggle orthogonal mode with `8`

While in insert mode, hit the `l` key to cycle through different curve interpolation previews.

When finished drawing, press `enter`.

#### interpolations

These are commands, you'll have to enter command mode by pressing `:`

to interpolate specify level of detail as the argument to `bezier`, `bezier2`, or `bspline`

	bezier 5

hit `u` to undo and try these:

	bezier2 5
	bspline 5

name the object

	name mycurve	

#### creating a rectangular box and copying it to the curve

now add a add grid, and extrude it.
	
	add grid 0 0 1 4
	extrude 0 0 0 10
	name mygrid
	
now copy your rectangular box to the curve that you drew!
	
	copy mygrid mycurve geo align

#### split the window and add another camera
	
	Vexplore
	
	add camera	
	position 100 100 100


#### adding and moving objects

	add cube

press `m` to toggle move mode

press `z` to toggle pan/tumble when mouse movement occurs


You can do animations, add lights, and also sorts of super cool transformations. Read the docs and check out the examples!



# Docs

[Cheet Sheet](docs/cheet-sheet.md)

[Basic Commands](docs/basic-commands.md)

More docs to come, for more syntax, and how-to: [vim3d.com](http://vim3D.com)

