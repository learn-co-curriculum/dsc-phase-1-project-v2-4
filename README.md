# Han and Jeff Microsoft Streaming Service Project (Project 1)

### Overview

This project explores the profitability, ROI, and user engagement of various genres of film to recommend
films for Microsoft to grow their new streaming service.

### Business Understanding
* Which genre got most profitability, ROI
* which genre got most engagement and ratings to get Microsoft movie good reputation
* which is the best season for movie release

### Conclusion
* We found that Adventure, Sci-Fi, Animation, Action, Comedy, and Drama (in that order) were relatively high-performing on most or all metrics.
* Biography films were intersting in that they had very high ratings, although they performed poorly financially. 
* Films with multiple genres also performed better on both financial measures.


### Data Understanding and Analysis
we explored these datasets:
* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [List of films based on video games](https://en.wikipedia.org/wiki/List_of_films_based_on_video_games)
* [Film Adaptations of Video Games](https://www.kaggle.com/datasets/bcruise/film-adaptations-of-video-games?resource=download)



### Files

* Jeffsploration contains Jeff's Jupyter Notebook Jeffsploration uses imdb data together with budget data from the-numbers.com to create visualizations comparing genres as well as number of genres for films. Data wrangling and exploration is done with pandas. Genres are one-hot encoded so that a mask can be created. This allows values for each genre to be aggregated, and these aggregates include the genres when a film has multiples. Data visualizations are done with matplotlib.

* hy_exploration_1: han's early EDA

* hy_exploration_2: han's second EDA and plots exploration

* hy_exploration_3: han's cleaned-up and Final Notebook. it covers data import, data cleaning, brief observation and plots.

* Growing a Streaming Service.pptx: presentation doc

* Plots folder contains exported images of seaborn and matplotlib images