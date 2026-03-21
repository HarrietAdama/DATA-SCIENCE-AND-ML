# LAB TITLE: PANDAS, DATA COMBINATION: JOINING & MERGING, HANDLING MISSING VALUES, IMPORTING A FILE FROM THE INTERNET IN GOOGLE COLAB, NUMPY, LINEAR ALGEBRA, STATISTICAL FUNCTIONS, DATA VISUALIZATION: MATPLOTLIB

# PANDAS(DATA COMBINATION: JOINING & MERGING): We continued with data combination as we left with joining and merging.

# MERGING:the merge function is used to combine two or more dataframes based on similar/common columns.
We call or use the word 'merge' anytime we are merging two or more dataframes. In merging we have the following functions:

df_5 = pd.DataFrame({'names':['Ama','Barry','Celestine','Dela'], 'Score':[1,2,3,4])

df_6 = pd.DataFrame({'names':['Barry','Dela','Emma','Frank'], 'Score':[5,6,7,8])

# 1. Inner Merge: The inner merge allows you to pick the items or elements in both dataframes that are similar. It will match the common items in both rows that are similar.

 # pd.merge(df_5, df_6, on='Names, how='inner')   # this merges dataframe5 and dataframe6 by matching common items in both dataframes. And the common items here is 'Dela' who has score of 4 in df_5 and a score of 6 in df_6 and Barry who has a score of 2 in df_5 and 5 in df_6.


# 2. Outer Merge: this allows you to perserve the rows and the elements within. We are maintaining  every element on the Names column. We use the first dataframe as a reference point.

# 3. Right merge: With this, we will preserve all the elements in the 2nd dataframe and merge with the similar items on both dataframes.

# 4. Merging two dataframes having different columns: we merge both dataframes when not all elements within the dataframes are similar so with this:

df_7 = pd.DataFrame({'Name1':['Ama','Barry','Celestine','Dela'], 'Score':[1,2,3,4]})

df_8 = pd.DataFrame({'Name2':['Barry','Dela','Emma','Frank'],'Score':[5,6,7,8]})

 you call:

 merged_df = pd.merge(df_7,df_8, left_on 'Name1',right_on='Name2', how='inner', suffixes=('df_7','df_8')

 
# JOIN-DATA COMBINATION: The join() function is used to combine two dataframes on their indexes.

df_9 = pd.DataFrame({'value1':[1,2,3,4], 'index':['A','B','C','D']})

df_10 = pd.DataFrame({'value2':[5,6,7,8], 'index':['B','D','E','F']})

# So to join the two dataframes we will consider the index. That is, the index that is common.

joined= df_9.join(df_10, how='left', lsuffix='_left', rsuffix='_right')
joined

# we are going to do a join but this time around we want to join df_9 and df_10. How do we want to join. we join it on the left and we want our suffix, which is the lsuffix. That is , the suffix for overlapping columns in df_9.

left(rsuffix): Is that we are going to look at the other components of those 

Right(rsuffix):


# Filtering: You can filter data based on conditions. We are making a decision on what to keep and what not to keep.
# We can filter by Age or by Name
x= {'Name':['Harriet','Rashid','Ololade'],'Age':[30,25,35, 'City':['New York','Paris','London']}

df = pd.DataFrame(x)
df
# we want to filter by age> 30 from this dataframe we do this:
filteres_df= df[df['Age']>30]
print(filtered_df) to get your output

# ADDING AND REMOVING COLUMNS

# adding columns

-To add a new column you need to state the column.

- df is the dataframe from above which we want to add a new column.

- df['Gender']=['Male','Female','Male']
  print(df)

- to remove a column from the initial dataframe, you follow this:
- we use :

- df.drop  # you state the column to remove like this:

df.drop('city', axis=1, inplace=True)

.drop means you want to drop a column from your initial dataframe

N.B: Whenever we are working with a Dataframe a axis= 0 means we are dealing with a row and axis=1 means we are dealing with a column.

# GROUPING AND AGGREGATION
We can group data based on one or more columns and perform aggregation functions.
-with aggregation we talk about: mean, maximum, minimum, mode etc.
# Grouping by age column

grouped_df = df.groupby('Age').mean()

- so just grouping it by age without .mean() only groups it by age but by adding the .mean() we are asking  it to group by age and also to find the mean age and print it.

- # HANDLING MISSING VALUES: Pandas can help us find missing values by either dropping them or filling them.

- Dropping missing values
- Filling missing values

- We use the .dropna() or the .fillna() functions

- # NUMPY: This is a general purpose array processing package in python. Numpy deals with numbers. It arranges numbers in a form of an array.

- An array is a data structure that is used to store multiple values in a single variable.

- We have to impory numpy as np to be able to use it.

- # We have a 1- dimensional array and a 2-dimensional array

- arr1d= np.array([1,2,3,4,5])

- arr2d = np.array([1,2,3],[4,5,6])

- Zeros array: it is an array that comprises only of zeros.

zeros_arr = np.zeros(3,4)
this produces a zeros array with 3 rows and 4 columns.

# ARRAY ATTRIBUTE
# .shape()
shape= arr2d.shape()          # this helps you to determine the number of rows and coulmns in an array.

# .size()
size = arr2d.size()            # this tells us the number of elements in an array.

# Data type: 
data_type= arr2d.dtype()    # tells you the what data type your array is.

# ARRAY OPERATIONS

We can add two, subtract and multiply two arrays.
# ADDITION: with the addition operations whatever number is added to the array is added to the individual elements in the array.
# For example:
2 + arr2d

2 + [1 2 3 
     4 5 6] 
     =[3 4 5
       6 7 8]

# SUBTRACTION: We do the same as the addition of an array.

arr2d-3
[1 2 3
4 5 6]   -3 = [-2 -1 0
               1  2  3]


# Multiplication
4 * arr2d = [4 8 12
             16 20 24] 

# AGRREGATE FUNCTIONS
# SUM: This means to add each and element in the array

total_sum = arr2d.sum
total_sum = 21

# MAXIMUM: We find the maximum value in the arrray.
max_val = arr2d.max()
max_val      # 6

# MINIMUM: We find the lowest or minimum value in the array.
min_val = arr2d.min()
min_val    # 1

# INDEXING: With indexing we take critical observation of the number of rows and columns.. We slice the columns to get what we want and also slice the rows to get want we want.

arr2d = [1 2 3   index0
         4 5 6]   index1

# Second Row
# We use the slicing method to obtain a particular row or column from an array.
# second_row = arr2d[1:,:]
# With this, start from the second row and end at any row available to us and with arr2d there is no other row aside the 1st and 2nd row so our output is [4 5 6]

# First Row
# first_row = arr2d[0:,1:]
# Start at the row with index 0 but stop before row1. This means row 1 is not inclusive. So the output will be [ 1 2 3]

# Second Row Element
# second_row_element = arr2d[1:,1:]
# output   [5,6]

# First Row Element
# first_row_element = arr2d[0:1,0:2]
# output    [1 2]


# FIRST ROW
# first_row = arr2d[0:1.1:]
# output   [2 3]


# ARRAY MANIPULATION: This invloves reshaping pr manipulating the array. That is, change how the rows and columns look like.
# We can use the function .reshape() to change how the columns and rows looks like.

    arr2d = [1 2 3
             4 5 6]

 # We want to reshape arr2d from having 2 rows and 3 columns to having 3 rows and 2 columns:
 reshaped_arr = arr2d.reshape(3,2)
 reshaped_arr    # output  [1 4
                            2 5] 
                            3 6]

# Concatenate Arrays

arr1d = [1 2 3]
in Pandas we use pd.concat but in arrays we use numpy. That is, np.concat

- This joins or merges two or more dataset together. So we add two one-dimensional arrays together

- We use the concat method to add arr1d + arr1d

- concat_arr = np.concat([arr1d, arr1d]
  # output   [1 2 3 1 2 3]

# Another Approach : We can create a new array and add it to arr1d

arr1d =([1 2 3])
arr3d =([4 5 6])

# So to join arr1d to arr3d we follow this:
# first we call the new and old array

arr1d = np.array([1 2 3])

arr 3d = np.array([4 5 6])
# to add both arrays:

concat_arr = np.concat([arr1d, np.array([4 5 6])])
concat_arr    # output  ([1 2 3 4 5 6])

# We use the .append() method to add a new entity to the array.

# we can append an array to an already existing array
arr4d = np.array([1 2 3],[4 5 6])
append_arr = np.append(arr4d, [7,8,9,10])
append_arr   # Output  ([1 2 3 4 5 6 7 8 9 10])

# BROADCASTING:Broadcasting allows operations between arrays of different shape without explicitly reshaping it.

a = np.array([1 2 3 4])
b = 4
print(a + b)       # output  ([5 6 7 8])

# RANDOM NUMBER GENERATION: In python numpy allows us to generate random nubers that we can work with. We generate random numbers by:

# random_numbers = np.random.rand(3,3)
random_numbers
 - np.random is used to generate random numbers but.rand means that we want to genrate random numbers from a uniform distribution
between 0 and 1.

# .CHOICE(): This receives only two arguements. the array and the size

items = np.array(['A','B','C','D'])

random_numbers2 = np.random.choice(items,size=(3,2))

# LINEAR ALGEBRA: We perform addition, subtraction and multiplication operations.

# create a matrix A and B
A = np.array([[1, 2],[3, 4]])
b= np.array([[5, 6],[7, 8]])

# ADDITION
A + B = [1 2         [5 6   =     [6 8
         3 4]     +   7 8]        10 12]

# SUBTRACTION
B-A = [4 4
       4 4]


# MULTIPLICATION : We multiply each element with each other bassed on their positions to each other. So then, to perform a multiplication operation, use the symbol @
A @ B= [19 22
       43  50]

 # WE CAN ALSO USE THE .dot() method to multiply two matrices.

 # TRANSPOSE OF A MATRIX
 A =[1 2
     3 4]
 Transpose_A = np.transpose(A)
 # OUTPUT  [1 3
            2 4]

 # INVERSE OF A MATRIX
 A*-1= A_inv= np.linalg,inv(A)
 print(A_inv)   # output   [-2 1.0
                            1.5 -0.5]


# IDENTITY MATRIX: To find the identity matrix we use this function:
identity_matrix = np.eye(3)
identity_matrix    # output  [1 0 0
                              0 1 0]
                              0 0 1]

# DETERMINANT OF A MATRIX                              
                              
 


         


























