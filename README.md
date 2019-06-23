# string_functions
Assignment 2 from Intro programming class 1

Emily Zastenchik
Assignment 2

Problem:

Return original string of 4 words spaced with "*" in 
	reverse order without spaces using function prototype: 
	string split_and_reverse(string)
	(function must: 	-extract each word from original string and store each token as a string object
						-concatenate words in reverse order as a string
						-return result as a string
		Example. The*sky*is*blue	(original string)
				blueusskythe		(final string)
        
Analysis: 

    INPUTS 
    
     string fullName				//fullName = firstName+lastName
		 gender
     
    OUTPUTS 
    
        string fullName		//original string "Hello*Mr./Ms.*fullName
        string R = split_and_reverse(s)		//final string "lastNamefirstNameMr./Ms.hello"
        
    FUNCTIONS 
    
    	string split_and_reverse(string)
      
    		member functions -
    			getline
    			astring.assign
    			astring.replace
    			astring.erase
          
Design:

	Ask user for first name and last name
  
	Use getline function to store both tokens in fullName
  
	Use replace function to replace " " with "*" in fullName 
  
    Ask for gender
    
    	Pass gender through if statement
      
    	Display original function
      
    Pass original function through split_and_reverse function
    
    	string h, m, f, l, R
  		h.assign(a, 0, a.find("*"))				//h = Hello
		h.replace(0, 1, "h")					//h = hello
		m.assign(a, a.find("*") + 1, 3)			//m = (Ms./Mr.)
		a.erase(0, h.length() + m.length() + 2)	//a = fullName
		f.assign(a, 0, a.find("*"))				//f = firstName
		a.erase(0, f.length() + 1)				//a = lastName
		l.assign(a, 0, a.length())				//b = lastName
		R = l + f + m + h						//R = lastNamefirstName(Ms./Mr.)hello
    Return final string R
