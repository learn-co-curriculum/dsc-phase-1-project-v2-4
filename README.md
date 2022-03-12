# Phase 1 Project 

MICROSOFT FILMS

Introduction

Microsoft sees all the big companies creating original video content and they want to get in on the fun. They have decided to create a new movie studio, but they don’t know anything about creating movies.

Objectives

-Find ROI:domestic ROI and world wide ROI 
-Which genre do people like?
-Find the most valuable directors

Return on Investment Analysis
We want to find the ideal budget for the best chance at maximizing revenue
Convert budget and revenue datasets into integers

Convert release date to datetime

The movie industry has changed so rapidly. Covid and the prominence of streaming services has dramatically influenced the way people consume movies. In 2020, box office revenue was only 2.09B for the North American film industry. Down from 11.32B in 2019 per Zippia Research. When we're looking at profitability, we want to use the last five years of data to try to account for trends that may no longer be applicable.
Remove outlier movies with no budgets or no revenue that were either never released or the data may be unavailable

Calculate Return on Investment (ROI) for both domestic and gross revenue columns. REMOVE EXTREME OUTLIERS

Let's compare the budget with gross revenues and ROI

Looking above at the table of correlations, some interesting statistics are shown. As you might expect, there is a moderate positive correlation between production budget and both worldwide and domestic gross revenues. The larger the movie, the more revenue you could probably expect. However, budgets have the smallest of effects on a movie's overall profitability. In fact, the correlation between budget and both global and worldwide ROIs is actually negative. This underscores just how difficult it is to produce a successful hit movie and the formula is not as simple as pouring dollars in.

Let's look at some graphs showing budget vs global and domestic ROI

ROI has nearly no correlation to Budget
What genre(s) of movies should Microsoft pursue?
Let's start by looking at the types of info in our dataframes

After looking at the rt_reviews_df table, movie titles were not listed so we only focused on tmdb_movies_df. We want some rows with certain amount of vote count, so we check the describe and drop all row with low vote count.

Drop all rows below vote_count.mean() and rows with no genre id

Let's look at the new vote count

The Correlation between Good rating and popularity

Let's create a visualization for the average vote score vs popularity
Even if your movie is highly rated, popularity is not assured

Popularity is more valuable than rating. Which genre(s) are most popular?
We must convert genre from integer to string

Store all rating and popularity as list in a dict call dict_of_genre.

Who are the directors Microsoft should want based upon our chosen genres and box office success?

Let's look at the respective datatypes

Let's look at the recommended directors and writers Microsoft should align with
