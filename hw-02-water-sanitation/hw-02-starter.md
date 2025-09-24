HW 02 - Water and Sanitation - Answer Key
================
Tasneem Arabi
09/24/25

## Load packages and data

``` r
library(tidyverse)
wat_san <- read_csv("data/water-and-sanitation.csv")
```

## Exercises

### Exercise 1

The dataset has r nrow(wat_san) observations (rows).

### Exercise 2

Each row represents a country–year record (an Entity in a given Year)
with the percentages of the population in that country/year at different
water and sanitation service levels.

### Exercise 3

Between 2000 and 2020, the distribution of no sanitation service shifts
left (toward lower percentages) and becomes more concentrated at lower
values—evidence that open defecation generally declined over time,
though some high-value outliers remain.

``` r
wat_san %>% 
  filter(Entity != "World", Year %in% c(2000, 2020)) %>% 
  ggplot(aes(x = sanitation_none)) +
  geom_histogram(binwidth = 5, boundary = 0, closed = "left") +
  facet_wrap(~ Year) +
  labs(x = "No sanitation (% of population)", y = "Count of countries",
       title = "Distribution of 'no sanitation' across countries in 2000 vs 2020")
```

    ## Warning: Removed 31 rows containing non-finite outside the scale range
    ## (`stat_bin()`).

![](hw-02-starter_files/figure-gfm/no-sanitation-years-1.png)<!-- -->

### Exercise 4

Insert your answer here…

### Exercise 5

Insert your answer here…

### Exercise 6

Insert your answer here…

### Exercise 7

Insert your answer here…

### Exercise 8

Insert your answer here…
