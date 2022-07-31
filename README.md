# The-Titanic-Prediction
This is Machine Learning Prediction of the Titanic Dataset using Logistic Regression while the Exploratory Data Analysis is done with Power BI.

# THE CHALLENGE
The sinking of the Titanic is one of the most infamous shipwrecks in history.

On April 15, 1912, during her maiden voyage, the widely considered “unsinkable” RMS Titanic sank after colliding with an iceberg. Unfortunately, there weren’t enough lifeboats for everyone onboard, resulting in the death of 1502 out of 2224 passengers and crew.

While there was some element of luck involved in surviving, it seems some groups of people were more likely to survive than others.

In this challenge, I built a predictive model that answers the question: “what sorts of people were more likely to survive?” using passenger data (ie name, age, gender, socio-economic class, etc).

# DATA SOURCE
The data is gotten from the popular Titanic Competition on kaggle.com https://www.kaggle.com/competitions/titanic/data. The description of the data is also well explained on the page. here is a brief summary;

Variable Notes
pclass: A proxy for socio-economic status (SES)
1st = Upper
2nd = Middle
3rd = Lower

age: Age is fractional if less than 1. If the age is estimated, is it in the form of xx.5

sibsp: The dataset defines family relations in this way...
Sibling = brother, sister, stepbrother, stepsister
Spouse = husband, wife (mistresses and fiancés were ignored)

parch: The dataset defines family relations in this way...
Parent = mother, father
Child = daughter, son, stepdaughter, stepson
Some children travelled only with a nanny, therefore parch=0 for them.

# EXPLORATORY DATA ANALYSIS
Exploring a dataset is majorly used by Data Scienctist to undesrtand the data better before proceeding in the Data Cleaning Process. I therefore used Power BI Desktop to explore the data by building a visualization Report from the Dataset. Pushed it to PowerBI Service and and import it in the Jupyter Notebook. please note that only the training dataset was explored in this visual because most of the Preprocessing are majorly from the train dataset.
click to view the Report dashboard https://app.powerbi.com/view?r=eyJrIjoiZDE1MzQyMWQtZWU1ZS00NjM5LWI1MGItNWE2MDgwMGNhZDc3IiwidCI6IjMyNzk2YmUyLTYwZmItNGRhMi04ZDI2LTA2ZTU5MzhlNmU2YiIsImMiOjh9&pageName=ReportSection

a brief JPEG is thus 
![image](https://user-images.githubusercontent.com/60477717/182039610-2c09c77e-0686-4e91-a231-7ff0ad7fe6f4.png)

# PRERPOCESSING 
In Power BI, diffrent measures were created to prepare the data for better exploration and visualization

1. The Age was categorised as Infant, Toodler, Teenager, Youth, Adult and Old Age  
<img width="684" alt="NEW_AGE" src="https://user-images.githubusercontent.com/60477717/182038859-ef925b63-2452-4fff-83e0-99b484bacc13.PNG">

2. Some Ages were missing in the Age Column, there were therefore filled using the Passenger Class Column, details below;
<img width="683" alt="AGE_BASE_ON CLASS" src="https://user-images.githubusercontent.com/60477717/182039222-9a2b6a42-9148-4673-8ad7-73a135c780d9.PNG">

3. The Class is represented in numbers as 1,2,3 and are mapped to First Class, Second and Third Class repectively using an IF statement
<img width="690" alt="NEW_CLASS" src="https://user-images.githubusercontent.com/60477717/182039193-a7eb2746-b08b-44e9-9473-19ede109ddaa.PNG">

4. Convert Blank to Zero in the Gender Column 
<img width="713" alt="NEW_GENDER" src="https://user-images.githubusercontent.com/60477717/182039399-7dec6ac8-b914-4146-9e60-af6b5805e1cd.PNG">

5. Point of Embarked were represented with 'S', 'Q', 'U' and re-categorissed as Southampton, Queenstown and Cherbourg respectively
<img width="702" alt="POE" src="https://user-images.githubusercontent.com/60477717/182039525-cada68c2-fd74-477e-8713-1f00b8994a54.PNG">
 

# MODEL BUILDING
This is the process in building a Logistic Regression using the whole of the Titanic Dataset (the train and the test dataset).
Among other Classification models (K-Nearest Neighbor, Select Vector Machine, Random Forest, Decision Tree...) only Logistic Regression gave a better performance of model prediction when only the train dataset was used to predict, hence it was adopted in this model. 
This model used both train and test data to predict which passenger in the test data will survive or not. The model predicted 78% of the Passengers accurately and had 22% wrong prediction.

The data cleaning process is well explained in the Notebook and more preprocessing methods shall be adopted in earnest to increase the model prediction.

shall be explored to increase the model prediction as well.

You can direcly view the Jupyter Notebook with this link https://github.com/Abdur-RasheedAde/The-Titanic-Prediction/blob/main/PREDICTION_OF_SURVIVAL_OF_THE_TITATIC_DATA.ipynb

Your comment will be well appreciate to improve the Model performance. Thanks in advance
