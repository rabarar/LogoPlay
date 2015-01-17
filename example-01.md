This example contains the following functions:

box
spiral
tree
forest

Open the .acsl file and in the intrepreter type "Forrest 50" followed by command-enter to run it.

Recursive tree function:

	setpenwidth :size / 25
	forward :size
	if :size > 2 [ local "angle make "angle (30 + random 60)  local "scale make "scale 0.6 + (random 20)/100
	    right :angle / 2
	    setpencolor random 5
	    tree (:size * :scale)
	    setpencolor random 5
	    left :angle 
	    tree (:size * :scale)
	    right :angle / 2
	]
	[]
	back :size

Forest function:

	cs
	ht
	pu
	repeat :trees [
	local "xpos make "xpos (power -1 random 3) * (random 500)
	local "ypos make "ypos (power -1 random 3) * (random 500)
	local "l make "l [:xpos :ypos]
	setpos list :xpos :ypos

	pd
	setpencolor random 5
	tree random :size
	pu
	]
	print "done

