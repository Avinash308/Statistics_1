# Statistics_1
Mean and standard deviation


#find the standard deviation of the following rents paid using numpy and pandas
import numpy as np
import pandas as pd
list=[1500,1700,900,850,1000,950]
std=np.std(np.array(list))
print(std)
df=pd.DataFrame(list)
df.describe()
#finding variance of the following set which represents the heights of trees

list2=[3,21,98,203,17,9]
print(np.var(np.array(list2)))
df1=pd.DataFrame(list2)
print(df1.var(ddof=0),"Variance using pandas dataframe")

#In a class on 100 students, 80 students passed in all subjects, 10 failed in one subject, 7 failed in two subjects and 3 failed in three subjects. Find the probability distribution of the variable for number of subjects a student from the given class has failed in.
# solution starts Percentage and Probablity of the data Total Students = 100 => 100% 
# All Passed = 80 => 80% =>80/100 => 80% 0.8 
#Probability 1 Subject Failed = 10 => 10% 0.1 
#Probability 2 Subjects Failed = 7 => 7% 0.07 
#Probability 3 Subjects Failed = 3 => 3% 0.03 
import scipy.stats as stats 

df3=pd.DataFrame([0.8,0.1,0.07,0.03])
df3.describe()

#Find the probability distribution of the variable for number of subjects a student from the given class has failed in.
#for this we are using mean and standard deviation
m=25 #which is mean and standard deviation and multiplied by 100
sd=36.77

#cumilative density function
stats.norm(m,sd).cdf(80)

stats.norm(m,sd).pdf(80)
