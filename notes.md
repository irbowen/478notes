Lecture #8

** Prime Implicants

	Any single 1 or group of 1's that can be combined together on a
	Karnaugh map of the function F represents a product term which
	is called an IMPLICANT.

	A PRIME IMPLICANT is a product term that cannot be combined with
	another term to eliminate a variable.


	A single 1 is a prime implicant if it is not adjacent to any other 1's.

	Two adjacent 1's form a prime implicant if they are not contained in
	a group of four adjacent 1's.

	Four adjacent 1's form a prime implicant if they are not contained in
	a group of eight adjacent 1's.

	The minimum sum-of-products expression for a function consists of
	some (BUT NOT NECESSARILY ALL) of the prime implicants of a function.


	 \ AB
	CD\  00  01  11  10
	   \_______________
	   |   |   |   |   |   
        00 |   | 1 | 1 |   |    Prime implicants: A'B'D, BC', AC, A'C'D
	   |___|___|___|___|                      AB, B'CD
           |   |   |   |   |  
        01 | 1 | 1 | 1 |   |    Minimum solution: F = A'B'D + BC' + AC
	   |___|___|___|___|
	   |   |   |   |   | 
        11 | 1 |   | 1 | 1 | 
	   |___|___|___|___| 
           |   |   |   |   |
        10 |   |   | 1 | 1 |  
	   |___|___|___|___|

	To ensure that a minimum solution is found, select essential prime
	implicants first.  Then find a minimum set of prime implicants
	that cover the remaining 1's on the map.


	 \ AB
	CD\  00  01  11  10
	   \_______________
	   |   |   |   |   |   
        00 | X | 1 |   | X |    Essential prime implicants are:  
	   |___|___|___|___|    A'C', ACD, and A'B'D'
           |   |   |   |   |  
        01 | 1 | 1 |   |   |    Either A'BD or BCD can be chosen for
	   |___|___|___|___|    final minimum solution.
	   |   |   |   |   | 
        11 |   | 1 | 1 | 1 | 
	   |___|___|___|___| 
           |   |   |   |   |
        10 | 1 |   |   |   |  
	   |___|___|___|___|


** 5- and 6-Variable Karnaugh Maps

	A 5-variable map can be constructed in 3 dimensions by
	stacking two 4-variable Karnaugh maps.


	     \ BC
	   DE \  00  01  11  10
     	       \_______________
	       |  /|1 /|1 /|1 /|  8 terms combine to form BD'
            00 | / | / | / | / |
	       |/_1|/__|/_1|/_1|  4 terms combine to form CDE
	       |  /|  /|1 /|1 /|
	    01 | / | / | / | / |  2 terms combine to form AB'DE'
	 A     |/__|/__|/_1|/_1|
	1/0    |  /|1 /|1 /|  /|  Two 1's in upper left are not adjacent
	    11 | / | / | / | / |
	       |/__|/_1|/_1|/__|
	       |1 /|1 /|  /|  /|
	    10 | / | / | / | / |
	       |/__|/__|/__|/__|


	     \ BC
	   DE \  00  01  11  10
     	       \_______________
	       |  /|  /|  /|  /|
            00 | / | / | / | / |
	       |/__|/_1|/__|/__|  Each term can be adjacent to exactly 5
	       |  /|1 /|  /|  /|  other terms.
	    01 | / | / | / | / |
	 A     |/_1|/_1|/_1|/__|
	1/0    |  /|  /|  /|  /|
	    11 | / | / | / | / |
	       |/__|/_1|/__|/__|
	       |  /|  /|  /|  /|
	    10 | / | / | / | / |
	       |/__|/__|/__|/__|

	
	     \ BC
	   DE \  00  01  11  10
     	       \_______________
	       |1 /|X /|1 /|  /|
            00 | / | / | / | / |
	       |/__|/_X|/_1|/__|   Essential prime implicants are
	       |  /|  /|  /|  /|   AB'D'E' and CE' and A'BE
	    01 | / | / | / | / |
	 A     |/__|/_ |/_1|/_1|
	1/0    |  /|  /|  /|  /|
	    11 | / | / | / | / |
	       |/__|/__|/_1|/_1|
	       |  /|1 /|1 /|  /|
	    10 | / | / | / | / |
	       |/__|/_1|/_1|/__|

	

	A 6-Variable Karnaugh Map:

 	       \ CD
	     EF \  00   01   11   10
     	         \___________________
	         |\1 /|\1 /|\  /|\1 /|   
              00 |1\/ |1\/ | \/ | \/ |   Terms are:
		 | /\1| /\1| /\ | /\1|
		 |/_1\|/_1\|/__\|/__\|   C'E'F', BCD'E'F', ABEF'
	         |\  /|\  /|\1 /|\  /|  
          AB  01 | \/ | \/ | \/ | \/ |   ABCDE'F, and A'B'CDE'F
	 \11/    | /\ | /\ | /\ | /\ |
	  \/01	 |/__\|/__\|/_1\|/__\|
	10/\     |\  /|\  /|\  /|\  /|
         /00\ 11 | \/ | \/ | \/ | \/ |
		 | /\ | /\ | /\ | /\ |
		 |/__\|/__\|/__\|/__\|
	         |\1 /|\1 /|\1 /|\1 /|
              10 | \/ | \/ | \/ | \/ |
		 | /\ | /\ | /\ | /\ |
		 |/__\|/__\|/__\|/__\|

	AB = 00 is bottom layer, then AB = 01, then AB = 11, and AB = 10
	is top layer.


** Other Uses for Karnaugh Maps

	Many operations that can be performed using a truth table or
	algebraically can be done using a Karnaugh map.

		- Determination of minterm and maxterm expansions
		- Proof that two functions are equal (same maps)
		- ANDing and ORing two functions by performing the
		  function on the correspondings positions on their maps
		- etc. 

