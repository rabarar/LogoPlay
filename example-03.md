

This example contains the following functions:

spiral

Open the .acsl file and in the intrepreter type "spiral  8 36 80 44" followed by command-enter to run it.

where the parameters are: inner, outer, radius, angle

spiral function:

	cs 
	pu 
		setpos [0 0] 
	pd 
	repeat :outer 	[ rt 10 repeat :inner  	[ fd :radius lt :angle] ] 
	ht

