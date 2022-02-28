# Ford GoBike System Data
## by Fatma ElBoshy


## Dataset

> This data set includes information about individual rides made in a bike-sharing system covering the greater San Francisco Bay area.

>My dataset is 183412 rows and 17 column, after cleaning it became 174952 rows and 14 column

> The main features I'm interested in are 'distatnce' as our dependent variable. I will extract it from the start coorinates and end coordinates.

> 'user_type', 'member_birth_year', 'member_gender' as well as 'duration_sec' as our independent variables.

> The only wrangling steps I took to clean the date were:
1. dropping unnecessary columns like 'start_station_id' and 'end_station_id'
2. removing all rows that contain null values
3. engineering new features like 'distance', 'duration_hr', 'duration_min' and 'age'

## Summary of Findings

> My variable of interest is 'distance', there were a lot of unusal points since the distance crossed at 75% is 2.2 km, while the max distances crossed is 69.5 km, I didn't need to perform any transformations on the variable itself but I had to use 'plt.xlim' to exclude outliers.

> As for the 'duration_sec' feature, I had to transform it into minutes or hours to be more comprehensible, as for the distribution of minutes, it was similar to the distribution of distance with avrage 13.15 minute at 75% and maximum duration of 23.5 hours.

> As for the 'age' distribution, it was pretty normally distributed with some outliers, we can conclude that the avrage age of bikers is from 25 to 45 years old. The more the age increases, the less people tend to ride bikes.

> From the distribution of 'gender' we can see that 74.6% of bikers are males, while only 2.1% are categorized as 'others' with the rest being females.

> As for the user, it's apparent that most of the bikers are 'subscribers' with percentage of 90.5%

> The avrage trip takes about 11.73 minute.

### How did the 'distance' vary with other features in the dataset?¶
> 'distance' our feature of interest varies with age in a way that makes it clear the more the 'age' increases, the less distance one crosses. But most people who ride bikes are between 25 to 40 years old and usually cross a distance between 1 to 1.5 km.

> Also we can conclude that a distance of 1.5 km usually takes under 10 minutes with a bike.

> As for 'member_gender', all the three genders tend to cross the same distance on avrage, but crossing a distance of 1 km seems to be a trend among 'males' while 'females' tend to cross a distance of a little more than just 1 km.

### Relationships between the other features:
> Between 'user_type' and 'member_gender' it's apparent that subscribers make up the majority of Males, Females and other.

> Also, at older ages (+40): between age 50 and 60, 'others' gender tend to ride bikes more than either males or females. But between 45 and 50, 'males' tend to ride bikes more.

> However, at younger ages (20 to 40): 'others' gender tend to ride bikes the most, 'males' come in second then 'females' come last.

> As for 'user_type', subscribers' age vary from 25 to 40 years old while 'customers' age tends to range around 30s.

> Customers tend to ride bikes for longer periods (around 40 minutes max) than Subscribers ( around ~23 minutes max).

### What effect did the gender type, the user type and the duration have on the 'distance'?

> Looking at the duration vs distance heatmap for each gender, we observe that: 
1. both males and other tend to cross less than 5 km in about 150 minutes (~2.5 hours)
2. however, in the same period of time, females tend to cross about 6 km.

> Looking at the user type vs distance violinplot for each gender, we conclude:
1. Male subscribers tend to go on longer distances than male customers.
2. But the female customers tend to go on longer distances than female subscribers. 

### Surprisingly!

> Majority male customers tend to go on trips that lasts for less than 25 minutes, while majority of male subscribers can last for as long as 50 minutes.

> While for females, it's the complete opposite, since majority of female subscribers go on trips less than 25 minutes while female customers go for trips that can last for about 50 minute!

## Key Insights for Presentation

> So majority of bikers are 'males' with percentage of 74.5%, most of them are actually subscribers not customers, males also tend to cross a distance of 1 km while females tend to go a little further.
