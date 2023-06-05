# final-grades-prediction
As final grades of the students are very important for acedamic upgradation. Grades are the basic scale to set the bar for students academic goals. The performance of the students depend on different aspects like 'where he resides'; 'what is family background and family relations'; 'what is parental qualification'; 'what is study time, travel time, activites' etc. Here the grades from 2 different schools  'GP' - Gabriel Pereira and  'MS' - Mousinho da Silveira are collected. .In this scholar system grades are between 0 and 20 in follwing hierarchy:

grade                         Qualification

20-17.5                         Excellent

17.4-15.5                       V.Good

15.4-13.5                       Good

13.4-9.5                        Sufficient

9.4-3.5                         Weak

3.4-0                           Poor

The school year is divided in three parts and the grades are of G1, G2, G3. Final grades are in the form of G3.
  
 # Problem Statement
Performance of the student is reflection of the knowledge and grade is one of the crucial part of it. The purpose of this project is to the train some machine learning models in order to predict the final grade of the studnets attend in the following dataset and apply exploratory data analysis (EDA) in 'Final Grades of Students' with Pandas framework.
 
# Data Description
The data is featuring various 28 diiferent attributes which are contribute towards the grade of the students. Following are the features:
##### school: student's school
'GP' - Gabriel Pereira                                                       'MS' - Mousinho da Silveira
##### sex: student's sex
'F' - female                                                                 'M' - male
##### age: student's age
from 15 to 22
##### address: student's home address type
'U' - urban'                                                                 'R' - rural
##### famsize: family size
'LE3' - less or equal to 3                                                   'GT3' - greater than 3
##### Pstatus: parent's cohabitation status
'T' - living together                                                        'A' - apart
##### Medu: mother's education
##### Fedu: father's education 0 - none
1 - primary education (4th grade)                                             2 – 5th to 9th grade
3 – secondary education                                                       4 – higher education
###### Mjob: mother's job
###### Fjob: father's job
'teacher'                                                                     'health' care related
civil 'services' (e.g. administrative or police)                              'at_home' or 'other')
##### reason: reason to choose this school
close to 'home'                                                                school 'reputation'
'course' preference                                                            'other'
###### guardian: student's guardian
'mother'                                                                      'father' 
'other'
###### traveltime: home to school travel time
1 - <15 min.                                                                   2 - 15 to 30 min. 
3 - 30 min. to 1 hour                                                          4 - >1 hour
##### studytime: weekly study time
1 - <2 hours                                                                   2 - 2 to 5 hours 
3 - 5 to 10 hours                                                              4 - >10 hours
##### failures: number of past class failures
n if 1<=n<3, else 4
##### schoolsup: extra educational support
##### famsup: family educational support
##### paid: extra paid classes within the course subject 
##### activities: extra-curricular activities
##### nursery: attended nursery school
##### higher: wants to take higher education
##### internet: Internet access at home
##### romantic: with a romantic relationship
yes or no
##### famrel: quality of family relationships
from 1 - very bad to 5 - excellent
##### freetime: free time after school
##### goout: going out with friends
##### Dalc: workday alcohol consumption
##### Walc: weekend alcohol consumption
from 1 - very low to 5 - very high
##### health: current health status
from 1 - very bad to 5 - very good
##### absences: number of school absences
from 0 to 93
##### G1 - first period grade
from 0 to 20
##### G2 - second period grade
from 0 to 20)
##### G3 - final grade
from 0 to 20

# Machine Learning Models
K-Nearest Neighbors (KNN)

Decision Tree (DT)

Support Vector Regressor (SVR)

Random Forest (RF)

# Approch 
Data Preprocessing

Data Exploration

Model Prediction

# CONCLUSION
1. The best models to predict the final grade G3 are Support Vector Regressor (SVR) and Random Forest (RF), and the latter have a mean absolute error (MAE) around 2.29 and 2.26 respectively.

2. Both SVR and RF tend to predict the final grade around the mean value of the latter. Consequencially, both tend to underestimate the grades higher than the mean and to overestimate the grade lower than the mean.

3. By analysing the distribution of the errors made by both models it follows that SVR is 'more balanced', i.e. it has a better ratio between underestimated and overestimated grades, while RF performs better on the outliers. Thus, the choice between which model to use depends on the application needs.

4. According to the common sense and the provided EDA the most important features for the prediction of G3 should be 'studytime', 'higher', 'failures' and 'Walc'. However, the RF indicates 'absences', 'failures', 'mothers education','mothers job' and 'age' as the most important features. This is not surprising, since also the variables which we have not considered as the most important clearly show an influence of the final grade as showed in the EDA. Moreover, according to RF the 'absences' variable is by far the most important one.
