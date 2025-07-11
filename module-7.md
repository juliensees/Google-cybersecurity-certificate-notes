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

##Python Environments
  - Notebooks - online environment for writing, storing, and running code (Jupyter Notebook & Google Colaboratory)
      - Code Cells - meant for writing and running code. has a "play" button
      - Markdown Cells - meant for describing code
  - IDE (Integrated Development Environment) - app for writing code, that gives editing help and error correction tools, uses gui
  - CLI (Command-Line Interface) - text based interface that can also run python

#Core Python components

  #Data type - a category for a particular type of data item
   - String data - data consisting of an ordered sequence of characters (must be placed within quotations or apostrophes!!)
   - Numeric data - does NOT use quotation marks
       - Float data - consists of a number with a decimal point (whole numbers also get a decimal -- 2.0)                                 - / symbol is a divide, but // divides and returns as rounding down to the nearest whole number 
       - Integer data - consists of a number without a decimal point
   - Boolean data - can only be one of two values (true or false)
   - List data - data structure that consists of a collection of data in sequential form
        - entirety of list must be placed within brackets [ ]  , and separated by commas, -ex. print (["estrada", "zamboni"])
   - Tuple data - data structure that consists of a collection of data that cannot be changed. Like lists, tuples can                   contain elements of varying data types
           - tuple data cannot be changed (unlike list data)
           - placed in parentheses vs list data in brackets
   - Dictionary data - is data that consists of one or more key-value pairs.
           - Each key is mapped to a value. A colon (:) is placed between the key and value. Commas separate key-value pairs             from other key-value pairs, and the dictionary is placed within curly brackets ({}).
   - Set data - data that consists of an unordered collection of unique values. This means no two values in a set can be the             same.
           - Elements in a set are always placed within curly brackets and are separated by a comma. These elements can be               of any data type.

   #Variable - a container that stores data  
       - username = "jrafael"  assigns the variable username a value of "jrafael"  
       - The syntax for assigning a variable requires a name for the variable, then an equals sign (=), and finally the               value for the variable. 
