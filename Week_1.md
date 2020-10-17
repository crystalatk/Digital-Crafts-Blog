# The *first* WEEK!

This has been a week full of new skills that are *so far* pretty simple to understand:)

## **This week's skills include:**
- Setting up the "Command Center"
    - Creating our file systems
    - Checking the basic functions of GitHub, VS Code, and Markdown.
- Programming 101!
## **Command Center**
This week, we learned how to navigate our computer without the use of GUI's. 
From a terminal, I can now:
- go to a folder
```terminal
cd DigitalCrafts/classes #goes to my "classes" folder inside of my "DigitalCrafts" folder
```
- create a folder
```terminal
mkdir classes #this creates a "classes" folder in the current directory
```
- create a file
```terminal
touch 1-command.me #this creates a "1-command" file in the current directoy
```
## **Programming 101**
In Programming 101, we are learning some simple commands and we using those commands to create programs.

### The Data Types
- **String**: any characters grouped by " ". This includes words, phrases, numbers, symbols. These are represented as they are typed and are not modified the same way that numbers are.
```python
# /n means new line!
haiku ="Haikus are easy.\nBut sometimes they don't make sense.\nRefrigerator."
print(haiku)

# /t tabs!
tabbed = "Look\tI'm tabbed"
print(tabbed)

# quoted
sarcastic = 'I "really love" talking politics'
print(sarcastic)

# spaces use commas
print("and", "this", "that")
```

- **Numbers**: these are integers. Any positive or negative whole number. 
    - **Floats**: these are used to represent decimals.
- **Booleans**: these are always true or false
### Ways to Combine Strings!
- **concatenate**: 
```python
message = "hello"
print(message + " " + "world")
```
 - **f-string**:
```python
message = "Hello"
name = "Crystal"
print(f"{message}, my name is {name})
```
- **interpolation**:
```python
breed = "Akita"
print("Hello! What a beautiful dog! Is it an %s?" % (breed))
```
### **Basic Commands I've Learned so Far**
### Print
```python
print("I love dogs!") #Result: I love dogs!
```


### Python Operators 
```python
+= # x = x + (Same is true of other operators)
** #Exponents
== #Equal
!= #Not Equal
> #Greater than
< #Less than
>= #Greater than or Equal to
<= #Less than or Equal to
```
## **User Input** 
This is how we interact with users. When we ask for user input, it will relay the request to the user and wait for an answer. That answer can then be used within our program to do all kinds of fun things!
```python
first_name = input("Please tell me your first name:\n")
last_name = input("Please tell me your last name:\n")

print(f"Hello, {first_name} {last_name}. Isn't it a beautiful day for a walk?")
```
Be careful, users can not be controlled. All user inputs return as strings!

## **If/Then Statements** 
These help get things done. We can create an action if something is true. 
```python
if 1 < 3:
    print("this will be printed")
    print("this is the same level")# you can keep going on the same level...
```
We can also use elif and else to expand further on this idea.
```python
age = int(input("How old are you?\n"))  #age will always be an integer now!

if age == 21:
    print("You are a great age to party.")
elif age >= 21:
    print("You are old enough")
elif age >37:
    print("this will never print!")
else:
    print("You are not old enough")
```
It is important to note here that, once something true is found, the block stops. Only the code up to the true point will try to be read.

Also, be sure to double check your indents. They matter! VS code uses the same spacing for tab and four spaces, but things copied from the internet may result in error because of spacing (little gray dots mean spaces and gray arrow means tab)


## **Loops!** 

### **While Loop** 
Self contained, will continue until parameter is met.

### **Infinite Loop** 
A loop that continues infinitely. Control C to stop:)

### **Input to stop a Loop** 
``` python
name = ""
while name != "Star":
    name = input("Please say your name is Star.\n")

print("Great, I knew you could do it.")
```
This will appear as a request to the user "Please say your name is Star.", then it will continue to ask for that until you satisfy the parameters.

Loops can be more complicated...
```python
user_name = ""
password = ""
i = 0


while i <= 10 and user_name != "Daisy" and password != "flower":
    i += 1
    if i == 11:
        print("You suck!")
        break
    print(f"attempt {i}")
    user_name = input("What is your username?\n")
    password = input("What is your password?\n")

if i <11:
    print(f"Welcome, {user_name}! So glad you could make it!")
```

Fun tip! Put the try in a while True and break the while true loop when the try works!

Example:

```python
while True:
    try:
        bill = float(input("How much was your total bill?\n$ "))
        break
    except ValueError:
        print("Your bill should be a number.")
service = input("How was your serivce today?\nPlease choose: Good, Fair, or Bad\n")
service_u = service.upper()
if service_u == "GOOD":
    tip_multiplier = .2
elif service_u == "FAIR":
    tip_multiplier = .15
elif service_u == "BAD":
    tip_multiplier = .1
else:
    print("Please choose the level of service using the terms: Good, Fair, or Bad.\nThanks!")
    exit()
tip_f = bill * tip_multiplier
tip = "${:,.2f}".format(tip_f)
total = "${:,.2f}".format(bill + tip_f)
print(f"Tip amount: {tip}")
print(f"Total Amount: {total}")
```


## **Errors** 
Common Errors
    - Type Errors
    - Value Errors
    - Zero Division Errors

Example in dealing with Errors:
```python
try:
    100 / int(input("Give me a number\n"))
except ZeroDivisionError:
    print("You tried to divide by 0")
except TypeError:
    print("You did something wrong with the type")
except ValueError:
    print("You didn't give a number! I said a number!")
```
Note: The try/except is very useful when dealing with a variable you can't control, like a user input.

## **Nesting** 
As shown up in the Loop section, Nesting involves putting blocks inside of other blocks.
```python
name = input("What is your name? ")
if len(name) > 3:
    print("Your name is long enough.")
    if len(name) > 15:
        print("That is way too long.")
    else:
        print(f"Welcome, {name}.")
```

# **Put it all together for some practices!** 
Here you will see:
- use of numbers
- use of strings
- user input
- changing the type of input from a string to a number
- a loop!
- checking for errors
- printing a result to our user!

```python
try:
    start = int(input("Choose any whole number to start with.\n"))
    end = int(input("Choose any whole number to end with.\n"))
    while start <  end:
        start += 1
        print(start)
except ValueError:
    print("I said, choose a whole number!")
```

And one more because we don't want to forget our if statements!

```python
print("Let's guess a day of the week!")
try:
    day = int(input('Pick a Day (0-6)? '))
    if day == 0 or day == 6:
        print("Sleep in")
    elif day >0 and day < 6:
        print("Go to work")
    else:
        print("This does not follow our days of the week. Please enter a number between 0 & 6")
except ValueError:
    print("Cannot Process. Please enter a number from 0 - 6.")
```
It's been a good week!