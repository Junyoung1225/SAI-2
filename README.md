# SAI-2
import pandas as pd
import matplotlib.pyplot as plt
import numpy as np
from matplotlib import dates
import seaborn as sns 
df = pd.read_csv('Global YouTube Statistics.csv', encoding='cp949')
df.columns
sample = df[['subscribers', 'video views',
       'uploads',
       'video_views_rank', 'country_rank', 'channel_type_rank',
       'video_views_for_the_last_30_days', 'lowest_monthly_earnings',
       'highest_monthly_earnings', 'lowest_yearly_earnings',
       'highest_yearly_earnings', 'subscribers_for_last_30_days',
       'created_year', 'created_date',
       'Gross tertiary education enrollment (%)', 'Population',
       'Unemployment rate', 'Urban_population', 'Latitude', 'Longitude']]

plt.figure(figsize=(15,15))
sns.heatmap(data = sample.corr(), annot=True, 
fmt = '.2f', linewidths=.5, cmap='Blues')
