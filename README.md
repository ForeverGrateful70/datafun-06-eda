# datafun-06-EDA

### Project 06 is an opportunity to create your own custom exploratory data analysis (EDA) project using GitHub, Git, Jupyter, pandas, Seaborn and other popular data analytics tools.

## Initiate project 06 repository in GitHub
## Clone GitHub repository to local machine
'''
git clone https://github.com/ForeverGrateful70/datafun-06-eda.git
'''

## Create a README, .gitignore and requirements.txt files

# Import Dependencies
'''
import matplotlib.pyplot as plt
import pandas as pd
import seaborn as sns
'''

## Link to Data File Location
[mpg.csv] (https://github.com/mwaskom/seaborn-data/blob/master/mpg.csv)

## Install Dependencies and Freeze Requirements
'''
python3 -m pip install jupyterlab, pandas, pyarrow, matplotlib, seaborn
python3 -m pip freeze > requirements.txt
'''

## Data Set Load
'''
df = sns.load_dataset('mpg')
'''

## Git Commands
'''
git add .
git commit -m ""
git push origin main
'''

## Rename Columns
'''
df.rename(columns={'mpg': 'MPG'}, inplace=True)
df.rename(columns={'cylinders': 'Cylinders'}, inplace=True)
df.rename(columns={'displacement': 'Displacement'}, inplace=True)
df.rename(columns={'horsepower': 'Horsepower'}, inplace=True)
df.rename(columns={'weight': 'Weight (lbs)'}, inplace=True)
df.rename(columns={'acceleration': 'Acceleration'}, inplace=True)
df.rename(columns={'model_year': 'Model Year'}, inplace=True)
df.rename(columns={'origin': 'Origin'}, inplace=True)
df.rename(columns={'make': 'Make'}, inplace=True)
'''

## Initial View of Dataframe
'''
print(df.head())
print(df.head(10))
print(df.shape)
print(df.dtypes)
print(df.describe())
'''

## Histogram
'''
df['MPG'].hist()
plt.title(f'Distribution of MPG')
plt.show()


df['Cylinders'].hist()
plt.title(f'Number of Cylinders')
plt.show()
'''

## Record Observatoions
'''Miles Per Gallon: Initially the MPG seemed to be very low for these vehicles but we have to keep in mind that the range of manufacture years is 1970 - 1976. With the oil crisis hitting in United State (US) in 1973 it would take some time for auto manufacturers to engineer more efficient engines and for US consumers to adopt these changes to their vehicles.

Number of Cylinders: The number of cylinders is pretty standard of what you would see today in the United States.  It is worth noting that a few auto manufacturers did make three and five cylinder vechiles.  You can still find five cylinder vehicles being manufactured in the US.'''

## Origin of Vehicles Count plot
'''
df['Origin'].value_counts()

# Inspect value counts for Origin column
sns.countplot(x='Origin', data=df)
plt.title(f'Countries/Regions of Origin')
plt.show()
'''

## Record Observations
'''Again keeping in mind that the manufacture years of the vehciles in this dataset is 1970 - 1976 the high number of vehicles manufactured in the USA makes sense.  After the oil crisis in 1973 Americans would buy more imported vehciles due to there engines being more gas efficient.  If we collected data from the present day I would suspect the number of vehicles originating from countries other the the USA would be much higher.'''

## Which Countries Vehicles have the most horespower bar plot and scatter plot
'''
sns.barplot(x='Origin', y='Horsepower', data=df)

sns.scatterplot(x='Origin', y='Horsepower', hue='Cylinders', data=df)

plt.show
'''

## Record Observations
'''As we can see from the bar graph and scatter plot above the USA manufactures more eight cylinder vehicles then both Japan and Europe. Therefore vehicles manufactured in the USA gererally have higher horsepower then those made in Japan and/or Europe for the years 1970 - 1976.'''

# Conclustion
'''By looking at the data we have for the miles per gallon of vehicles manufactured between 1970 and 1976 we can see that the majority were made in the USA, had eight cylinders and were not very gas efficient. The high amount of horsepower produced by American made vehicles likely contributed to there low miles per gallon scores.'''