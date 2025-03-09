#archive 
- [x] Challenge 1
- [x] Challenge 2
- [x] Challenge 3
- [ ] Challenge 4 
- [ ] Challenge 5
- [ ] Challenge 6
- [ ] Challenge 7 
- [ ] Challenge 8
- [ ] Challenge 9
- [ ] Challenge 10


Coding Logic for Pattern:
- Make the buttons be represented by numbers.
- Choose a number randomly 0-9 (choosing one button to the sequence)
- Push number into an array.
- When the user inputs, it must make sure it follows the array
	- Probably just do a for loop and check each number.

Steps for Project Setup.
1) Create pattern alg
	1) Variable Declaration
		1) Create array to hold values
		2) Create variable to hold newest value (temp)
	2) Pattern Creation
		1) Store random value in temp
		2) Push temp to array
		3) Loop for a certain amount of iterations (remove for final product)
		4) Each number correlates with an output pin. Use output pin to light up leds to see the pattern
	5) Pattern Detection
		1) After the pattern is played
		2) Loop to check each button is pressed in the correct order by scrolling through the array and checking if the correct button is pressed for that portion of the loop.