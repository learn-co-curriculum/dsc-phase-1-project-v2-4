# Han and Jeff Microsoft Streaming Service Project (Project 1)

### Overview

This project explores the profitability, ROI, and user engagement of various genres of film to recommend
films for Microsoft to grow their new streaming service.

### Business Understanding
* Which genre got most profitability, ROI
* which genre got most engagement
* which is the best season for movie release

### Conclusion
* We found that Adventure, Sci-Fi, Animation, Action, Comedy, and Drama (in that order) were relatively high-performing on most or all metrics.
* Biography films were intersting in that they had very high ratings, although they performed poorly financially. 
* Films with multiple genres also performed better on both financial measures.


### Data Understanding and Analysis
In the folder `zippedData` are movie datasets from:

* [Box Office Mojo](https://www.boxofficemojo.com/)
* [IMDB](https://www.imdb.com/)
* [Rotten Tomatoes](https://www.rottentomatoes.com/)
* [TheMovieDB](https://www.themoviedb.org/)
* [The Numbers](https://www.the-numbers.com/)

Because it was collected from various locations, the different files have different formats. Some are compressed CSV (comma-separated values) or TSV (tab-separated values) files that can be opened using spreadsheet software or `pd.read_csv`, while the data from IMDB is located in a SQLite database.

![movie data erd](https://raw.githubusercontent.com/learn-co-curriculum/dsc-phase-1-project-v2-4/master/movie_data_erd.jpeg)

Note that the above diagram shows ONLY the IMDB data. You will need to look carefully at the features to figure out how the IMDB data relates to the other provided data files.

It is up to you to decide what data from this to use and how to use it. If you want to make this more challenging, you can scrape websites or make API calls to get additional data. If you are feeling overwhelmed or behind, we recommend you use only the following data files:

* `im.db.zip`
  * Zipped SQLite database (you will need to unzip then query using SQLite)
  * `movie_basics` and `movie_ratings` tables are most relevant
* `bom.movie_gross.csv.gz`
  * Compressed CSV file (you can open without expanding the file using `pd.read_csv`)



### Files

* Jeffsploration contains Jeff's Jupyter Notebook Jeffsploration uses imdb data together with budget data from the-numbers.com to create visualizations comparing genres as well as number of genres for films. Data wrangling and exploration is done with pandas. Genres are one-hot encoded so that a mask can be created. This allows values for each genre to be aggregated, and these aggregates include the genres when a film has multiples. Data visualizations are done with matplotlib.

* hy_exploration_1: han's early EDA on IMDA and TM

* hy_exploration_2: han's second EDA and plots exploration

* hy_exploration_3: han's cleanedup and final Notebook. it covers data import, data cleaning, brief observation and plot attempts.

* Growing a Streaming Service.pptx

* Plots folder contains exported images of seaborn and matplotlib images