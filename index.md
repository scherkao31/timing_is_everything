---
layout: post
title: Is timing everything ?
subtitle: A Data-Driven Dive into Movie Release Strategies and Success
cover-img: /assets/img/season_movie.jpg
thumbnail-img: /assets/img/thumb.png
share-img: /assets/img/path.jpg
author: Léa, Pierre-Hadrien, Yanruiqi, Jason and Salim
---

Sometimes, despite having all the pieces in place and doing everything right, success seems elusive. It's often a game of patience. Hard work is undoubtedly a significant factor in achieving success, but there's another crucial element at play – timing. It's about being in the right place at the right moment, seizing opportunities as they arise, and connecting with others at just the right time.

Movies reflect this aspect of life brilliantly. The impact of a film on us depends not just on its content, but also on when we watch it. The right movie at the right time can make us laugh, cry, or reflect. It's a personal experience, unique to each viewer.

But let's zoom out from the individual experience to the broader perspective of the movie industry. Have you ever considered how the timing of a movie release might be a key to its success? In our story, 'Is Timing Everything?', we delve into the CBU movie dataset to explore this fascinating aspect. We'll look at how the release dates of movies influence their success and reception. So, whether you're a film lover, a data geek, or just someone intrigued by the behind-the-scenes of the movie world, join us. We'll dive into patterns, make predictions, and maybe even unearth some insights useful for filmmakers and the movie industry. Life is often about luck, but what if you could sway it in your favor? What if you knew exactly how to time the release of your masterpiece? Ready to make yourself lucky? Let's begin: Action!

_______________________________________________________________

# Release Dates and Movie Genres - Orchestrating the Perfect Season (Question 1)

Let's dive into the intriguing interplay between movie genres and their release calendars. Are horror films naturally drawn to Halloween? Do summer months exclusively belong to action-packed blockbusters? In this part of our story, we'll try to see if there are any recurring patterns between a film's genre and its release timing within a year. Do these rhythms exist, and if so, do they change depending on where the movie is released? This exploration isn't just about identifying patterns; it's about understanding whether these insights can help us predict the genre of upcoming film releases in different seasons. It's time to discover if there's a secret rhythm dictating when different genres of movies make their grand entrance on the big screen.

### 1.1 Sub-part title
Add your stuff here.
### 1.2 Sub-part title
Add your stuff here.
### 1.3 Sub-part title
Add your stuff here.
### 1.4 Sub-part title
Add your stuff here.

#### Transition :

As our data story unfolds, it's clear that certain movie genres do have their preferred release times. But why? While it's straightforward for Christmas and Halloween movies, other genres aren't as clear-cut. Perhaps production companies are tuning into the public's mood, providing just the right kind of film at just the right time. Or maybe, they've learned from experience that release timing can significantly influence a film's success. After all, isn't that a key goal for them - to make their movies as successful as possible? But here's a thought - what exactly defines success in the film industry? Is it the accolades from peers or the applause from the audience? Well, it's time to explore both. To satisfy the film aficionados among us, let's first dive into how the release calendar impacts the most prestigious accolade in the movie world – the Oscar.

_______________________________________________________________

# Setting Your Watch for the Red Carpet - How Timing Influences Oscar Success (Question 2)

Now, as we roll out the red carpet, it's time to see how timing influences a movie's journey to Oscar glory. Is there a 'golden month' for releasing a film that could increase its chances of capturing that coveted golden statue? In this part of our exploration, we will try to see which factors impact a movie's success, especially in terms of its likelihood to win an Oscar. Does release timing play a crucial role, and has its effect evolved over time? We're also going to delve into whether it's possible to predict a film's Oscar odds based on various factors, including its release month, the country of origin, language, and more. Let's discover the intricate dance between the calendar and the Oscars.  

### 2.1 Overview
There is no shortcut to win the crown. However, good timing makes an easier way! We can sometimes observe that winning movies are not always promised to be the best. While opinions on the quality of movies can vary, one example often cited as a movie with mixed critical reception that still won multiple Oscars is "Crash" (2004). Directed by Paul Haggis, it won the Academy Award for Best Picture at the 78th Academy Awards. However, its victory was met with controversy, as some critics and viewers felt that other films, such as "Brokeback Mountain," were more deserving. Another example is "The Greatest Show on Earth" (1952) directed by Cecil B. DeMille. This circus drama won the Academy Award for Best Picture at the 25th Academy Awards. While it achieved commercial success, it wasn't universally praised by critics and has received a quite low IMDb rating of only 6.5/10.  

Among other factors, We will ask, if the release timing plays a role in winning an Oscar prize. We first have a look at how the movies with different release months are distributed in the Oscar selection.  
[Release_Month_Distribution]("assets/img/Release_Month_Distribution.png")  

The imbalanced distribution indicates that we can explore how timing poses an impact on the possibility of winning an Oscar. For example, why movies released in December are significantly more than in other months?  

### 2.2 Level I: Entry to Oscar selection
As a bright pearl in the film industry, the Oscar Prize favors only the most successful movies with profound thinking and artistic value. Due to the fierce competition for final awards, many good movies cannot eventually get the Oscar prize, but getting selected as Oscar candidates is also an amazing achievement. Therefore, directors holding films with aspirations for the Oscar awards want to ask, if an optimal release timing can help them to win in the Oscar selection more easily. Generally, we can inspect the ratios of selection in each month. To view the results more clearly, we run a k-means clustering for release months.  

[Selection_Kmeans]("assets/img/Selection_Kmeans.png")

From the graph, the optimal timings for entering Oscar selection are December and June, while movies released from January to April are harder to win the favor of the judges.

### 2.3 Level II: Oscar Winner
Do you know, that only **17.35%** nominated movies successfully take home Oscar awards! And thinking about the low selection ratio, winners need not only good quality films but also some good luck.  

If a director has produced a film expected to be highly praised and is confident that this movie can be selected for Oscar grading for sure, when is the optimal timing in this case? Is it the same as timing for Level I players? We investigated it by clustering the winning ratio in the Oscar selection dataset.  

[Win_Kmeans]("assets/img/Win_Kmeans.png")  

The results reveal that the optimal timing is shifted to January and May, and December is now a very bad choice, only better than June and July.  

How does the winning probability change over the years?  

[Dynamic Graph: Oscar Probability over Years]
[Oscar_Probability_over_Years]("assets/img/Oscar Probability over Years.png")

### 2.4 Confounders: Locations and Languages
Except for the timing, other factors may influence the winning probability as well. Here, we can take locations and languages into account.  

We first check their percentage in the selected movies dataset.  
[Movie_Countries_Selected]("assets/img/Movie_Countries_Selected.png")
[Movie_Languages_Selected]("assets/img/Movie_Languages_Selected.png")

Then, for the winners:
[Movie_Countries_Win]("assets/img/Movie_Countries_Win.png")
[Movie_Languages_Win]("assets/img/Movie_Languages_Win.png")

They show the phenomenon that US movies and English movies take a predominant majority because they are mostly overlapping. We therefore assume that the influence of languages can be covered in location influence. For simplicity, we convert the countries to continents. 

[Win_Possibility_per_Continent]("assets/img/Win_Possibility_per_Continent.png")

It presents that the most intense competition happens in North American movies. Even though their number is large in absolute value, it is never easy for them to win Oscar awards. In contrast, each Oceanian movie selected has a 40% winning probability.  

Based on this, we suggest that **common** North American directors, with the wish to win Oscar prizes, should generally consider releasing new movies in January and May. For **common** Australian directors, they should release the films in December and June.

As a detailed exploration, we run clustering on the continental subsets to evaluate the chance of winning an Oscar after the nomination. 

[Continent_Clustering]("assets/img/Continent_Clustering.png")

Then we can advise **successful directors** who promise to have Oscar-selected movies: 
- for American and European movies, the general suggestion in Level II  (January) still holds.
- despite the limited data, we are reluctant to say that, for Asian movies, the optimal timings are March, August, and November, while for Oceanian movies November is the only best time
- for African and South American movies, we cannot conclude anything without extra data.

Intuitively, this is shown in the heat map below.
[Oscar_Heatmap]("assets/img/Oscar_Heatmap.png")

## 2.5 Box Office Revenue

To continue our analysis of research question 2, we now delve into the other factors impacting a movie's success. We start by looking at the box office revenue of the movies in our dataset. Our insight leads us to believe that higher box office revenues are correlated with a higher probability of winning an Oscar, which we will test via statistical analysis.  

Let us first plot the box office revenue of movies based on whether they received an Oscar or not.  

[Oscar_Box]("assets/img/Oscar_Box.png")

Mean Box Office Revenue (Oscar Winners): $141.49 million  
Standard Deviation Box Office Revenue (Oscar Winners): $274.32 million  

Mean Box Office Revenue (Non-Winners): $94.29 million  
Standard Deviation Box Office Revenue (Non-Winners): $164.44 million  

The difference in Mean Box Office Revenue between Winners and Non-Winners: $47.20 million  

As shown by the box plot and the statistics of our movies' box office revenues, we can see that the average and median box office revenue of movies that received an Oscar is higher than the average box office revenue of movies that did not receive an Oscar. We also notice that the standard deviation of the box office revenue of movies that received an Oscar is much higher than for those that did not, indicating more variability in this category.  

Indeed, if we compare the differences between the highest and lowest-grossing movies that have received an Oscar, we notice a huge difference as shown below. Movies such as "The Times of Harvey Milk" received the Oscars for Best Documentary Feature in 1984 with a box office revenue of 29,802 USD, while movies such as "Avatar" received the Oscars for Art Direction in 2009 with a box office revenue of 2,782,275,172 USD. This indicates that the Oscars Awards do not necessarily reflect the success of a movie, which can often be the case for movies that are not blockbusters.  

To test whether the difference in box office revenue is statistically significant, we will perform a Welch's t-test. This test is used to test the null hypothesis that two populations have equal means. It is an adaptation of the Student's t-test and is more reliable when the two samples have unequal variances and unequal sample sizes.  

The key findings of this analysis are as follows:  

1) T-test Results:  

- T-test statistic: 3.49  
- T-test p-value: 0.0005  

Conclusion: The t-test results reveal a substantial difference in box office revenue between movies that received Oscars and those that did not. The low p-value of 0.0005 indicates a high level of statistical significance. This suggests that the observed difference in box office revenue is unlikely to have occurred by random chance.  

2) Correlation Analysis:  

- Correlation coefficient: 0.09  
- Correlation p-value: 0.0005  

Conclusion: The correlation analysis indicates a significant positive correlation (coefficient of 0.09) between box office revenue and the number of Oscars won. The low p-value of 0.0005 reinforces the statistical significance of this positive correlation. Therefore, higher box office revenue is associated with an increased likelihood of receiving Oscars.  

Our analysis provides compelling evidence supporting a clear relationship between box office success and Oscar recognition. The statistically significant t-test results affirm that movies with Oscars differ significantly in terms of box office revenue from those without Oscars. Additionally, the positive correlation observed further emphasizes that higher box office revenue is positively linked to an increased likelihood of receiving Oscars. This underscores the influential role of commercial success in garnering industry acclaim and recognition.  

However, as we have shown previously, it is important to notice that the Oscars do not necessarily reflect the success of a movie. Indeed, the Oscars can be awarded to movies that are not blockbusters. This is why we will now look at the ratings of the movies in our dataset to see if they are correlated with the Oscars.  

## 2.6 Ratings

We will now conduct a similar analysis to the one we performed for box office revenue, but this time for ratings. We will start by plotting the ratings of movies based on whether they received an Oscar or not.  


Mean Average Vote (Oscar Winners): 6.89  
Standard Deviation Average Vote (Oscar Winners): 0.92  

Mean Average Vote (Non-Winners): 6.59  
Standard Deviation Average Vote (Non-Winners): 0.92  

The difference in Mean Average Vote between Winners and Non-Winners: 0.29  

Once again, we can see that movies that received an Oscar have a higher average and median rating than movies that did not receive an Oscar. We also notice that the standard deviation of the ratings of movies that received an Oscar is higher than for those that did not, indicating more variability in this category, as noticed for the box office revenue.

To test whether the difference in ratings is statistically significant, we once again performed a Welch's t-test.  

The key findings of this analysis are as follows:  

1) T-test Results:  

- T-test statistic: 5.77  
- T-test p-value: 8.99e-09  

Conclusion: The t-test results indicate a substantial difference in average ratings between movies that won Oscars and those that did not. The extremely low p-value of 8.99e-09 underscores the high level of statistical significance. This implies that the observed disparity in average ratings is highly unlikely to have occurred by random chance.  

2) Correlation Analysis:  

- Correlation coefficient: 0.12  
- Correlation p-value: 8.99e-09  

Conclusion: The correlation analysis reveals a significant positive correlation (coefficient of 0.12) between average ratings and the likelihood of winning an Oscar. The extremely low p-value of 8.99e-09 emphasizes the statistical significance of this positive correlation. Therefore, higher average ratings are associated with an increased likelihood of winning the Oscars.  

In Summary:  

Our analysis provides compelling evidence supporting a clear relationship between average ratings and Oscar recognition. The statistically significant t-test results affirm that movies with Oscars differ significantly in terms of average ratings from those without Oscars. The positive correlation observed further indicates that higher average ratings are positively linked to an increased likelihood of winning the Oscars. This underscores the importance of critical acclaim and audience appreciation in influencing industry recognition.  

Associated with our analysis of box office revenue, this statistical test and the measures of our ratings prove once again the importance of a movie's sucess in its likelihood of receiving awards. However, as we have shown previously, it is important to notice that the movies that have received Oscars can divert from these assumptions, receiving low ratings and box office revenue. This is mostly due to artistic opinions directing the awards designations, which can be very different from the public opinion, as well as categories. Movies such as documentaries or foreign ones are often less likely to gross high revenues or receive high ratings, but can still be awarded Oscars. We show these deviations in the following section.  

[Oscar_Category_Box]("assets/img/Oscar_Category_Box.png")
[Oscar_Vote_Box]("assets/img/Oscar_Vote_Box.png")

As we can see from the two box plots shown above, there is a significant difference in box office revenue and ratings between movies that received Oscars based on their category. Movies with Oscars such as Best Actress (in general) or Best Documentary generally received lower box office revenue and ratings than movies with Oscars such as Best Short Film or Actor. We also notice that the best documentary categories showcase an especially high variability in box office revenue and ratings, which is not the case for the best short film category. All these features indicate thus once again the biases that can be shown in the Oscars awards, which are not always correlated with the success of a movie, even though on a general basis, the Oscars are awarded to movies that have a higher box office revenue and ratings.  

#### **Conclusion:** 

USA is the country of most movies in the dataset, and the majority of movies are in English. While the correlation between release month and whether the movie wins an Oscar award is weak, release timing might still be a significant factor influencing the success of the movie. 

#### Transition :

Alright, film enthusiasts, brace yourselves for a bit of a reality check. Let's face it - are Oscar-winning movies always the ones we enjoy the most? Think about it. We know the superhero blockbusters aren't exactly Oscar bait, but come on, how good was the latest Spiderman? With that in mind, let's shift our focus from the glittering Oscars to the wider world of box office hits and audience favorites. After all, there's more to movie success than just golden statues.

_______________________________________________________________

# Box Office and ratings – Timing the Public's Pulse (Question 3)

As we continue our quest to discover if a movie's success can be timed, we now turn to the big question: how does the release timing impact a movie's box office success and public appeal? We're about to connect the dots between calendars, cash, and crowds. For this, we'll delve into the box office, which essentially measures the total revenue a movie earns from ticket sales. It's a fair assumption that the more people flock to see a movie, the more it resonates with the general public.

But that's not the only metric we're considering. We're also looking at how viewers rate movies, another crucial indicator of public opinion.

In this part, we will try to see how the release month of a movie influences its overall success and popularity. We'll examine this through various lenses – box office revenues, viewer votes, and ratings, while also considering how the quality of data documentation has evolved over the years. Let's dive into this multifaceted analysis and see what the numbers reveal about timing and movie success.

### 3.1. Ratings Versus Revenue – Does a "bad movie" makes less money than a "better" one ?
First, let's tackle the correlation between ratings and revenue. It seems intuitive that higher ratings should mean more money, right? Well, our data tells a more nuanced story. We'll explore why movies with mediocre ratings don't necessarily earn less, and how those with top ratings don't always hit the jackpot in terms of revenue. It's a complex equation where excellence in ratings doesn't always translate into box office gold.
### 3.2. Timing and Ratings – Searching for a Pattern
Next, we look at whether there's a link between when a movie is released and the ratings it receives. Does a summer blockbuster get rated differently from a cozy winter flick? Our findings might surprise you, as we unravel the (non)relationship between release months and how viewers rate these films.
### 3.3. Box Office Timing – Identifying the Lucrative times
#### 3.3.1. By Month – The Monthly Box Office Cycle
Let's break down the box office cycle month by month. We'll analyze which months are box office magnets, attracting audiences in droves, and which ones seem to be stuck in a cinematic slump. Our data suggests that not all months are created equal when it comes to raking in the revenue.
#### 3.3.2. By Season – The Seasonal Box Office Trends
Zooming out, we'll assess box office performance by season. Is summer really the blockbuster champion? Does winter bring more than just the holiday spirit to theaters? We'll see how each season stacks up in the race for box office success.

#### Transition :
Small conclusion

_______________________________________________________________

# Conclusion

Summary, and conclusion.
<iframe src="assets/plot/distribution_ethnicity.html" width="750px" height="530px" frameborder="0" position="relative">Genre plot</iframe>

Deuxième : 

<iframe src="assets/plot/plot.html" width="750px" height="530px" frameborder="0" position="relative">Genre plot</iframe>
