# Analyzing E-commerce User Interactions to determine KPIs

## Usage
Prior to running the Jupyter notebook, please input the appropriate path for the data 

```python
interact_oct2019 = pd.read_csv('./data/interactions-2019-Oct.csv')
interact_nov2019 = pd.read_csv('./data/interactions-2019-Nov.csv')
interact_dec2019 = pd.read_csv('./data/interactions-2019-Dec.csv')
interact_jan2020 = pd.read_csv('./data/interactions-2020-Jan.csv')
interact_feb2020 = pd.read_csv('./data/interactions-2020-Feb.csv')
items = pd.read_csv('./data/items_catalog.csv')
```

## Important Decisions for Metrics

First Visit Date: Date of the first interaction in pandas datetime format

Last Visit Date: Date of the last interaction in pandas datetime format

Average Gap: Average gap between visits in days/time

Average Monthly Spend: Total spend over all months divided by duration in months from the user's first visit till the last date of data

Favorite Brand: 
The favorite brand for each user is determined in a hierarchical fashion. The following is the priority in which the brands are selected for each user:
1) Most frequently occuring brand with respect to purchase interactions
2) Most frequently occuring brand with respect to "Add to Cart" interactions
3) Most frequently occuring brand with respect to other types of interactions