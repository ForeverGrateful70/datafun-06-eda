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
python3 -m pip install jupyterlab pandas pyarrow matplotlib seaborn
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
