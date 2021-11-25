
# Principle Components Analysis - PCA 主成分分析
## 1. What PCA does
- An approach for deriving a low-dimensional (reduce dimension) set of features from a large set of variables. 数据降维或特征降维
- It finds a sequence of linear combinations of the variables that have maximal variance, and are mutually uncorrelated.
- Some concepts:
  - **Mean Centering**: the subtraction of the variable averages from the data. It corresponds to moving the origin of the coordinate system to coincide with the average point. 中心化
  - the **First Principle Component, PC1**
  - the **Second Principle Component, PC2**
  - **Liner Combination**
  - **Singular Vector**
  - **Eigenvector**
  - **Loading Scores**
  - **Singular Value Decomposition**
  - **Scree Plot**
## 2. Why PCA
- When faced with a large set of correlated variables,principal components allow us to summarize this set with a smaller number of representative variables that
collectively explain most of the variability in the original set. 从冗余特征中提取主要成分，找出数据中的主要成分来代表数据
- a tool for `data visualization`; discover if there is an informative way to visualize the data. 数据可视化 
- `data pre-processing` before supervised techniques are applied. 数据预先处理

## 3. PCA With R
Dataset: USArrests data set, which is part of the base R package 
1. **View Data**
```diff
# the rows of the dataset
states = row.names(USArrests)
states. 
# the columns of the dataset
name(USArrests) 
fix(USArrests)
 ```
 Here is the result after run it in R studio
 
3. s
4. s





  








