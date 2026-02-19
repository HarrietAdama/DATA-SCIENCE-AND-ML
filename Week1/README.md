#Lab Title
DATA STRUCTURES PART 1: Lists, Tuples, and Dictionaries
Objective
- the objective of this is to enable students to learn how to efficiently organize and store datasets since they are the foundation of data science.
  Tools Used
  The following tools were employed:
  -Google Colab
  -Python
  -Jupiter
  Step-by-Step Process
  the following are the step-by-step process in learning about the part1 of data structures:
  #Lists
  -With list, I learned that lists are ordered collection of items in python that are mutable, meaning that, they can be altered or modified after creation. They can be created using list() or a square brackets[]. lists have many methods since they can be modified and they are:
  - Append(): it is used to add or append a new item/element to the end list.
  - extend(): it is used to add items or elements from one list to the existing list.
  - insert(): it is used to insert an item/element to a specified location. For example: if you want to insert 10 at the position of 2 in a list you use the insert method(insert 10 at index 2).
  - remove(): it is used to remove the first occurrence of a specified value or element from the list.
  - pop(): it is used to remove and return an item or element from a specified position in the list.
  - index(): it is used to find the position of an element in a list.
  - count(): it gives the number of times a specified value or element has ocurred in a list.
  - sort(): it is used to generate the list in ascending order.
  - reverse(): it is used to reverse the sort method.
#TUPLES
  - With tuple, I learned that tuples are also a collection of items or elements in python but the difference between it and lists is that, tuples are immutable, meaning that, they cannot be altered or modified after creation. They can be created used the normal parenthesis symbol() or tuple(). Since tuples cannot be modified we have only two methods in tuples and they are:
  - index() and count()
 #DICTIONARIES
  - With dictionaries, they are an unordered collection of key-value pairs. They are mutable and are good for storing data.
  - They are created using the curly brackets{} or dict(). The folloing are the methods in dictionaries:
  - clear(): it is used to remove all key-pair values from the dictionary.
  - copy(): it is used to create a shallow copy of the original dictionary.
  - get(): it is used to obtain the value of a specific key.
  - items(): it is used to show or display the view object of key-value pairs.
  - keys(): it is used to show or display the view object containing keys.
  - values(): it is used to display the view object containing values.
  - pop(): it is used to remove and return an arbitrary key-value pair.
  - update(): it is used to add a specified key-value pair from another dictionary.
 
Commands Executed
-the following are the commands executed in each of methods under the data structures mentioned above:
#LISTS
-Append(): my_list=[1,2,3,4,5]
my_list.append(6)   #this command will add 6 to the my_list
[1,2,3,4,5,6]
-Extend():
my_list.extend([7,8,9])  #this command will add the numbers from this list of 7,8,9 to my_list
[1,2,3,4,5,6,7,8,9]
insert():
my_list.insert(3,10)   #this will insert 10 at the position/index of number 4
[1,2,3,10,4,5,6,7,8,9]
-Remove():
my_list.remove(4)   #this removes the first occurrence of 4 from the list
[1,2,3,10,5,6,7,8,9]
-Pop():
popped_element= my_list.pop(4)
print(popped_element)   #this removes the number 5 from the list
print(my_list)  #this prints out this list [1,2,3,10,4,6,7,8,9]
-Index():
index=my_list.index(10)   #this will give you the position occurrence of the number 10 in the list and wwhich is 3
-Count():
count= my_list.count(2)    #this wwill give you the occurrence or the number of times the number has appeared in the list and which is 1
-Sort():
my_list.sort()
print(my_list)                #this prints the list in ascending order [1,2,3,4,6,7,8,9,10]
-Reverse():
my_list.reverse()
print(my_list)                #this prints the list in the reverse order [10,9,8,7,6,4,3,2,1]

#TUPLES
my_tuple= (1,2,3,4,5,6)
-Index():
index= my_tuple.index(2)
print(index)                    #this prints the position or first occurrence of 2 which is 3
-Count():
count= my_tuple(3)
print(count)                   #this prints out the number of times or occurrence of the number 3 which is 1

#DICTIONARIES
my_dict= {'name":'Raahat','age": 26,'city':'Accra'}
-Methods in Dictionaries
-Get():
age=my_dict.get('age')
print(age)                   #this prints out the value of the key 'age' which is 26
-Items():
items=my_dict.items()
print(items)             #this prints the view oject of the key-pair values
dict_items[('name','Raahat'),('age', 26),('city','Accra')]
-Keys():
keys=my_dict.keys()
print(keys)               #this prints out the view object containing keys
dict_keys(['name','age','city'])
-Values():
values=my_dict.values()
print(values)            #this prints out view object containing values
dict_values(['Raahat',26,'Accra'])
-Update():
my_dict.update({'gender':['Female'})
print(my_dict)              #this adds the key-value pair of 'gender':'Female' to my_dict
{'name':'Raahat','age':26,'city':'Accra','gender':'Female'}
-DICTIONARY WITH MUTIPLE VALUES
my_dict= dict([('name',['Rebecca','Raahat','Rita']),('age',[23,34,46]),('city',['Seychelles','Seoul','Bern']])
print(my_dict)
{'name':['Rebecca',Raahat','Rita'],'age':[23,34,46],'city':['Seychelles','Seoul','Bern']}

Screenshots of Results







