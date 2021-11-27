
# Principle Components Analysis in R- PCA 主成分分析
#### Lei ZHANG


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
Dataset 1: USArrests data set, which is part of the base R package 
1. **View Data**
```diff
# the rows of the dataset
states = row.names(USArrests)
states. 
# the columns of the dataset
name(USArrests) 
# view data
fix(USArrests)
 ```
 Here is the result after run it in R studio
 ![alt text](https://github.com/leizhangg/Data-Analysis-with-R/blob/main/Principle%20Components%20Regression/img/result%20of%20view%20data.png)
 ![alt text](https://github.com/leizhangg/Data-Analysis-with-R/blob/main/Principle%20Components%20Regression/img/preview%20of%20USArrest.png)
 
 The dataset contains 50 rows (states) and 4 columns ("Murder", "Assault", "UrbanPop", "Rape"). Here UrbanPop variable measures the percentage of the population in each state living in an urban area, which is not a comparable number to the number of rapes in each state per 100,000 individuals

```diff
# use apply()function to calculate the mean,variance and sd of row(use 1), column (use 2), here we calculate columns
apply(USArrests, 2, mean)
apply(USArrests, 2, var)
apply(USArrests, 2, sd)
```
2. Performing PCA
```diff
# prcomp()function and returns the resukts as an object of class prcomp
# by default, the prcomp()function centers the variables to have mean zero 
# scale = TRUE means scale the variables to have standard deviation one.
pr.out = prcomp(USArrests, scale = TRUE)
names(pr.out)
summary(pr.out)
```
Output:
![alt text](https://github.com/leizhangg/Data-Analysis-with-R/blob/main/Principle%20Components%20Regression/img/preOut.png)




Reference:
- [PCA Well-explained Video](https://www.youtube.com/watch?v=FgakZw6K1QQ)
- [prcomp function](https://stat.ethz.ch/R-manual/R-devel/library/stats/html/prcomp.html)








  








