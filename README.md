# QM_Group_Work
In groups of 4, find a data set that is broadly related to cities research or spatial analysis. Considering methods from the course related to exploring, summarising, and visualising data, communicate the key features of this data set through a 10minute presentation.
# 1 Data cleaning
## 1.1 choose rows
choose ENG data
## 1.2 choose columns
Independent variable: PROP_TYPE	PROP_AGE_BAND	FLOOR_AREA_BAND	COUNCIL_TAX_BAND	IMD_BAND_ENG REGION	LI_FLAG CWI_FLAG PV_FLAG MAIN_HEAT_FUEL  
Dependent variable: Gcons2019-Gcons2005 Econs2019-Econs2005
## 1.3 Filling up vacancy
Gcons和Econs都缺失：删除整行  
Gcons或Econs都缺失：填0  
Gcons和Econs有部分缺失：填该列的平均值
## 1.4 Changing data type
PROP_TYPE COUNCIL_TAX_BAND REGION: object -> int64
# 2 Summary statistics of key fields
Independent variable: pie
Dependent variable: box
# 3 Appropriate plots to communicate the distribution of key fields
Dependent variable: frequency distribution
# 4 Appropriate plots to illustrate the relationship between key fields
all dependent variable ~ all independent variable  
box or hist
![box](https://github.com/gordenleee/QM_Group_Work/blob/main/reference/1.png)
![hist](https://github.com/gordenleee/QM_Group_Work/blob/main/reference/2.png)
