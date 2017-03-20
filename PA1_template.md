# Reproducible Research: Peer Assessment 1


## Loading and preprocessing the data

```r
# load the activity-data
activity <- read.csv("activity.csv")

# create new column date in data-format
activity$date2 <- as.Date(activity$date, format = "%Y-%m-%d")
```

## What is mean total number of steps taken per day?

```r
# create an aggregate data set of the sum of the steps per day
agg_day_activity <- aggregate(activity$steps, by=list(activity$date2), FUN=sum, na.rm=TRUE, na.action=NULL)

# create a histogram of the total number of steps per day
hist(agg_day_activity$x, main = "Histogram of total number of steps per day", xlab = "Steps per day")
```

![](PA1_template_files/figure-html/total_steps_per_day-1.png)<!-- -->


## What is the average daily activity pattern?



## Imputing missing values



## Are there differences in activity patterns between weekdays and weekends?
