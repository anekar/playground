[![GitHub issues](https://img.shields.io/github/issues/anekar/playground)](https://github.com/anekar/playground/issues)

# Project Infromation 

Fundamental purpose of this project is to analyze the data from big retail grocery chains in order to extract patterns and key insights.
Visuals from this project will be provided from RSutdio with library ggplot2 and Tableau Public. Furthermore,  the project comes
with an extra excel file which is exported from tidy data  after analyzing them. 


# Languages
```R```
# Environment
```RStudio```

# Installation 

```R
setwd('C"/YourPathGoesHere/')
.libPaths('C:/Users/')
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
``` Visuals created via ```
* RStudio and 
* Tableau

![What Consumers buy the most from each Market](https://user-images.githubusercontent.com/47696240/134463586-9c2beb9f-fd15-484b-aae5-b3dd82c28fca.png)

![Sheet 3](https://user-images.githubusercontent.com/47696240/134463641-d9e51019-1abc-4ce1-941f-cfb11f0f1b63.png)

# Code Samples
```R
ggplot(AB, aes(Category_Name, AB)) +
  geom_bar(stat = 'identity') +
  labs(x = 'Category Name',
       y = 'Total Sum',
       title = 'Which is the most preferred category from Food',
       subtitle = 'Market: AB') +
  coord_flip()
```
![Rplot](https://user-images.githubusercontent.com/47696240/134349679-c1284e3c-40b0-4aaa-b679-bcf167b471e9.png)!
