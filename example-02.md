
This example contains the following functions:

polar
polars
headRad
rad
deg
while

Open the .acsl file and in the intrepreter type "polar 5 1 1" followed by command-enter to run it.

polar function:

	if :erase > 0 [cs] []
	make "theta 0
	make "r 0
	make "pscale 100* :scale


	make "t_bound 3.140
	make "t_inc 0.01
	make "t_rep :t_bound / :t_inc

	setpos [0 0]
	pd
	setpenwidth :scale
	repeat :t_rep [  local "r  make "r sine(:rose * deg :theta) local "x make "x :r * cosine(deg :theta) local "y make "y :r * sine(deg :theta) make "theta :theta + :t_inc local "h make "h headRad :theta setheading :h  setpos list :x*:pscale :y*:pscale ]


polars function:

	cs
	make "x 1
	make "scale 1.0
	while [:x<25] [ polar :x 0 :scale make "scale :scale*1.2 make "x :x +1 ]




