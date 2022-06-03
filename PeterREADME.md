# Overview

The project is to analyze the landscape of the movie studio industry, and develop some recommendations for Microsoft Movie Studios about which metrics most impact movie success, and how to leverage that information when selecting a future project. 

Undertaking movie projects is valuable on several levels. They are a source of consumer loyalty and  increase the value of Microsoft’s brand, and they position Microsoft competitively in other related fields, especially when there is an overlap with digital media and franchising opportunities. In addition, a new film project presents a valuable revenue stream. We are going to delve into the expected revenue and explore further, as we assess the value of potential film project opportunities by isolating their potential revenue and their return on investment(ROI). 

Film projects are notoriously risky, and can tie up large amounts of investment for projects that may not come to fruition in the way that studios hope for. However, they can also be quite lucrative, and by analyzing the success and patterns of past films in the market, we hope to shed light on some business decisions Microsoft can make when selecting which projects to pursue that can give them the best odds for success. 

## Research Process 

In order to determine which types of movies Microsoft Movie Studios should pursue when launching a movie studio, we analyzed two datasets from two different data sources. The first, im.db.zip , is a SQL database from the IMDb — an online movie database that includes general information about movies (title, year released, runtime, actors, writers, directors) as well as consumer ratings. From the IMDb database we focused on variables that covered the characteristics of movies, rather than the consumer ratings. 

The second data source we used in our analysis was the tn.movie_budgets.csv from The-Numbers, an online movie database with an open API that covers box office performance and budget information. From this data file we used Worldwide Gross and Budget information for XXXXX movies 

Since there was an overwhelming amount of information across both files, we narrowed down the variables of interest to what we thought was essential for our research. We then joined the two tables to create a large master data set. Finally we created a new variable “Estimated Profit” by subtracting the Production Budget variable from the Worldwide Gross variable. This Estimated Profit variable served as our proxy for ROI for each movie and benchmark for profitability. As a note, we call the variable “Estimated” because the financials of the movie business are complex, and typically a movie studio does not receive the full amount of our Estimated Profit because of marketing costs, payments to distributors and theaters, and the like. 

Once we created our master data set and narrowed our universe down to just profitable movies (where our Estimated Profit variable > 0 ), we were able to dig into the variables we felt were most relevant to starting a profitable movie studio. We focused on three variables: Movie Genre, Movie Director, and Movie Runtime. 

What Are The Most Popular Genres?
We first looked into genres. Genre is one the most important things we need to decide when making movies. There are many different types of movies that are released in theaters every year, but not all of them have the same popularity. Here is the bar chart that we found represents the most popular genres of top 100 profitable movies. We can see action, adventure, sci-fi related movies that are much more popular than types of genres. 
[insert image]
The movie business is a big business and not all movies are money makers; in fact many movies end up being losing bets. So we need to have a clear view on the budget of each of these genres. If Microsoft wants to pursue new movies in any of the top movie genres, the average budget will be somewhere between sixty million to two hundred million dollars. From the previous plot, it shows that the most popular genre is the combination of action, adventure, sci-fi. It is worth noting that this genre of movie also has the highest budget. This makes sense as most of the blockbusters are made on the highest budgets.
[insert image]
Director Impact on Film Performance

One of the links that we wanted to take a closer look at is the link that a director has on the film's performance in the market. When we analyze the data and look at the films that have not just been box office sensations, but also the most profitable, we notice a common theme. There is a strong overrepresentation of many of the same directors within the best performing film projects. In the top 500 most profitable movies that we analyzed, here are the directors that appeared the most frequently: 

![awesome](http://localhost:8888/view/images/Top500perdirector.png)


If we take an even closer look at this data, we can see that even among the top directors, there are some that consistently perform above what is expected. In this next graph, we look at the top directors. That is, the ten directors that appeared most frequently in our high revenue movie projects list:

## insert Scatterplot 

When we compare those ten directors side by side, we can see a few trends. Noticeably, the director whose movies most frequently performed well above the average, and had the highest return on investment (ROI) on his film projects is James Wan. There are other directors that also performed relatively well, such as Tom McGrath and Mike Mitchell, and some relatively low performers such as Tim Burton. It is important to note that a relatively high performance on this chart is extremely impressive, 
considering that the directors are only being compared against other highly successful directors and projects. 

Based on our review of the impact the director has on a films ROI, we strongly would recommend working with one of the established directors on this list, particularly on of the high performers, and if possible, Mr. Wan.  

Analysis of Movie Profitability & Movie Runtime 
The final variable we examined to make a recommendation to Microsoft Movie Studio was a movie's runtime and whether or not that runtime is associated with higher estimated profitability. 

First, when looking at the profitable movie dataset (the dataset where our Estimated Profitability variable was > 0) we found that there was a slight positive correlation between runtime and profitability. 

<<<Scatter on Runtime vs. Estimated Profitability for Profitable Dataset >> 

However, the scatter is not entirely clear and does not tell us much about which runtimes are associated with the most profitable movies. Narrowing down our analysis to the 100 most profitable movies we find that there is still a slight positive correlation, but again does not illuminate which times are consistently seen as profitable. Thus, we plotted a histogram to see the frequency of runtimes associated from the most profitable movies. 

<<Histogram of the most profitable movies and their runtimes>> 

The distribution is an odd shape, but with a few quick calculations we see that the mean runtime for the 100 most profitable movies is 121 minutes and the median is 124 minutes. However, while helpful information, this histogram alone did not shed light on whether or not these runtimes were distinct from other movies — namely movies Microsoft should avoid making: unprofitable movies. 

To dig further, we created a new data set of the 100 least profitable movies (also termed most unprofitable) and mapped the histogram of runtimes from that data set against the histogram of runtimes for the 100 most profitable movies. 

<<Histogram of the most profitable movies and least profitable movies>> 

Here we can clearly see there is a large distinction between the runtimes of the 100 least profitable movies and the runtimes of the 100 most profitable movies. Looking deeper at the descriptive statistics we find that the runtime of the 100 least profitable movies had a mean runtime of 102 minutes and a median of 104 minutes. Interestingly, and of note for our suggestion, the mean and median of the runtimes of the least popular movies did not differ from the same descriptive statistics for runtimes of the overall movie dataset. Thus, it was clear to conclude that a longer runtime — around 120 minutes/2 hours—is associated with more profitable movies. 
To summarize, we recommend that Microsoft make movies that are around 120 minutes in length. 

## Director Impact on Film Performance

One of the links that we wanted to take a closer look at is the one between that a director has on the films performance in the market. When we analyze the data and look at the films that have not just been box office sensations, but also the most profitable, we notice a common theme. Their is a strong overrepresentation of many of the same directors within the best performing film projects. In the top 500 most profitable movies that we analyzed, here are the directors that appeared the most frequently: 

## insert top directors bar graph


If we take an even closer look at this data, we can see that even among the top directors, there are some that consistently perform above what is expected. In this next graph, we look at the top directors. That is, the ten directors that appeared most frequently in our high revenue movie projects list:

## insert Scatterplot 

When we compare those ten directors side by side, we can see a few trends. Noticeably, the director whose movies most frequently performed well above the average, and had the highest return on investment (ROI) on his film projects is James Wan. There are other directors that also performed relatively well, such as Tom McGrath and Mike Mitchell, and some relatively low performers such as Tim Burton. It is important to note that a relatively high performance on this chart is extremely impressive, 
considering that the directors are only being compared against other highly successful directors and projects. 

Based on our review of the impact the director has on a films ROI, we strongly would recommend working with one of the established directors on this list, particularly on of the high performers, and if possible, Mr. Wan.  

# Conclusion
We recommend Microsoft to make a movie which has Action, Adventure, Sci-Fi elements. Based on our research, action and adventure genres are the most frequently appeared genres in the top 100 most profitable movies. Despite the high budget these types of movies typically carry, pursuing them would very likely end up with a positive net return for Microsoft. 
We also recommend that Microsoft employ directors that outperform their peers when it comes to return on investment, especially James Wan.  As one of the most important positions in the film industry, a director plays a pivotal role in the marketing and eventual success of a movie. James Wan, known for “Furious 7” and “Aquaman”, has very positive reviews on his recent blockbusters, which reaffirms our recommendations. 
Finally we suggest that Microsoft make movies that are 2 hours in length. Our research shows that the most profitable movies have a runtime average of 121 minutes compared to 101 minutes in all other films. 

