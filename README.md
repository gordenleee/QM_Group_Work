# QM_Group_Work
In groups of 4, find a data set that is broadly related to cities research or spatial analysis. Considering methods from the course related to exploring, summarising, and visualising data, communicate the key features of this data set through a 10minute presentation.
## 数据清洁
### 1.1 选择行
- 选择 `IMD_BAND_ENG` 非空的行，确保所有行都包含关键的英格兰多维贫困指数数据。
### 1.2 选择列
- **独立变量**：`PROP_TYPE`, `PROP_AGE_BAND`, `FLOOR_AREA_BAND`, `COUNCIL_TAX_BAND`, `IMD_BAND_ENG`, `REGION`, `LI_FLAG`, `CWI_FLAG`, `PV_FLAG`, `MAIN_HEAT_FUEL`。
- **因变量**：`Gcons2019` 至 `Gcons2005` 以及 `Econs2019` 至 `Econs2005`。
### 1.3 异常值处理
- 对于数值列，使用 IQR 方法识别并处理异常值。异常值被定义为低于 Q1 - 1.5 * IQR 或高于 Q3 + 1.5 * IQR 的值，并将这些异常值替换为边界值。
### 1.4 数据类型转换
- `PROP_TYPE`, `COUNCIL_TAX_BAND`, `REGION`：从对象（字符串）类型转换为整数类型，这是通过独热编码实现的。
### 1.5 填充NaN和应用数据转换
- 使用 `Pipeline` 和 `ColumnTransformer` 对数值列进行中位数填充和标准化，对分类列进行众数填充和独热编码。
tip: 分类变量 (`PROP_TYPE`, `COUNCIL_TAX_BAND`, `REGION`) 是通过独热编码转换的，而不是直接转换为整数 (`int64`)。独热编码创建了额外的列来表示这些分类变量，每个唯一的类别值都对应一个新列。
## 2 Summary statistics of key fields
Independent variable: pie  
Dependent variable: box
## 3 Appropriate plots to communicate the distribution of key fields
Dependent variable: frequency distribution
## 4 Appropriate plots to illustrate the relationship between key fields
all dependent variable ~ all independent variable  
box or hist
![box](https://github.com/gordenleee/QM_Group_Work/blob/main/reference/1.png)
![hist](https://github.com/gordenleee/QM_Group_Work/blob/main/reference/2.png)
## 5 Simple analyses relating to the data
