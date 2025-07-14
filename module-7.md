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
    
  "# Print Hello Python"     ----- don't use quotes
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
     
    -   device_id = "mr5lkvi"  
        data_type = type(device_id)  
        print (device_type)  
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

  - "elif" - precedes a condition that is only evaluated when previous conditions evaluate to False. Unlike with else, there             can be multiple elif statements following if.

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

        - in above statement, the "not" operator inverts whether conditions are met in order to print. so if both things are                 not met, then it will PRINT.
        - MUST USE PARENTHESES AFTER "NOT", SO THAT BOTH ASPECTS ARE INCLUDED!

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

  ### While Loops
   
   - repeatedly execute a function, but the repetition is based on a condition you create before.
   - "while" indicates the beginning, followed by the condition, that contains the loop variable,
             in this case "time"
             - so you assign the variable beforehand, and then reference in the loop. 
      
  - so in the below statement, time = 0 is the variable, and then underneath is the condition using it
    - in the indented body, it consists of the actions to take while the loop iterates
    - so the first line prints the current variable (0), and then print every two minutes; so this will.
      only print out even numbers less than or equal to 10. 
-
        time = 0.   
        while time <= 10:   
          print(time)  
          time = time + 2. 

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
