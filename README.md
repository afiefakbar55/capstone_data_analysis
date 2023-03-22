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

We can conclude that the Music and Entertainment category are the most significant category with the highest views than other videos category.  
What we can do:
* We can more focus on Entertainment and Music videos in placing our ads in youtube to get more engagement with public

## 2. **What category often get high dislikes?**

We like to analyze the proportion of dislikes just to make sure that the channel that we are working with is not associated with the disliked videos in society, because we don't want to associated with the negativity. It can damage our brand and sales value.  
By seeing the chart above, the highest proportion of dislikes category is News & Politics followed by Nonprofits & Activism in the 2nd rank.  
**Disclaimer:**  
* The datasets is only for trending youtube which is the youtube videos with the highest views and high likes amount each date. So it makes sense if the proportion of likes from the datasets are high.

## 3. Is the difference between time on getting trending will get different views? 

Although not significant, We can notice that the relation between pub_to_trend_dtdiff is negative, meaning that if the video is really quick to get trending on youtube i.e one day only, then the views will be much higher than the other which needs a longer time to get trending.

## 4. Which publishing day has the most trending videos?

What we know from the graphic is that the trending channel which publish videos on Friday and Sunday have more views than the other days.
We also will know from the charts above that the trending channel get more views when they publish the video at 4 AM and around 7-10 AM.

## 5. What are the words of tags that often get trending?

In the image in notebook, we can see the most common tags used in trending videos which is the large words in the image such as star wars, music video, super bowl, charlie puth, will smith and etc.

## 6. What words in description which can get more views?

As you can see from images, the large words are mostly in link format such as google, youtube, bitly, facebook and etc. Perhaps most of the trending videos have link in the description.

## 7. What is the proportion of views when the comment or the rating is disabled and when the video is error or removed? 

Most of trending videos allows their comments section, ratings section and the video is not error or removed.

# Conclusions

From analysis that we made, we can take the key **conclusions**: 

* The trending category with the most trending videos is Music and followed by Entertainment in the 2nd rank. This can happen as people tend to watch Youtube Music videos many times. Even people like to loop the videos just to hear the music in Youtube.
* By seeing the chart above, the highest proportion of dislikes category is News & Politics followed by Nonprofits & Activism in the 2nd rank.
* There are videos that can get trending in youtube in just one day after the video is published and there are 10 categories which have videos with the shortest time to get trending in youtube. The top are Entertainment with 36 videos get trending only in a day.
* There are also 10 Channels above are the channel which have videos with the shortest time to get trending in youtube. The top are Saturday Night Live and The Voice for 5 videos get trending only in a day.
* We notice from the analysis above that videos which are published on friday and sunday have more views than published in other days
* We know from the charts above that the trending channel can get more views when they publish the video at 4 AM and around 7-10 AM.
* We can see the most common tags used in trending videos which is the large words in the image such as star wars, music video, super bowl, charlie puth, will smith and etc.
* We also noticed that the trending videos mostly use some links in their description whether it is instagram link, google link, bitly and etc.
* Lastly, we knew that most of the trending videos allow the comment and the rating sections, and the video is not error or removed.

From the conclusions above we can take recommend some points:

* It is better for the company to work with entertainment and music channel as the ambassador of the product or cooperate in selling our products
* It is better for the company to stay away from News, Politic, Nonprofits or Activism channel to protect the brand and value
* We can more focus on cooperate with entertainment channel as they often very quick in getting trending in Youtube, meaning we can engage the audience in short time.
* We can cooperate with some channel which is often to get trending in short time such as Saturday Night Live and The Voice
* We can ask our partner or Youtube channel that we are working with to post the video in strategic way such as posting the video around 7-10 AM, use most related tags, use links to get into company homebase or channel so that the company can engage the audience even further, do not disable the comments and rating sections and protect the video so that youtube doesn't remove it
* In enhancing our analysis, we can make further analysis towards the datasets which are coming from common videos or videos in Youtube which are not trending to see the comparison between the trending and the common videos.

*(Disclaimer)The dataset that we are using are coming from trending videos in Youtube USA only.
