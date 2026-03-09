# LAB TITLE: STRINGS & CONTROL FLOW, IF STATEMENTS, IF-ELSE STATEMENTS, NESTED IF, IF-ELIF-ELSE STATEMENTS, TENARY OPERATORS, LOOPS:  FOR LOOP & WHILE LOOP, FUNCTIONS& MODULES, LAMBDA FUNCTIONS, BUILT-IN FUNCTIONS, PANDAS, DATA MANIPULATION, DATA COMBINATION

# STRING & CONTROL FLOW

# STRINGS FORMATTING: With strings formattig it allows you combine text and variables together seamlessly. We have three(3) types of strings formatting and they are:

1. the one we use the + sign to combine text and variables
   # example
   
   name = 'Harriet'

   age = 54

   print('Hello, my name is ' + name + ' and I am ' + age + ' years old')
   # Output  Hello, my name is Harriet and I am 54 years old
3. f-string method: With this method, you introduce f before writing what you want in quotation marks then to add the variables and text which was already called in a curly bracket{}.
 
  # example
  

  name = 'Stanley'

  age = 21

  print(f'Hello, my name is {name} and I am {age} years old'.)

  # output    Hello, my name is Stanley and I am 21 years old.

  4. .format() method: this allows for more complex string formatting by using placeholders and format specifiers.

# EXAMPLES

people ='gentiles'

number= 5

print('Jesus fed the {0} with {1} loaves of bread.'.format(people, number))

# output    Jesus fed the gentiles with 5 loaves of bread.

people = 'gentiles'

number1 = 5

number2 = 2

print('Jesus fed the {people} with {number1} loaves of bread and {number2} fish.'.format(people=people, number1=number1, number2=number2)
# output    Jesus fed the gentiles with 5 loaves of bread and 2 fish.


# CONTROL FLOW: IF STATEMENTS, LOOPS, AND CONDITIONAL STATEMENTS

# IF STATEMENTS: This allows you to execute code conditionally based on the evaluation of an expression or condition.

# SYNTAX

# IF STATEMENT
x = 10
if x>0 and x%2 ==0    # this is the condition that has to be met for it to be able to print that x is an even number
print('x is an even number')


# IF-ELSE STATEMENT: This allows you to execute different block of codes basedon the evaluation of a condition.

# SYNTAX

IF CONDITION
# CODE BLOCK TO EXECUTE IF CONDITION IS TRUE

ELSE:

# CODE BLOCK TO EXECUTE IF CONDITION IS FALSE

# EXAMPLE

x= 15

if x>0 and x%2==0:

print('x is an even number')

else:

print('x is an odd number')

# NESTED IF

age = 14
 if age >= 18:
 if age < 21:
 print('You are an adult but not allowed to drink')
 print('You are an adult and allowed to drink')
 else:
 print('You are underage)

 # IF-ELIF-ELSE STATEMENTS: This allows you to test multiple conditions sequentially and execute corresponding blocks of code of the first true condition.
condition 1

 # code block to execute if condition is True

 elif condition or condition 2

 # code block to execute if condition is True

 else:
  # code block to execute if all conditions are not met/ False.

# example
  
score= 98
if score >= 90:
   print('A')
elif score >=80:
   print('B')
elif score >=70:
    print('C')
else:
     print('Fail')
  # output   'A'


 # TENARY OPERATORS: This is a concise way to express conditional statements.

 num = 10

 result= 'Positive' if num>0 esle 'Negative'

# output   Positive
 # LOOPS
 
 -FOR LOOP
 
 -WHILE LOOP

 # FOR LOOP: It is used to iterate over a sequence( such as list, tuple, string) and execute block of code for each element in the sequence.

 SYNTAX
 For item in iterable/sequence:
 # code block to execute for each item

 # EXAMPLE:

 list_ = ['apple', 'mango', 'strawberry','kiwi']
 for item in list_:
 print(item)

 # output  apple
           mango
           strawberry
           kiwi

 # the item or i= depends on how you want to define each element(s) in the list.

 # ITERATING OVER A DICTIONARY

 person = {'name':'Jonah', 'age': 34, 'location': 'Lima'}
  # we have a dictionary which uses 'key and value pairs' so our items in the dictionary would not be 'i or items' but key and value and our variable name is 'person', so hence, we have:
   for key, value in person:
   print(f'{key}:{value}')

   # output  name: Jonah
             age : 34
             location : Lima

   # WHILE LOOP: While loop repeatedly executes block of codes as long as a specified condition is True.

   SYNTAX
   While condition:
   # the code will be executed if the condition is True or met.

   # Looping and printing a value:

   i = 1
   while i<= 10
   print(i)
   i=+1
   # output  1
             2
             3
             4
             5
             6
             7
             8
             9
             10

 - First, you need to specify your variable which is(i =1), then set your condition (while i<=10). Lastly, set an ending(i=+1).


# Looping over a list and printing the items in the list.

emma=['Tomatoes', 'Carrot', 'Cabbage']
i= 0
while i<=2
i=+1
print(emma[i])

# OUTPUT    Tomatoes
            Carrot
            Cabbage

# STEPS:

-Make or call your list

-Specify your variable(i=0)

- Set your condition(while i<=2)
  
-Set an ending limit(i=+1)

- Then you print your output

# FUNCTIONS AND MODULES

Functions are blocks of reuseable code that perform a specific task. You can use it at all times so far as it is being defined already.

- To call a function:
  
- definition of the function
  def add(a,b):

- Code block

- Outcome you want to see

  # EXAMPLE

  def add(a,b)
  provide arugments a and b. You can provide the number of arguments you want.

  c= a+b

  return c

  add(4,5)
  
  # output   9

  # you can do it for subtraction, multiplication, exponentiation etc. You just need to define your function and it would do the calculation for you.


# FUNCTION TO GREET A USER

def greet(name)

return f'Hello,{name}!'

message= greet("Sophie")
print(message)

# output   Hello, Sophie!

# LAMBDA FUNCTION: This function is a small anonymous function that is written in one line.

- It is used when you need a quick function without formally defining it.

# adding numbers

add = lambda x,y:x+y

* x,y - are my parameters
* x+y - is my expression

# EXAMPLE

add = lambda x,y:x+y
print(add(3,6))     # 9

subt= lambda x,y:y-x
print(subt(4,9))     # 5

mult= lambda x:x*x
print(mult(4))    # 16

# USING THE LAMBDA FUNCTION FOR DICTIONARIES

Students = [{'name':'Sophie', 'Score':78},{'name':'Jayden','Score':90}]

# we are sorting the students by their names and scores so we use the sorted method here:
sorted_students= sorted(students, key=lambda x:x['name'], reverse=True)

 # in this case we are sorting by the names of the students not their score. The reverse function there gives the order of sorting. That means, we can also sort my score so the reverse of sorting by score is true and possible.

 print(sorted_students)
   [{'name': 'Xena', 'score': 75}, {'name': 'Abel', 'score': 90}]


 # BUILT-IN FUNCTIONS

# MAP FUNCTION: This function matches each item in the iterable or sequence and returns a new iterable with the results. 

 # FINDING THE SQUARE OF THE NUMBERS IN THE LIST

 numbers = [1,2,3,4,5]
 squared_num = map(lambda x:x**2, numbers)
 print(list(squared_num))

# output  1, 4, 9, 16, 25

# FILTER FUNCTION: It filters the entity you are working on. The function must return True or False.
# It will only return the elements that satisfy the condition.

# EXAMPLE

numbers = [1, 2, 3, 4, 5, 6]
filtered_numbers = filter(lambda x:x % 2 ==0, numbers)
print(list(filtered_numbers))

# 2, 4, 6

# FILTERING OUT NEGATIVE NUMBERS FROM A LIST OF NUMBERS.
numbers = [4, 8, -2, 3, -6, -12]
neg_numbers = filter(lambda x:x > 0, numbers)
print(list(neg_numbers))

# 4, 8, 3

# REDUCE FUNCTION: This takes a collection and reduces it to a single value by repeatedly applying a function.
- combines a group of elements into one final result.
- You need to import the reduce function from functools

  # EXAMPLE

from functools import reduce 
numbers = [1, 2, 3, 4, 5]
product = reduce(lambda x, y:x*y, numbers)
print(product)

# 120

numbers= [1, 2, 3, 4, 5, 6]
add_numbers = reduce(lambda x, y:x + y, numbers)
print(add_numbers)

#  21

# MAXIMUM FUNCTION: This look for the maximum element within the list. It uses the reduce function to reduce or remove all other elements that do not satisfy the condition.

# EXAMPLE

numbers = [3,8,1,6,10]
max_num= reduce(lambda x,y:if x>y else y, numbers)
print(max_num)      # 10

# MINIMUM FUNCTION: This returns the minimum or lowest element in the list or iterable.

# EXAMPLE

numbers =[2,4,6,8,0]
min_num= min(numbers)
print(min_num)             # 0

# PANDAS: Pandas is a powerful library in python for data manipulation and analysis. It has two primary data structures and they are:

-SERIES: A series is a one-dimensional data structure and it is capable of holding any data type.

# creating a series from python
s= pd.Series([1,2,3,'Toys',6,'Candybars'])

-DATAFRAME: is a a multi-dimensional data structure. This is similar to spreadsheet and SQL table with rows and columns.

# creating a DataFrame

df = {'names':['Sandra','Humphrey','Ines'],'age':[21,45,12],'Locatio':['Tehran','Lima','Peru']}

data=pd.DataFrame(df)
print(data)

-Converts all the keys as column names.

-Put under each column their respective values.

# DATA MANIPULATION: In data manipulation we have two types:

-Indexing: You can access a single element in the iterable.

-Slicing: You can locate a range of elements in the iterable.\

# USING THE INDEX METHOD

x= [1,2,3,'Angels','Heaven',21]

print(x[3])   # Angels

# this means that at index/ position 3 the element 'Angels'can be found or located.


# With Slicing it is going to pick a range of elements in the iterable.

# []-single square bracket indicates a Series.

# [[]]- double square brackets indicates a DataFrame.

# USING THE SLICING METHOD

# using the slicing method
x= {'name':['Hocket','Ahmed','Sarah'], 'age':[23,35,40], 'location':['Istanbul', 'Kuwait', 'Doha']}
df = pd.DataFrame(x)
print(df)

# Slicing a DataFrame
df[['name']]                    #Accessing a column

df[['location']]

# DATA COMBINATION: Data combination is the process of joining, merging, and concatenating multiple pandas data structure into a single data structure.

# We have:

- joining method

- merging method

- Concatenation method

# CONCATENATION: Thia combines two or more DataFrames with the same columns either vertically or horizontally.

- It has a key word 'Concat'.

- If your dataframes do not have the same columns you cannot use the concatenation method.

  # EXAMPLES USING CONCATENATION

 df_1 = pd.DataFrame({'A':[4, 2, 6], 'B':['m', 'n', 'o']})
print(df_1)

# OUTPUT
A  B
0  4  m
1  2  n
2  6  o


df_2 = pd.DataFrame({'A':[45, 8, 9], 'B':['x', 'y', 'z']})
print(df_2)

# OUTPUT
  A  B
0  45  x
1   8  y
2   9  z


# VERTICAL CONCATENATION(ROW-WISE)
vertical_com = pd.concat([df_1,df_2], axis=0, keys=['df_1', 'df_2'])
vertical_com

# OUTPUT
A 	B
df_1 	0 	4 	m
1 	2 	n
2 	6 	o
df_2 	0 	45 	x
1 	8 	y
2 	9 	z

# .LOC MEANS THE LOCATION OF THE VALUES
vertical_com.loc['df_1', 0]

df_1
0
A	4
B	m

# WITH THIS WE ARE LOCATING THE VALUES IN COLUMNS A AND B THAT ARE IN POSITION OR IDEX ZERO(0) AND THESE VALUE ARE 4 AND STRING M.

vertical_com.loc['df_1', 0][0]

# OUTPUT 4

# This gives the value's specific location or position in the DataFrame.

# USING THE IGNORE INDEX FUNCTION IT DOES NOT SHOW THE DF_1 AND DF_2 LABELS IN THE OUTPUT
# So by using the 'ignore index' function, it ignores or does not show df_1 and df_2 labelling in the output.

vertical_com = pd.concat([df_1, df_2], axis=0, ignore_index=True)
vertical_com

# OUTPUT
A 	B
0 	4 	m
1 	2 	n
2 	6 	o
3 	45 	x
4 	8 	y
5 	9 	z

# HORIZONTAL CONCATENATION: WE CHANGE THE AXIS FROM 0 TO 1. THIS JOINS DF_1 AND DF_2 HORIZONTALLY.
horizontal_com= pd.concat([df_1, df_2], axis=1, keys=['df_1','df_2'])
horizontal_com

# OUTPUT
df_1 	df_2
	A 	B 	A 	B
0 	4 	m 	45 	x
1 	2 	n 	8 	y
2 	6 	o 	9 	z


# EXAMPLE
accra=pd.DataFrame({'Town':['Cirlce', 'Madina', 'East Legon'], 'Humidity':[32, 29, 34], 'Temperature':[28, 30, 25]})

kumasi=pd.DataFrame({'Town':['Kejetia', 'Amakom', 'Mantia'], 'Humidity':[27, 39, 36], 'Temperature':[30, 26, 24]})

df_3= pd.concat([accra, kumasi], ignore_index=True)
df_3

# OUTPUT

Town 	Humidity 	Temperature
0 	Cirlce 	32 	28
1 	Madina 	29 	30
2 	East Legon 	34 	25
3 	Kejetia 	27 	30
4 	Amakom 	39 	26
5 	Mantia 	36 	24

df_4= pd.DataFrame({'Windspeed':[8,5,2,4,6,7,9,2,16]})
df_4

# OUTPUT

Windspeed
0 	8
1 	5
2 	2
3 	4
4 	6
5 	7
6 	9
7 	2
8 	16

# to combine windspeed to the accra and kumasi we concate
vertical_com=pd.concat([df_3, df_4], ignore_index=True, axis=0)
vertical_com

# OUTPUT

Town 	Humidity 	Temperature 	Windspeed
0 	Cirlce 	32.0 	28.0 	NaN
1 	Madina 	29.0 	30.0 	NaN
2 	East Legon 	34.0 	25.0 	NaN
3 	Kejetia 	27.0 	30.0 	NaN
4 	Amakom 	39.0 	26.0 	NaN
5 	Mantia 	36.0 	24.0 	NaN
6 	NaN 	NaN 	NaN 	8.0
7 	NaN 	NaN 	NaN 	5.0
8 	NaN 	NaN 	NaN 	2.0
9 	NaN 	NaN 	NaN 	4.0
10 	NaN 	NaN 	NaN 	6.0
11 	NaN 	NaN 	NaN 	7.0
12 	NaN 	NaN 	NaN 	9.0
13 	NaN 	NaN 	NaN 	2.0
14 	NaN 	NaN 	NaN 	16.0

# FROM THIS OUTPUT WE HAVE CONCATENATED VERTICALLY AND ALSO IGNORED THE INDEX, THAT IS WHY WE DO NOT SEE ANY INDEX IN THE OUTPUT AND ALSO WE CAN SEE THAT BY JOINING DF_3 TO DF_4 WE HAVE SOME EMPTY SPACES FOR TEMPERATURE AND HUMIDITY IN THE PARTS OF ACCRA AND KUMASI FOR WINDSPEED.


pd.concat([df_3,df_4], ignore_index=True, axis=1)

# OUTPUT
0 	1 	2 	3
0 	Cirlce 	32.0 	28.0 	8
1 	Madina 	29.0 	30.0 	5
2 	East Legon 	34.0 	25.0 	2
3 	Kejetia 	27.0 	30.0 	4
4 	Amakom 	39.0 	26.0 	6
5 	Mantia 	36.0 	24.0 	7
6 	NaN 	NaN 	NaN 	9
7 	NaN 	NaN 	NaN 	2
8 	NaN 	NaN 	NaN 	16

# WE HAVE CONCATENATED HORIZONTALLY BY CHANGING THE AXIS FROM 0 TO 1.











   



  

           
             
 
 
 








     

