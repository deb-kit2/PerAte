# Per-ate Syntax

All commands can be put one after the another with spaces in between or not. However, it is recommended to use spacing and indentation for ease of readability. Note that, no spaces must occur between operators @, g=, g+, g-, g*, g/ and corresponding address number. All address are initialized to value zero by default.

1. Operators:-
	a. @___		Here, ___ represents a 3 digit number, for example, 124, 001, or 000. This sets the pointer to that particular address. Example usage is - @438  
	b. =		This is the assignment operator.  
	c. +		This is the increment operator. It increases the value at the current address by right hand side.  
	d. -		This is the decrement operator. It decreases the value at the current address by right hand side.  
	e. *		This is the self-multiply operator. It multiplies the value at the current address by right hand side.  
	f. /		This is the self-divide operator. It divides the value at the current address by right hand side.  
	g. g=___	This gets the value at @___ and assigns it to the curent location.  
	h. g+___	This gets the value at @___ and increases the value at current location by that amount.  
	i. g-___	This gets the value at @___ and decreases the value at current location by that amount.  
	j. g*___	This gets the value at @___ and multiplys the value at current location by that amount.  
	k. g/___	This gets the value at @___ and divides the value at current location by that amount.  
	l. { 		Start loop. (Working of loops is explained in section 2. Loops)  
	m. } 		End loop.  
	n. >		Point to the next location.  
	o. <		Point to the previous location.  
	p. |		Used to assign integers to adresses. Example: @100 = |200|  
	q. '		Used to assign characters to addresses. Example @345 = 'k'  
	r. ( )		Anything between parantheses is completely ignored, so you can use it for debugging or commenting.  
	

2. Loops:-
	Whenver a '{' is encountered, the value at current location is checked. If it is zero, the loop is skipped. Any non-zero value results in execution of the loop. When the corresponding } is encounter, execution moves to back to }, value is checked at current pointer and loop continues.  
	
	For example:  
		@100 = |3|  
		{  
			@001 + |2|  
			@100 - |1|  
		}  
		
	This loop will be executed 3 times, and will increment @001 by 6.  
	Ofcourse, loops can be nested.

3. I/O
	Mainly, 2 data types exist in Per-ate -- integer and character, with float in the works. The following can be used for I/O:  
		a. pi	Output current value to screen as integer (put - integer).  
		a. pc	Output current value to screen as character (put - character).  
		a. gi	Read value from screen as integer (get - integer) and save it to current location.  
		a. gc	Read value from screen as character (get - character) and save it to current location.  

		
For sample programs and "tips and tricks", see other files in this package.