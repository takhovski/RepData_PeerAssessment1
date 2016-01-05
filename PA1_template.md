# Reproducible Research: Peer Assessment 1
Shobeir K. S. Mazinani  
January 4, 2016  


## Loading and preprocessing the data

Packages `dplyr` and `lubridate` are loaded to make cleaning and processing data easier.
In loading the `dplyr` package I am using the `suppressMessages` command to avoid seeing the dependency and warnings for aesthetic reasons.
The assumption is the dataset 'activity' is inside a folder called activity in your working directory.

```r
suppressMessages(library("dplyr"))
library("lubridate")
data <- read.csv(file = "activity/activity.csv")
data <- tbl_df(data)
```
The `date` column of the data is transformed into the *time* class by using `lubridate` package.

```r
data$date <- ymd(as.character(data$date))
data
```

```
## Source: local data frame [17,568 x 3]
## 
##    steps       date interval
##    (int)     (time)    (int)
## 1     NA 2012-10-01        0
## 2     NA 2012-10-01        5
## 3     NA 2012-10-01       10
## 4     NA 2012-10-01       15
## 5     NA 2012-10-01       20
## 6     NA 2012-10-01       25
## 7     NA 2012-10-01       30
## 8     NA 2012-10-01       35
## 9     NA 2012-10-01       40
## 10    NA 2012-10-01       45
## ..   ...        ...      ...
```



## What is mean total number of steps taken per day?



## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
