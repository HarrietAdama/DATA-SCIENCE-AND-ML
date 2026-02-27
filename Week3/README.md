LAB TITLE: DATA STRUCTURES PART2: ARITHMETIC OPERATORS, COMPARISON OPERATORS, LOGICAL OPERATORS, ASSIGNMENT OPERATOR, BITWISE OPERATOR, MEMBERSHIP OPERATOR, IDENTITY OPERATOR

LAB TITLE: STRINGS & CONTROL FLOW

OBJECTIVE:The objective of the lessons taught in week3 was a continuation of the part 1 of  data structures that was taught in week2 and in week 3 we were taught how to use the different types of opertors in python to gain the ability to:

1.To perform basic mathematical calculations(+,-*,/) and advanced computations, such as modulus(%) or floor division(//).

2. To learn how to use the(==,<,>) operators to compare and combine conditions using the logical operators(and, or, not) which allows programs to make decisions and execute conditional workflows.
 
3. To learn how to use the in(membership) and is(identity) operators to verify if data exists within a collection or to check the memory or storage of the data.
   
4.To learn how to use the bitwise operators(&,|,~,^,<<,>>) for data manipiulation.  

TOOLS USED: The tools used are: Google Colab, Jupyter notebook, Python.

STEP BY STEP PROCESS

The following is the step by step process of producing labs in the class in week 3:

ARITHMETIC OPERATOR

- I started with the Arithmetic operators which consist of addition(+), subtraction(-), multiplication(*), modulo(%), floor division(//), exponentiation(**).
  
- I called two variables x and y and assigned values to them respectively which we used the arithmetic operators to perform mathematical calculations and produced outputs from each operator.

COMPARISON OPERATOR

-  I used the comparison operators(<,>,==,<=,>=) to compare conditions and produced boolean outputs from each operator.

LOGICAL OPERATOR

-  I used the logical operators(AND,OR,NOT) to compare and combine statements using the comparison operators to see whether a statment was TRUE or FALSE.

  ASSIGNMENT OPERATOR
  
-  I used the assignment operator to values to variables such as: x=3 or x-=3.

  BITWISE OPERATOR

-  I used the bitwise operator(&,|,~,^,<<,>>) to reference integers in the binary level, that is, in 0's and 1's.

  MEMBERSHIP OPERATOR

- with the membership operator, I used the IN and NOT IN operator to check whether a particular value exists or does not exist in a sequence or collection.

IDENTITY OPERATOR

- I used the identity operator IS and IS NOT operator to check for the storage or memory of the variables not the value of the variables.
  

  STRING & CONTROL FLOW: with the strings and control flow we are looking at the order the program's statements is executed. Strings are immutable so they cannot be changed or modified after they have been created so the methods used here does not alter the string called and any operation that seems to modify the string creates a new string in memory. Therefore, we use these methods in the control flow of the strings:
  

  -UPPERCASE: I used the uppercase function to determine whether the letters in the string called is all in uppercase.

  -LOWERCASE: I used the lowercase function to determine whether the letters in the string called is all in lowercase.

  -ISDIGIT: I used the isdigit function to check to see if there are any digits in the string called.

  -ISALPHA: I used the isalpha function to check to see if the letters in the string called is all alphabets.

   -ISLOWER: I used the islower function to change the string called to lowercase letters.

  -ISUPPER: I used the isupper function to change the string called to uppercase letters.

  -SPLIT: I used the split function to divide the each word in the string into individual components.

  - JOIN: I used the join function to join the split components with a hyphen.
 
  - REPLACE: I used the replace function to replace specfic words in the string called.
 
  - STARTSWITH: I used the startswith function to check to see what an element starts with.
 
  - ENDSWITH: I used the endswith function to check to see what an element ends with.
 

    COMMANDS EXECUTED

    ARITHMETIC OPERATOR


#ADDITION(+)
x=5
y=6
print(x+y)     # OUTPUT 11


#SUBTRACTION(-)
x=3
y=6
print(y-x)     #OUTPUT 3


#MULTIPLICATION(*)
x=2
y=4
print(x*y)    # OUTPUT 8



#DIVISION
x=30
y=3
print(x/y)     # OUTPUT 10


#FLOOR DIVISION(//)
x=10
y=3
print(x//y)      #OUTPUT 3


MOUDLO(%)
x=500
y=6
print(x%y)    # 2


#EXPONENTIATION(**)
x=5
y=3
print(x**y)    # 125


COMPARISON OPERATOR

GREATER THAN(>)
x=64
y=33
print(x>y)  #TRUE


LESS THAN(<)
x=23
y=16
print(x<y)   #FALSE


EQUAL TO(==)
x=42
y=22
print(x==y)   #FALSE


#GREATER THAN OR EQUAL TO(>=)
print(x>=y)     #TRUE


LESS THAN OR EQUAL TO(<=)
print(x<=y)  #FALSE

NOT EQUAL TO(!=)
print(x!=y)  #TRUE

LOGICAL OPERATORS

x=16
y=23
#AND
print(x>y and y>x)   #FALSE


#OR
print(x>y or y>x)  #TRUE

#NOT
not(x<16)   #TRUE

ASSIGNMENT OPERATOR

x=65
x    #65


ADDITION
x+=12
x   #77


SUBTRACTION
x-=12
x   #65

MULTIPLICATION
x*=12
x   #780


DIVISION
x/=12
x   #65

#FLOOR DIVISION
x//=12
x    #5.0


#EXPONENTIATION
x**=12
x     #244140625


BITWISE OPERATOR

x=10
y=2

 USING THE & OPERATOR
print(x&y)   #2

print(x|y)   #10

 ^ OPERATOR
print(x^y)   #8

~ OPEARTOR
print(~x)   #-11

#RIGHT SHIFT(>>)
print(x>>2)   #2

LEFT SHIFT(<<)
print(x<<2)   #40

MEMBERSHIP OPERATOR

b=(1,2,3,4,5)

print(4 in b)  #TRUE

print(4 not in b)  #FALSE


IDENTITY OPERATOR

a=(1,2,3,4,5)
b=(1,2,3,4,5)


print(a is b)  #FALSE

print(a is not b)  #TRUE


STRING AND CONTROL FLOW


name= "Dangote INC"
name

#upper()
name= name.upper()
name               #"DANGOTE INC"

#ISALPHA
name= name.isalpha() 
name      #FALSE


#lower()
name= name.lower()
name              #"dangote inc"

ISDIGIT
name= name.isdigit()
name           #FALSE

#ISLOWER
name= name. islower() 
name     #FALSE

 #ISUPPER 
 name= name.isupper() 
 name      #FALSE

 ballet= "All ballerinas are athletic"
ballet                                  #"All ballerinas are athletic"

ballet= "All ballerinas are athletic"
ballet.split(" ")                  #"All", "ballerinas", "are", "athletic"

#JOIN
word= ballet.split(" ")
print("_".join(word))             # All_ballerinas_are_athletic


#replace
word= ballet.replace("athletic","graceful")
print(word)                                 #"All ballerinas are graceful"


#STARTSWITH: TO CHECK WHAT A STRING STARTS WITH
flowers = "Tulips"
flowers.startswith("o")                        #FALSE




#ENDSWITH: TO CHECK WHAT A STRING ENDS WITH
flower= "Peonies"
flower.endswith("s")             #TRUE



KEY OBERVATIONS/LESSONS LEARNED

The following are my key observations and lessons I learned:

-I observed that with strings every letter counts, even a space count and its very important.

-I learned how to perform advanced and basic mathematical calculations using the operators which makes calculations less tedious.

 - I also learned the idea behind some of the operators in the bitwise operators such as the XOR rule in obtaining outputs.

 - I learned how to combine the logical operators and the comparison operators to determine whether a statement was true or false.

 - I learned how to use the functions in strings and control flow to manipulate data.

