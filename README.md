# capstone_data_analysis
Capstone Data Analysis

# Context
There are a lot of improvements made by Youtube channel until now. It is one of the most used Social Media Website and Apps all the time around the world. Currently the user traffic in Youtube is also rises from the past years until now and people start seeing business opportunities in Youtube.
So, We are the youtube ads consultant which provides analysis and recommendation for the people or company that want to sell their products using Youtube and engage more audiences in Youtube.

# Business Question?
* How can we optimize our YouTube advertising strategy? We can use Youtube datasets to understand which ads perform best and make informed decisions about targeting, placement, and budget allocation for the company who wants to sell their product in youtube.

# Data
## Data Insights -
* There are 16 columns available with 40949 datasets of trending video in youtube.
* There are 570 missing values in description column.
* We can drop the thumbnail_link because the value is only a link to the thumbnail of the video. We think it will be irrelevant with our analysis.
* Trending date and publish time can be converted into more proper date and time format so we can extract the date and time information.
* Category ID is still in number. We can extract the category name from the US_category_id.json file using video_id and category Id.

## Key Observations -
* The mean values of 4 numerical columns (views, likes, dislikes and comment_count) are not close enough to the median, meaning these 4 columns are not normally distributed.
* There is notably large differences between the Q3 and max values of numerical columns. It happens because the dataset is about the trending youtube videos, so mostly it contains high amount of views or likes.
* Thus observation 1 and 2 suggests that there are outlier in our datasets but the outlier is still makes sense. 
* There are many '[none]' values in tags column, meaning the video does not have any tags. We will not assume it as missing values as we still able to categorize it.

## Filling Missing Value
Let's see if we can fill the description missing value. We can use Youtube API to get description from Youtube website. For the '[none]' values in tags column, we can keep it for later because when the value of tags is '[none]', we can assume the total tags of the '[none]' row is 0.

# Analysis
## 1. **What category has the most views?**
![cat_name to views](https://user-images.githubusercontent.com/120706039/226159121-c08bc30f-725b-410d-8da0-8411db49210e.png)
We can conclude that the Music and Entertainment category are the most significant category with the highest views than other videos category.  
What we can do:
* We can more focus on Entertainment and Music videos in placing our ads in youtube to get more engagement with public

## 2. **What category often get high dislikes?**
![proportion of dislikes](https://user-images.githubusercontent.com/120706039/226158914-8a129618-6065-454e-a3fe-5c85cebbaebf.png)
We like to analyze the proportion of dislikes just to make sure that the channel that we are working with is not associated with the disliked videos in society, because we don't want to associated with the negativity. It can damage our brand and sales value.  
By seeing the chart above, the highest proportion of dislikes category is News & Politics followed by Nonprofits & Activism in the 2nd rank.  
**Disclaimer:**  
* The datasets is only for trending youtube which is the youtube videos with the highest views and high likes amount each date. So it makes sense if the proportion of likes from the datasets are high.

## 3. Is the difference between time on getting trending will get different views? 
![views to published trending difference corr](https://user-images.githubusercontent.com/120706039/226158896-4f0cbd66-5098-40ea-b7ed-9b9c9149a7d4.png)
Although not significant, We can notice that the relation between pub_to_trend_dtdiff is negative, meaning that if the video is really quick to get trending on youtube i.e one day only, then the views will be much higher than the other which needs a longer time to get trending.

