[![GitHub issues](https://img.shields.io/github/issues/anekar/playground)](https://github.com/anekar/playground/issues)

# Languages
```R```
# Environment
```RStudio```

# Installation 

```R
setwd('C:/Users/Lazaros/R/playground')
.libPaths('C:/Users/Lazaros')
```

# Libraries
```R
library(readr)
library(tidyverse)
library(magrittr)
library(writexl)
```
# Problems Faced
<details>
<summary>Common Problems </summary>

* Renaming Variables
* Dealing with NA values
* Dropping Columns
* Deleting Rows
</details>

<details>
<summary>Other Problems</summary>
* Each product category belongs into a more generic product category

</details>

# Reading  Files
```R
Markets <- read_csv("WorkingData/markets_all.csv")
Categories <- read_csv("WorkingData/categories.csv")
bar <- read_csv("WorkingData/bar.csv")
```
# Visuals
![Rplot](https://user-images.githubusercontent.com/47696240/134349679-c1284e3c-40b0-4aaa-b679-bcf167b471e9.png)!
# Code Samples
```R 
ggplot(Total,aes(Main_Category,AB)) +
    geom_bar(stat = 'identity') +
    labs(x = 'Product Category',
         y = 'Frequency',
         title = 'Most Profitable Product Category',
         subtitle = 'Super-Market: AB')
```
```R
AB <- Total %>% 
  select(product_id, AB, Main_Category_Id, Main_Category, Category_Name) %>% 
  filter(Main_Category == 'Food')  %>% 
  group_by(AB) %>% 
  arrange(desc(AB))
```
```R
ggplot(AB, aes(Category_Name, AB)) +
  geom_bar(stat = 'identity') +
  labs(x = 'Category Name',
       y = 'Total Sum',
       title = 'Which is the most preferred category from Food',
       subtitle = 'Market: AB') +
  coord_flip()
```