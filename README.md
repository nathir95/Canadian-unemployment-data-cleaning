# Canadian-unemployment-data-cleaning
Unemployment data cleaning

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import matplotlib.pyplot as plt
import matplotlib.gridspec as gridspec
import matplotlib.animation as animation


df= pd.read_csv(r'C:\\Users\\nhaim\\Downloads\\unemployment data.csv')

df1=  df[df['AgeGroup']== '15 years and over']

df1= df1[df1['Sex']== 'Both sexes']



df11= df1.drop(columns=['Quebec', 'Ontario', 'Sex', 'AgeGroup'])



df11.rename(columns = {"When":"Month"},inplace=True)


print(df11)


