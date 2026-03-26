# LAB TITLE: EXPLORATORY DATA ANALYSIS(EDA), STEPS FOR EDA ON A MESSY DATASET: LOADING THE DATA, INITIAL DATA INSPECTION, SUMMARY STATISTICS, MISSING VALUES ANALYSIS, DATA CLEANING, DATA VISUALIZATION.

# First and foremost, I loaded all the python libraries that will be needed in working with this dataset.

# I loaded the dataset which was is the titanic dataset from a url(Uniform Resource Locator) and I assigned the variable titanic = pd.read_csv(url) and it loaded the dataset to my code. Then I used the .head() to load the first five(5) rows of the dataset.

# I conducted a initial data inspection. I inspected the basic structure and summary of the dataset by using the function .info(). This function will help us find missing values and anything wrong with the dataset.

# Using, the .describe(include='all') function, I was able to display the summary statistics of the dataset. With the summary statistics, we have: the mode, median(50th percentile), mean, frequency, standard deviation, 25th percentile, 75th percentile, minimum, maximum etc.

# I then, divided the summary statistics into categorical and numerical statistics, where I assigned a varaiable categorical_summary for the categorical features of the titanic dataset. I showed the count, unique, top and frequency properities of the these features.

# I did the same for the numerical summary statistics for thenumerical features of the titanic dataset. I assigned numerical_summaery for the numerical summary statistics.

# Moving to handling the missing values in the dataset. I used the isnull().sum() to find the missing values in the dataset. and I also used the a heatmap to visually display the features of the dataset with missing values. From using the function .isnull().sum() function we can see that the feature 'Age', 'Cabin', and 'Embarked' have values that are missing. The rest of the features do not have any values missing.

# After knowing which features have values missing I try to clean the data by either filling the missing values or dropping the missing values by using the .fillna() or .dropna() functions. With, filling for missing values, I either fill with the median, mean or the mode. The mean and median is used for filling both numerical features of the titanic dataset and the mode is used to fill the categorical features of the dataset.

# I see that we have three(3) features in the titanic dataset that have missing values which are: 'Age', 'Cabin' and 'Embarked'. From what can be seen the numnber of missing values in the 'Cabin' feature is too much and, cannot be filled, hence, we drop it by using the .dropna() function.

# I use the .fillna() function to fill the medaian age for the values missing in the 'Age' features of the dataset. And I use the mode to fill in the missing values for 'Embarked'. I verify again using the .isnull().sum() to see if there are still any missing values and when I see that there are not, I proceed to the next step.

# I begin with displaying the data visually in other to show relationships between or among the features of the dataset.

# I start with the Count plot for survival of the passengers in the titanic. By using seaborn visualization python library I show a count plot of survival. This plot shows the number of people who survived or did not survive. Zero(0) represents those who did not survive and one(1) represents those who survived. And from the diagram we can see that more people died than they survived.

# The next diagram is a bar plot to show the passenger class. This does not show a relationship between features of the dataset but it shows the count of the number of passengers in each class that the titanic ship provided for the passengers. We can see that most of the passengers belonged to the class 3 which is the economy class for the poor and the second populated class is the first class  which is the first class, believed to be for the rich and privilege an the less populated class is class 2 which is almost same as the first class.

# Age Distribution histogram diagram is the used to display how the age is distributed  in the dataset. The kernel density line is showed and it helps determine where the age is populated more. It shows where the distribution is normally distributed, skewed to the left or to the right. We can see the age of the passenger is age 20 to age 40 to more of the age been concentrated age 20 to 30.

# We look at the Survival Rate by Passenger Class. From this diagram we can see the relationship between passenger class and the survival rate. And from this we can see that more of the passengers who belonged to the first class survived and the passengers who did not survrive belonged to the third class(class 3).

# Survival Rate by Sex. I use a counrplot to display the relatonship between survival rate and by sex. And from the diagram we can see that the females survived more than the males.

# I create separate countplots for both the males and females to see the number of females who survived and the number who did not survived and I did same for the males as well. By using subplots I was able to create separate plots side by side of the male andfemale survival rates respectively. From the male survival rate, more males died than they survived and also from the females countplot, more females survived than they died.

# Survival Rate by Passenger Class. I created countplots using the subplots function to create separate plots of the number of people who died and who did not by the passenger class. So, we had three classes and three separate countplot for each class. We can see that from the first diagram which is for the class1 more people survived than they died, also, from the second diagram, which is for class2 we can see that the difference between the number of people who survived and the number of people who died is not so much, and from the the third diagram which is for class3, we can saw that the number of people who survived was very low as compared to the people who died.

# I created a boxplot for age passenger class. This diagram shows the ages of the passengers in the three different class. It shows the relationship between the ages of the passengers in the three classes. We can see that in class1, the ages of the passengers is between 1 and 70 years with an outlier in the eighties. In class2 from the second diagram we can see that, the passenger ages ranges between, 2 years to 55 years old with somes outliers above 55 years to 70 years. Lastly, we cans see from the third class which is for class3, the passengers age ranges from 5 years to 45 years whith lots of outliers below 5 years and some above 45 years 75 years old.

# Boxplot for fare by passenger class, from the first class we can see that passengers in the first class paid a lot of money for that class with some few outliers which shows that some passengers paid above the range of the fare prices for class1. From the second diagram, we can see that the fare prices ranges between 0 to 2 that is lower than the first class and from the third diagram, we can see that the fare price is lower than that of the second and first class which shows that the passengers in the third class did not pay for much for that class.

# Age distribution by survival. This diagram shows the age distributrion by survival. From the first diagram which shows the number of people who did not survive, we can see that the age ranges from 5 years to 52 years with outliers below 5 years and some above 52 years. From the second diagram, which is for for people who survive, we can see that the age ranges from1 years to 55 years with some few outliers outside the range.

# Boxplot for fare by survival. This diagram shows the diagram between the fare  prices and the number of people that survived and those who did not survive. From the first boxplot we can see that the number of people who died they do not pay much for the fare and the second plot shows that those who survived paid more than those who died for the fare.

# The last diagram shows a heatmap which shows the correlation between the features of the titanic dataset. From the diagram we cans see that when a feature correlates with itself the correlation coeffeicient is 1 but when you correlate a feature with another feature is gives you a below 1 and it can either be a positive or negative number.




# 
