# Module 7: Automate Cybersecurity Tasks With Python

## Python 
- main usage in cybersecurity is for short automated tasks: like sorting through logs and managing access control list (employee access), and also connect processes together (like delivering a file and notifying specific employees)
- can be used for log & malware analysis, intrusion detection, compliance checks, and network scanning
  ### Advantages
  - resembles human language (easy to read)
  - requires less code in general
  - has an extensive collection of built-in code that can be imported to perform tasks
    
#Python Script

-#- hash symbol indicates a comment - the programmer is describing their intention behind the code
    - common practice to start with a comment
    
 	 	# Print Hello Python     
   		print ("Hello Python!")
   
   - print () -- outputs a specified object to the screen. so the initial hash (#) comment says what you want to do with the code, and the code below signifies the code to do that.
      
- Syntax - refers to the rules of the correct structure of programming language

## Python Environments
  - Notebooks - online environment for writing, storing, and running code (Jupyter Notebook & Google Colaboratory)
      - Code Cells - meant for writing and running code. has a "play" button
      - Markdown Cells - meant for describing code
  - IDE (Integrated Development Environment) - app for writing code, that gives editing help and error correction tools, uses gui
  - CLI (Command-Line Interface) - text based interface that can also run python

# Core Python components

  ## Data type - a category for a particular type of data item
   - String data - data consisting of an ordered sequence of characters (must be placed within quotations or apostrophes!!)
   - Numeric data - does NOT use quotation marks
       - Float data - consists of a number with a decimal point (whole numbers also get a decimal -- 2.0)                                 - / symbol is a divide, but // divides and returns as rounding down to the nearest whole number 
       - Integer data - consists of a number without a decimal point
   - Boolean data - can only be one of two values (true or false) NO QUOTATIONS EITHER!!
   - List data - data structure that consists of a collection of data in sequential form
        - entirety of list must be placed within brackets [ ]  , and separated by commas, -ex. print (["estrada", "zamboni"])
   - Tuple data - data structure that consists of a collection of data that cannot be changed. Like lists, tuples can                   contain elements of varying data types
           - tuple data cannot be changed (unlike list data)
           - placed in parentheses vs list data in brackets
   - Dictionary data - is data that consists of one or more key-value pairs.
           - Each key is mapped to a value. A colon (:) is placed between the key and value. Commas separate key-value pairs             from other key-value pairs, and the dictionary is placed within curly brackets ({}).
   - Set data - data that consists of an unordered collection of unique values. This means no two values in a set can be the             same.
           - Elements in a set are always placed within curly brackets and are separated by a comma. These elements can be               of any data type.

   ## Variable - a container that stores data    
        
  - username = "jrafael"
      - assigns the variable username a value of "jrafael"
       - The syntax for assigning a variable requires a name for the variable, then an equals sign (=), and finally the               value for the variable.  
       - used for abbreviating long strings or equations or numbers.  
       - the name of a variable should be separated by an underscore, no spaces.
       - EVERYTHING IS CASE SENSITIVE!
         - NEVER USE QUOTES for variable. Just parentheses
             
       			#Call a variable  
       			device_id = "mr5lkvi"
       				print (device_id)
 
         - this prints the variable's value (a string of characters) that you've already created

     ## type ()   - used to find what type of data is inside a variable. (string, integer, list, etc.)
     
    -   		device_id = "mr5lkvi"  
        		data_type = type(device_id)  
        		print (data_type)  
        		<class 'str'>

        - in above scenario, it would be 'str' for string
     
  ## type error - an error that results from using the wrong data type  
  - cannot combine a string with an integer

  		username = "nzhao"  
		old_username = username  
		username = "zhao2"  
			print("Previous username:", old_username)  
			print("Current username:", username)  

Previous username: nzhao  
Current username: zhao2  

The above scenario shows that things will recall within the order they were input. So when you print old_username, it shows how that variable was linked to the original value of username (nzhao). Then more recently the username value changed its variable to zhao2, so when printing username, it shows the most recent change.

# Conditional and Iterative Statements 

  ## Conditional Statement
- a statement that evaluates code to determine if it meets a specified set of conditions
  - "if" - starts a conditional statement and the first line of the header is always ENDED BY A COLON!!
  -
        if failed_attempts > 5:  
          print("Account Locked")

    - in a conditional statement, the print msg needs to be indented to function. so only prints if statement is True
    - the first line is called the "header" and the second line (if conditions are met) is called the body
    - "==" - double equal sign is used in conditional statements for equal value, and assigns a boolean value of True or False  
    - "!=" - used to say two things are "not equal", uses the boolean value of true, when they DON'T match

  - "else" - else precedes a code section that only evaluates when all conditions that precede it within the conditional               statement evaluate to False
        - always follow "if" statement and end in a colon
-
      operating system = "OS 3"  
      if operating system == "OS 2":  
        print("Updates Needed")  
      else:
        print("No Updates Needed")

  - "elif" - precedes a condition that is only evaluated when previous conditions evaluate to False. Unlike with else, there can be multiple elif statements following if.
 	- "elif" is basically an alternative sequence if the prior thing is false. so you can do 	multiple "elif's", and then as in below, "else" ends with a print

-
      if status == 200:  
        print("OK")  
      elif status == 400:  
        print("Bad Request")  
      elif status == 500:  
        print("Internal Server Error")  
      else:  
        print("check other status")  

   - the above statement goes through the "elif" possibilities, and then gets to "else", which prints since everything is false.

   -   if status >= 200 and status <= 226:  
        print("successful response")

    - in the above statement, the "and" operator is used. both things must be true in order to PRINT.
     
   -   if status == 100 or status == 102:  
        print("informational response")

       - in the above statement, the "or" operator is used. either can be true for it to PRINT.
   
       -
       if not(status >= 200 and status <= 226):  
         print("check status")

        - in above statement, the "not" operator inverts whether conditions are met in order to print. so if both things are not met, then it will PRINT.
        - ### MUST USE PARENTHESES AFTER "NOT", SO THAT BOTH ASPECTS ARE INCLUDED!

   - BELOW, uses the "in" operator, after creating a list:
      - the "in" operator tells python to run the loop for every item in the sequence.

  - 
        approved_list = ["elarson", "bmoreno", "tshah", "sgilmore", "eraab"]

        username = "bmoreno"

        if username in approved_list:
          print("access approved")
        else:
          print("access denied")

  ## Iterative Statement
    - a statement that repeatedly executes a set of instructions (loops)
     
      ### For Loops
        - begin with "for" (signals the beginning of the loop)
        - header is with the "for" keyword, body
        - "i" is the loop variable, which controls the iterations of a loop
          	- basically says to list each element (one at a time)
        - "in" is the operator; which tells python to run the loop for every item
        - must be a colon at the end of the header

-
        for i in [1,2,3,4]:    
          print (i)    

 - "range" function - generates a sequence of numbers. 
    range(0, 10) - will include 0-9... always includes first number, and then last number is when to stop  
      - if you don't provide a "start point", it will start at 0... so range(10), is the same as above
-
      for i in range(0, 5, 1):
        print(i)  

  in above loop, it prints 0-4 because the second number is the end point (which is not included), and then the 3rd number.            determines the incremental change (in this case, it increases by an integer of 1)

### If the start point is anything other than 0 or the increment is anything other than 1, they should be specified.

- For the below loop:
 		- when print is indented, it runs normally and prints through the entire loop  
   			- when it's not indented, it still runs, but only at the end. so it only   			prints "2", because it was the last number in the sequence (3 would not be   			printed)
  		- also, notice that you're telling it to print the word "Inside:" and then the comma   		separates to include a secondary option, which in this case is saying print whatever.  		"i" currently is  

		for i in range(3):
    			print("Inside:", i)   # runs each time

		print("Outside:", i)       # runs once, after the loop

So:
		Inside: 0  
		Inside: 1  
		Inside: 2  
		Outside: 2  



  ### While Loops
   
   - repeatedly execute a function, but the repetition is based on a condition you create before.
   - "while" indicates the beginning, followed by the condition, that contains the loop variable,
             in this case "time"
             - so you assign the variable beforehand, and then reference in the loop.
     ### Unlike "for" loops, While loops must always designate what the loop should do, or else will run 	forever on the first line. So with the setup below, it will continue to print "0", without the 		time = time +2 code
      
  - so in the below statement, time = 0 is the variable, and then underneath is the condition using it
    - in the indented body, it consists of the actions to take while the loop iterates
    - so the first line prints the current variable (0), and then print every two minutes; so this will.
      only print out even numbers less than or equal to 10. 
-
        time = 0.   
        while time <= 10:   
          print(time)  
          time = time + 2. 

- Below example will print in a list, everything from 5000 to 5150, but only divisible by 5

        i = 5000
        while i <= 5150:
          print (i)
          i = i + 5

- Below will show a list of ip addresses in list form. but if print(ip_addresses) was there, would list all 6, 6 times. but when print(i) is used, it knows ip_addresses is a list

        ip_addresses = ["192.168.142.245", "192.168.109.50"]

        for i in ip_addresses:
          print(i)

     - Another example below shows two variables created
            - with "While" loops, the variables are created separately!
            - the last line doesn't need to be indented because the action occurs outside the loop.                   basically once it's finished the loop (got to 5 devices), the loop stops and performs the next.            action in line
-
      max_devices = 5
      i = 1

      while i < max_devices:  
        print ("User can still connect to additional devices")  
        i = i +1  
      print ("User has reached maximum number of connected devices")  

- in the BELOW scenario, the variable is created. it prints "Login attempts:", and then whatever the login_attempt is, and then continues to add 1 to each attempt. so will print:
- Login attempts: 0   
  Login attempts: 1  
  Login attempts: 2   
  Login attempts: 3   
  Login attempts: 4   


      login_attempts = 0
      while login_attempts < 5:
        print("Login attempts:", login_attempts)
        login_attempts = login_attempts + 1
      
- in the BELOW scenario, count is a variable to track login attempts, and changes long_status to false once it equals 4

      count = 0
      login_status = True
      while login_status == True:
        print("Try again.")
        count = count + 1
        if count == 4:
          login_status = False

  ### Break keyword
    - used to break out (stop) a loop
    - so below sequence will only print "laptop1" beacuse it breaks when it gets to desktop20
-
        computer_assets = ["laptop1", "desktop20", "smartphone03"]  
        for asset in computer_assets:  
          if asset == "desktop20":  
              break  
          print(asset)  

    - when using "else", break must be at the end, in order for it to work. other wise won't print stuff after

               for i in ip_addresses:
	             if i in allow_list:
		              print("IP address is allowed")
	              else:
		              print("IP address is not allowed")
		              break
          
  ### Continue keyword
    - used to skip an iteration based on a certain condition in an if statement being true
   - below it will skip "desktop20", and just print laptop1 and smartphone03
    
-
        computer_assets = ["laptop1", "desktop20", "smartphone03"]
        for asset in computer_assets:
          if asset == "desktop20":
            continue
        print(asset)

    ### CTRL-C or CTRL-Z will exit an infinite loop!! Might need to be done when running a service that constantly processes data

# Introduction to Functions

- Function - a set of code that can be reused in a program
 		- Built-in functions - exist within python and can be called directly (like the print function)
   		- user-defined functions - ones that programmers design for their specific needs

  - "def" - placed before a function name to DEFINE a function
 	     
	      		# Define a function
   	   		def greet_employee():
      				print("Welcome! You're logged in.")

 			# Call a function
  			greet_employee()
    
    	-	Welcome! You're logged in.

    - "+" operator can combine two strings together into larger lists or data
   
    - 			def list_to_string():          # no indentation — function definition  
    				sum_variable = ""          # 1 indent — inside function  
    				for i in ["a", "b", "c"]: # 1 indent — still inside function   
        				sum_variable += i     # 2 indents — inside the loop  
        				print(sum_variable)   # 2 indents — prints every iteration (inside loop)  
    				print("Done")             # 1 indent — inside function, but outside loop  

	- Parameter - an object that is included in a function definition, to use within that function
    		- the parameter goes inside (). so with greet_employee(name) , name is the parameter
    		- the below code, shows two parameters (first_name and last_name)
    
    			def greet_employee(first_name, last_name):
    				print("Welcome! You're logged in", first_name, last_name)
    			greet_employee("Kiara", "Carter")
    
    	- Argument - the data brought into a function, when it is called
       		- so, as in the below code, "bmoreno" is the argument. so when the function is called up, and 			used, the argument, is what's inside those parentheses

	   				def display_username(username):
						print("Username is", username)
					display_username("bmoreno")

	- Return statement - a paython statement that executes inside a function and sends information back to the 	function call, using the "return" keyword
    		- lets you re-use a statement, unlike Print, which doesn't "Save" anything. this returns output 		(information) from a function
    		- the BELOW code stores 0 (3-3), inside of remaining_attempts. since that function is completed, 		it goes to the next line, which retrieves what's inside the variable remaining_attempts (the 			returned value) and puts it into the conditional statement. It's true, so it prints "Your account 		is locked"
 
    				def remaining_login_attempts(maximum_attempts, total_attempts):
   					return maximum_attempts - total_attempts
				remaining_attempts = remaining_login_attempts(3, 3)
				if remaining_attempts <= 0:
    					print("Your account is locked")

    	- Global variable - used throughout the entire program and assigned outside a function definition
       		- so, 	device_id = "7ad2130bd"
         - Local variable - a variable assigned within a function, and only used inside
           	- includes parameters as well as variables
           	- below, "total_string" and "name" are local variables:
          
           	  		def greet_employee(name):
					total_string = "Welcome" + name
					return total_string

	### it's best to avoid combining global and local variables within functions. Can cause confusion

## Built-in functions

- print() and type()
- max() - returns the largest numeric input passed int it. so below, 9 is the highest number
- min() - returns the smallest number

 				# Explore max
    				a = 3
       				b = 9
	  			c = 6
     				print(max(a,b,c))
	
				9

   - sorted() - sorts the components of a list, into alphabetical order (for strings), or in numerical order 		(for numbers)
  ### One more important detail about the sorted() function is that it cannot take lists or strings that have elements of more than one data type. For example, you can’t use the list [1, 2, "hello"].

     				# Use the sorted function
				usernames = ["elarson", "bmoreno", "tshah"]
   				print(sorted(usernames))
      
      				bmoreno, elarson, tshah

 - The below function shows that you can print the two separate lines, after you input the 3 arguments at the end of the code (calling the function) -- 'analyze_logins("ejones", 9, 3)' is calling the function
    
		# Define a function named `analyze_logins()` that takes in three parameters, 					`username`, `current_day_logins`, and `average_day_logins`

		def analyze_logins(username, current_day_logins, average_day_logins):

  		# Display a message about how many login attempts the user has made that day

    			print("Current day login total for", username, "is", current_day_logins)

    		# Display a message about average number of login attempts the user has made that day

    			print("Average logins per day for", username, "is", average_day_logins)

		# Call `analyze_logins()`

		analyze_logins("ejones", 9, 3)

 		Current day login total for ejones is 9
		Average logins per day for ejones is 3

   - The below function adds a second variable into this function, and then a 3rd print (or feedback msg)
  
      			# Define a function named `analyze_logins()` that takes in three parameters, 					`username`, `current_day_logins`, and `average_day_logins`

			def analyze_logins(username, current_day_logins, average_day_logins):

    			# Display a message about how many login attempts the user has made that day

    				print("Current day login total for", username, "is", current_day_logins)

    			# Display a message about average number of login attempts the user has made that day

    				print("Average logins per day for", username, "is", average_day_logins)

    			# Calculate the ratio of the logins made on the current day to the logins made on an 				average day, storing in a variable named `login_ratio`

    				login_ratio = current_day_logins / average_day_logins

    			# Display a message about the ratio print(username, "logged in", login_ratio, "times as 			much as they do on an average day.")

			# Call `analyze_logins()`

			analyze_logins("moreno", 2, 3)

			Current day login total for moreno is 2
			Average logins per day for moreno is 3
			moreno logged in 0.6666666666666666 times as much as they do on an average day.

# Modules

- a python file that contains additional functions, variables, classes, and any kind of runnable code
  - re module - used for searching for patterns in log files
  - csv module - used for working with csv files
  - glob & os modules - interact with the command line
  - time & datetime - working with timestamps
     
 ## Python Standard Library 
 - an extensive collection of usable python code (including modules), that comes with Python

  - external libraries can also be downloaded
    	- beautiful soup - parses html website files
    	- NumPy - for arrays and mathematical computations

    ### Importing an entire module
    - importing the statistics module

    			import statistics
				monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]
				mean_failed_attempts = statistics.mean(monthly_failed_attempts)
				print("mean:", mean_failed_attempts)

    				mean: 35.25
    
   - 	Note: When importing an entire Python Standard Library module, you need to identify the name of the module with the function when you call it. You can do this by placing the module name followed by a period (.) before the function name. For example, the previous code blocks use statistics.mean() and statistics.median() to call those functions. 

  - To import specific (but multiple in the below case), use the code below
    	- when importing specific function from a module, you don't neeed to specify the name of entire module 		(like the code above), but only need to say the specific function you're using from the module - 		mean(monthly_failed_attempts), instead of statistics.mean(monthly_failed_attempts)

    			from statistics import mean, median
				monthly_failed_attempts = [20, 17, 178, 33, 15, 21, 19, 29, 32, 15, 25, 19]
				mean_failed_attempts = mean(monthly_failed_attempts)
				print("mean:", mean_failed_attempts)
				median_failed_attempts = median(monthly_failed_attempts)
				print("median:", median_failed_attempts)

    - To import an external library in a Jupyter Notebook or Google Colab environment, you need to install them
      	- first, run the following line for (numpy) - %pip install numpy , then just import numpy (like the python 		library)
     
### Code Readability
- PEP Style Guide (Python Enhancement Proposals) - a resource that provides stylistic guidelines
	- not mandatory, but help create consistency among programmers
   	- keep all lines to 79 characters (including comments) to maintain readability
    		- if you need more for a comment, start a second line, again with an #
  	- another way to create a longer comment is to use three quotations """, at the beginning
    	and end of the statement, still with less than 79 characters per line, but then you don't
    	need a # at each line

    ### In Python, you should indent the body of conditional statements, iterative statements, and function definitions.

    -if you had a conditional statement inside of a while loop, the body of the loop would be indented four spaces and the body of the conditional would be indented four spaces beyond that. See below:
  -
  
    					count = 0
    					login_status = True
    				 	while login_status == True:
						   print("Try again.")
						   count = count + 1
						   if count == 4:
							   login_status = False

# Working with Strings

## String Operations
 
- len() - returns the number of elements in an object

  		# Print the length of a string "Hello"
  		print(len("Hello").
  
	 	5

 - Must use "len" in order to calculate below whether the employee_id is less than 5. can't do it without it

  		# Assign `employee_id` to a four digit number as an initial value employee_id = 4186

		# Reassign `employee_id` to the same value but in the form of a string employee_id = 				str(employee_id)

		# Display the `employee_id` as it currently stands print(employee_id)

		# Conditional statement that updates the `employee_id` if its length is less than 5 digits

		if len(employee_id) < 5:
    			employee_id = "E" + employee_id

		# Display the `employee_id` after the update

			print(employee_id)
     
- String concatenation - the process of joining two string together

  		# Concatenate two strings 
  		print("Hello" + "world")  
	 
	 	Helloworld

- Method - a function that belongs to a certain data type
  - unlike other functions, methods appear after the string.
  - two common string methods are the upper and lower methods. Below is the upper method

    		# Apply upper method to "Hello".
    		print("Hello".upper())  

    		HELLO

## String Indices
 - Index - a number assinged to every element in a sequence that indicates its position
 - so, the index is the position of each character in a string
   - placing an index in square brackets after a string returns the character at that index
 - start counting indices from 0. So HELLO, is 0-4

			"HELLO"[1]
			E
      
   - Slice - uses a "start" and "stop" to specify a set of indeces, in order to extract a larger part

			"HELLO"[1:4]
  			ELL

- Index Method - used to search in a string 
    - .index()
    - finds the first occurrence of the input in a string and returns its location
      - remember, they're case sensitive
    
			#Use the index string method. 
			print("HELLO".index("E"))  
			1

- below is similar to above, except that it's using a variable "ip_addresses" (so doesn't use quotes), and asking what to index (count) where the ip address starts

   			ip_addresses = "192.168.140.81, 192.168.109.50, 192.168.243.140"
			print(ip_addresses.index("192.168.243.140"))

  			32

### Strings are immutable - they cannot be changed after it is created and assigned a value


  			# Assign `url` to a specific URL

			url = "https://exampleURL1.com"

			# Display the index where the domain extension ".com" is located in `url`

			print(url.index(".com"))

   			19

- below shows how you can set an index of ".com", and then print between the starting string character of "8", and then print until the "Beginning" of the index...which was already set to ".com", and thus, when the "." starts

			# Assign `url` to a specific URL

			url = "https://exampleURL1.com"

			# Assign `ind` to the output of applying `.index()` to `url` in order to extract the 				starting index of ".com" in `url`

			ind = url.index(".com")

			# Extract the website name in `url` and display it

			print(url[8:ind])

## Lists and Algorithms
 ### Replacing an element in a list
 	- just add the brackets
```
			# Change a specific element in a list
  			my_list = ["a", "b", "c", "d"]
    			my_list[1] = 7
      			print(my_list)   

 			[a, 7, c, d]

			# Another example is below, but using words, so it's easier to see between the "2" & the name

			username_list = ["elarson", "bmoreno", "tshah", "sgilmore"]
			print("Before inserting an element:", username_list)
			username_list.insert(2,"wjaffrey")
			print("After inserting an element:", username_list)
```

## Inserting and Removing Elements in Lists
-
 ### Insert Element
- The method below takes two arguments: the first is the position we're adding the element to, and the second is the element we want to add. 
  - You can see that while above, something is replaced in a list, with insert, it shifts everything down

 	```
			# Use the insert method
			my_list = ["a", "b", "c", "d"]
			my_list.insert(1, 7)
			print(my_list)

			# Output:
			['a', 7, 'b', 'c', 'd']
	```

### Remove Element
 - The removed method removes the first occurrence of a specific element in the list. Unlike insert, the argument of removed is not an index value. 		Instead, you directly type the element you want to remove.

```
 			# Use the remove method
			my_list = ["a", "b", "c", "d"]
   			my_list.remove("d")
      			print(my_list)

  			[a, b, c, e]
```
## Writing an algorithm
- a set of rules/steps that solve a problems or tasks

    - Below has two tasks
      1) using string slicing to extract the first 3 digits from one IP address
      2) uses a loop to apply that solution to every IP address on the list

	- the second algorithm uses the .append() method to add input to the end of a list

```
address = "198.223.xx.xx"

# Extract the first three characters of an IP address
print(address[0:3])

198
```

  - below shows that "for" starts the loop, "address" as the variable inside the for loop, and the list IP as the iterable
  - the first line, creates an empty list, named networks
``` 
IP = ["198.223.XX.XX", "198.101.XX.XX", "180.064.XX.XX", "192.168.XX.XX", "184.090.XX.XX"]

# Extract the first three characters from a list of IP addresses
networks = []
for address in IP: 
	networks.append(address[0:3])
 print(networks)

 ['198', '198', '180', '192', '184']
 ```
### Below is code that shows how to index an item in one list, and then use that number to retrieve something with the same index. So once finding the index of "sgilmore" and putting it into the "ind" variable, you can then recall that output of "2" to retrieve the index of 2 in the "approved_devices" list
```
# Assign `approved_users` to a list of approved usernames

approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]

# Assign `approved_devices` to a list of device IDs that correspond to the usernames in `approved_users`

approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

# Assign `username` to a username

username = "sgilmore"

# Assign `ind` to the index of `username` in `approved_users`

ind = approved_users.index(username)

# Display the device ID at the index that matches the value of `ind` in `approved_devices`

print(approved_devices[ind])
```
### Below code is used to develop a function that uses a conditional inside of another conditional statement to automate the login process. 
- The outer conditional handles the case when the username is approved and the case when username is not approved. The inner conditional, which is placed inside the first if statement, handles the case when the username is approved and the device_id is correct, as well as the case when the username is approved and the device_id is incorrect. 

```
approved_users = ["elarson", "bmoreno", "sgilmore", "eraab", "gesparza"]
approved_devices = ["8rp2k75", "hl0s5o1", "4n482ts", "a307vir", "3rcv4w6"]

# Define a function named `login` that takes in two parameters, `username` and `device_id`

def login(username, device_id):
    if username in approved_users:

        # then display "The user ______ is approved to access the system.",

        print("The user", username, "is approved to access the system.")

        # assign `ind` to the index of `username` in `approved_users`,

        ind = approved_users.index(username)

        # and execute the following conditional
        # If `device_id` matches the element at the index `ind` in `approved_devices`,

        if device_id == approved_devices[ind]:
          print(device_id, "is the assigned device for", username)
        else:
          print(device_id, "is not their assigned device.")

    else:
        print("The username", username, "is not approved to access the system.")

login("bmoreno", "hl0s5o1")

The user bmoreno is approved to access the system.
hl0s5o1 is the assigned device for bmoreno
```
## Regular Expressions
- regular expressions (regex) - a sequence of characters that forms a pattern
  - this pattern can then be used to search within log files, find all strings that start with a prefix, or length
    ### Use "import re" to import the "re" module, each time you start a new python session
  - "+" - regular expression symbol that represents one or more occurrences of a specific character
    - "a+" matches - to any string that has "a" within it
    - "\w" - matches with any singular alphanumeric character, ### NO SYMBOLS! except the underscore "_" works as well
    - "\w+" - will match with multiple characters
    - "." - matches to all characters, including symbols
    - "\d" - matches to all single digits [0-9]
    - "\s" - matches to all single spaces
    - "\." - matches to the period character
    - "*" - represents zero, one, or more occurrences of a specific character
    - "{2}" - instructs python to return all matches of exactly two single digits in a row (or whatever # is inside)
      	- You can also specify a range within the curly brackets by separating two numbers with a comma. The first number is the minimum number of repetitions and the second number is the maximum number of repetitions. The following example returns all matches that have between one and three repetitions of a single digit:
      	  
```
import re
re.findall("\d{1,3}", "h32rb17 k825t0m c2994eh")

['32', '17', '825', '0', '299', '4']
```
- So "b\wa+b" could match with "bkaaab" because:
      	  	- it must start with "b"
      	  	- "\w" means that anything can come after "b"
      	  	- "a+" means a must come next
      	  	- "b" means it must end with "b"

  - Another example: user1@email1.com  
    		   - \w+ @ \w+ \. \w+  
      	  	- "\w+" is used to collect any characters until...  
      	  	- "@" is used to show that after an undetermined amount of characters, an "@" must be present.   
      	  	- "\w+" is again present for "email1" or any type of e-mail client. 
      	  	- "\." is used for the period because with the "\", it would be considered an operator    
      	  	- "\w+" is used for the ".com" or whatever ending is there. 
      	  		### So basically it would return any e-mails  

	- re.findall() - returns a list of matches to a regular expression  
  		- the first parameter is a regular expression pattern to search for, the 2nd parameter is the string   		it will search through  
    		- so you could use: print(re.findall("\w+@\w+\.\w+", email_log)) to find all e-mails within the   			email_log  

- the below code uses the basic \w to search, and you can see, each character is returned separately
```
import re
re.findall("\w", "h32rb17")

['h', '3', '2', 'r', 'b', '1', '7']
```

-The below example shows how you can extract just the username and login attempts from users. It disregards the employee ID number in the search because w+: will only bring any number of characters that ends with a colon. And because of the space between the ID number and the username, it's not connected. The \s includes the space after the colon, and the d+ is specific to numbers.
 
```
import re
pattern = "\w+:\s\d+"
employee_logins_string = "1001 bmoreno: 12 Marketing 1002 tshah: 7 Human Resources 1003 sgilmore: 5 Finance"
print(re.findall(pattern, employee_logins_string))

'bmoreno: 12', 'tshah: 7', 'sgilmore: 5']
```

- The below code is an iterative statement that loops through the valid_ip_addresses list and checks if each IP address is flagged.

```
log_file = "eraab 2022-05-10 6:03:41 192.168.152.148 \niuduike 2022-05-09 6:46:40 192.168.22.115 \nsmartell 2022-05-09 19:30:32 192.168.190.178 \narutley 2022-05-12 17:00:59 1923.1689.3.24 \nrjensen 2022-05-11 0:59:26 192.168.213.128 \naestrada 2022-05-09 19:28:12 1924.1680.27.57 \nasundara 2022-05-11 18:38:07 192.168.96.200 \ndkot 2022-05-12 10:52:00 1921.168.1283.75 \nabernard 2022-05-12 23:38:46 19245.168.2345.49 \ncjackson 2022-05-12 19:36:42 192.168.247.153 \njclark 2022-05-10 10:48:02 192.168.174.117 \nalevitsk 2022-05-08 12:09:10 192.16874.1390.176 \njrafael 2022-05-10 22:40:01 192.168.148.115 \nyappiah 2022-05-12 10:37:22 192.168.103.10654 \ndaquino 2022-05-08 7:02:35 192.168.168.144"

# Assign `pattern` to a regular expression that matches with all valid IP addresses and only those 
pattern = "\d{1,3}\.\d{1,3}\.\d{1,3}\.\d{1,3}"

# Use `re.findall()` on `pattern` and `log_file` and assign `valid_ip_addresses` to the output 
valid_ip_addresses = re.findall(pattern, log_file)

# Assign `flagged_addresses` to a list of IP addresses that have been previously flagged for unusual activity
flagged_addresses = ["192.168.190.178", "192.168.96.200", "192.168.174.117", "192.168.168.144"]

# Iterative statement begins here
# Loop through `valid_ip_addresses` with `address` as the loop variable
for address in valid_ip_addresses:
    # Conditional begins here
    # If `address` belongs to `flagged_addresses`, display "The IP address ______ has been flagged for further analysis."
    if address in flagged_addresses:
        print("The IP address", address, "has been flagged for further analysis.")
    # Otherwise, display "The IP address ______ does not require further analysis."
    else:
        print("The IP address", address, "does not require further analysis.")

The IP address 192.168.152.148 does not require further analysis.
The IP address 192.168.22.115 does not require further analysis.
The IP address 192.168.190.178 has been flagged for further analysis.
The IP address 192.168.213.128 does not require further analysis.
The IP address 192.168.96.200 has been flagged for further analysis.
The IP address 192.168.247.153 does not require further analysis.
The IP address 192.168.174.117 has been flagged for further analysis.
The IP address 192.168.148.115 does not require further analysis.
The IP address 192.168.103.106 does not require further analysis.
The IP address 192.168.168.144 has been flagged for further analysis.
```

## Python for automation
- Python can be used to automate security tasks in CI/CD Pipeline (Continuous Delivery/Deployment)
  	- SAST - Static Application Security Testing: scripts can be written to start SAST tools that look at your 	code for weaknesses before it gets built. Python can also be used to understand the SAST results, create 	reports, and automatically stop the process if serious security problems are found.
  	- DAST - Dynamic Application Security Testing: Python can be used to automatically run DAST tools to test 	software while it’s running in a test area. Then, Python scripts can look at the DAST results and give 		feedback in the CI/CD pipeline.
  	- SCA - Software Composition Analysis: Python can work with SCA tools to check your software’s 			dependencies for weaknesses. Dependencies are things like open source code and components from other 		companies. Scripts can control the SCA process, report problems, and set rules based on the severity of 	weaknesses.
 
- Automated Vulnerability Scanning Python scripts can organize vulnerability scans of things like container images, infrastructure settings, and the CI/CD pipeline itself. You can use Python to schedule these scans, collect the results, and send alerts when new vulnerabilities are discovered.
Compliance Checks 

- Python scripts can automatically check for compliance. For example, scripts can check if code follows secure coding rules or if infrastructure settings meet security guidelines. You can then use Python to make reports about compliance and ensure security standards are followed.
Secrets Management Automation 

- Python is key for automating secure secrets management. Scripts can be used to review through code and stop private credentials from being directly written in the code. Also, Python scripts can work with secret management tools (like HashiCorp Vault) to safely get and put secrets into applications during automated releases.
Policy Enforcement 

- "Policy as Code" and Python scripts work together to automatically enforce security policies. Python can be used to define and understand security policies. Then, scripts can check pipeline steps against these policies. If policies are broken (for example, if too many vulnerabilities are found), Python can automatically stop releases.

## Work with Files within Python
- with open(...) as file: - should be thought of as opening a file, and then will automatically "close" the file
	- "with" - handles errors and manages external resources
 	- "open()" - opens a file in python
  	- ".read" - converts files into strings
   	- "a" - used to append
    	- "w" - used to write new file, or OVERWRITE existing file
     		- With both "w" and "a", you can use the .write() method.
   ### "w" - write - can only be done with strings! so you must convert a list back into a string before writing
- below file is a variable that contains the file information as long as we're inside the with statement.
- similar to a loop, with statements start an indent on the next line. This tells Python that this code is happening inside the with statement
- "file_text = file.read()" - uses the read() function to turn the file into a string and store that inside a new variable, called "file_text". 
```
#Open a text file
with open("login_attempts.txt", "r") as file:
	file_text = file.read()
print(file_text)

elarson
errab
bmoreno
```

### Parse a text file
- Parsing - the process of converting data into a more readable format
-".split()" - converts a string into a list, based on spacing
- you use: print(file_text.split())
	"We are learning about parsing!" --- ["We", "are", "learning", "about", "parsing!"]
 - ALSO, after printing, you can create the split into a new file by creating a new variable:
   	- usernames = file_text.split()
### If you do not pass an argument into .split(), it will separate the string every time it encounters a whitespace.
- below uses (",") argument to use a comma to parse it into a list, since there are no spaces to do it automatically
```
approved_users = "elarson,bmoreno,tshah,sgilmore,eraab"
print("before .split():", approved_users)
approved_users = approved_users.split(",")
print("after .split():", approved_users)
```
### Why are things copied to the memory of the computer and not the HD
1. Speed
    RAM (Random Access Memory) is much faster than disk storage (HD or SSD).
    Reading and manipulating data in RAM is nearly instantaneous compared to reading/writing files on disk.
    So Python reads a file into RAM to allow fast operations (like .split(), slicing, etc.).
2. Safety
    Automatically saving to disk could accidentally overwrite data.
    Working in RAM allows you to process or test things without affecting your actual files.
    It gives you the choice to save the result only if and when you're ready.
3. Temporary Use
    Often you only need the data once — to count words, extract values, or parse something.
    There's no need to save the processed version unless you explicitly want to preserve it.
    So memory is the logical place to hold it temporarily while your program runs.
### Things will be stored in RAM until python is closed 
- below shows how after you've used "with" to open and copy the file into a read format in the updates variable, that the next line is not indented. not indenting it, closes the "with" command/closes the original file. so the split is done on the copy that exists in memory. but by closing the file, it frees up resources within the computer. so it's good practice to close things asap to save energy/memory space
```
with open("update_log.txt", "r") as file:
    updates = file.read()
updates = updates.split()
```
- .join() - converts a list into a string, using a separator that you provide
  	- BELOW USE THE QUOTES!
  	- ",".join(approved)_users or "|".join(approved_users) or " ".join(approved_users)  
  	- "\n.join(approved)users -- will separate by placing on separate lines  
- Below takes the updates variable and turns it back into a string separated by spaces, and then writes it to the original file
```
updates = " ".join(updates)
with open("update_log.txt", "w") as file:
    file.write(updates)
```
- Below appends the original import file by directly adding the missing_entry file to the end
### Also, as seen below, after writing a file, you must re-open in "read" mode, in order to print/read it
```
# Assign `import_file` to the name of the text file that contains the security log file
import_file = "login.txt"

# Assign `missing entry` to a log that was not recorded in the log file
missing_entry = "jrafael,192.168.243.140,4:56:27,2022-05-09"

# Use `open()` to import security log file and store it as a string
# Pass in "a" as the second parameter to indicate that the file is being opened for appending purposes
with open(import_file, "a") as file:
    # Use `.write()` to append `missing_entry` to the log file

    updates = file.write(missing_entry)

# Use `open()` with the parameter "r" to open the security log file for reading purposes
with open(import_file, "r") as file:

    # Use `.read()` to read in the contents of the log file and store in a variable named `text`
    text = file.read()

# Display the contents of `text`
print(text)

username,ip_address,time,date
tshah,192.168.92.147,15:26:08,2022-05-10
dtanaka,192.168.98.221,9:45:18,2022-05-09
jrafael,192.168.243.140,4:56:27,2022-05-09
```
```
#Open, read, and split a text file
with open("login_attempts.txt", "r") as file:
	file_text = file.read()
 usernames = file_text.split()
#create a function that counts a user's login attempts
 def login_check(login_list, current_user):
# You initialize a counter
 	counter = 0
# You loop through each item
  	for i in login_list:
# Check each item
   		if i == current_user:
# Increase the counter each time
     			counter = counter + 1
# After the loop is done, you check if that user tried logging in 3 or more times.
	if counter >= 3:
 		return "You failed"
   	else:
    		return "You succeed"

login_check(usernames, "eraab")
"You succeed
```

```
# Define a function named `update_file` that takes in two parameters: `import_file` and `remove_list`
# and combines the steps you've written in this lab leading up to this

def update_file(import_file, remove_list)

    # Build `with` statement to read in the initial contents of the file
    with open(import_file, "r") as file:

        # Use `.read()` to read the imported file and store it in a variable named `ip_addresses`
        ip_addresses = file.read()

    # Use `.split()` to convert `ip_addresses` from a string to a list
    ip_addresses = ip_addresses.split()

    # Build iterative statement
    # Name loop variable `element`
    # Loop through `ip_addresses`
    for element in ip_addresses:

        # Build conditional statement
        # If current element is in `remove_list`,
        if element in remove_list:

            # then current element should be removed from `ip_addresses`
            ip_addresses.remove(element)

    # Convert `ip_addresses` back to a string so that it can be written into the text file 
    ip_addresses = " ".join(ip_addresses)       

    # Build `with` statement to rewrite the original file
    with open(import_file, "w") as file:

        # Rewrite the file, replacing its contents with `ip_addresses`
        file.write(ip_addresses)

# Call `update_file()` and pass in "allow_list.txt" and a list of IP addresses to be removed
update_file("allow_list.txt", [192.168.25.60", "192.168.140.81", "192.168.203.198])

# Build `with` statement to read in the updated file
with open("allow_list.txt", "r") as file:

  # Read in the updated file and store the contents in `text`
  text = file.read()

# Display the contents of `text`
print(text)
```
## Debug Python Code
### Errors
	- Syntax errors - involve invalid usage of the python language (forgetting to add a colon)
 			- misspelling the python keyword elif by typing elsif
    			- EOL - End of Line
 	- Logic errors - instances when code is written incorrectly in terms of what you want it to do
  			- so it may not cause error messages to be produced, but instead make unintended results
     				- ex. a less than sign (<) , when it should have been less than or equal to (<=)
	 	* in order to diagnose
   			- 1) should use print statements to identify which sections of the code are working properly
      			- 2) use a debugger - which inserts breakpoints in the code, into sections and run just one 			portion of the code at a time.
	 - An Exception - happen when the program doesn't know how to execute code even though there are no problems 			with the syntax.
  			- ex.   - when something is mathematically impossible (divide by 0)
    				- when you ask python to access index values that don't exist 
       				- when python doesn't recognize variable or function mames
	  			- when you use an incorrect data type
      			- can also use a debugger to find out the issue
	 
      			- "IndexError" - when you place an index in bracket notation that does not exist in the 			sequence referenced. 
	 		usernames = ["bmoreno", "tshah"], print(usernames[3].... but 3 doesn't exist
      			- "TypeError" - results from using the wrong data type. Using a string value in math equation
	 		- "FileNotFound" - occurs when  you try to open a file that doesn't exist in that location
	 
