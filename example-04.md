
This example contains the following functions:

vonkoch
snowflake

Open the .acsl file and in the intrepreter type "snowflake size level" followed by command-enter to run it.

vonkoch procedure:

	if :level < 1 [forward :size stop][]
	vonkoch :size/3 :level - 1
	left 60
	vonkoch :size/3 :level - 1
	right 120
	vonkoch :size/3 :level - 1
	left 60
	vonkoch :size/3 :level - 1


snowflake procedure:

	cs
	pu
	setpos [0 0]
	pd
	left 180 repeat 3 [vonkoch :size :level right 120]

