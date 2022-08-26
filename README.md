# Microsoft’s Movie Studio
This repository was created to enable exploratory data analysis into the movie industry, specifically for films made from 2000 - 2018. The original stakeholder goal was to find the top performing genres in the box office, but through data analysis, the team was able to come up with three recommendations for Microsoft's market entry.
 
# Bottom Line Up Front
The team's exploratory data analysis discovered a few recommendations for Microsoft’s potential market entry.
The top genres to invest in are horror, myster, and thriller movies.
Aim to make a horror movie as they have the highest return on investment. (ROI)
Target either Lionsgate Films or Warner Bros. Pictures as a studio to collaborate with.
Hire Jason Blum as the producer for this horror film.
 
## Business Understanding
The business problem at hand is that Microsoft (our stakeholder) is looking at a potential market entry into the movie industry. They tasked the team with exploring what types of films are currently doing the best at the box office. Once these genres were identified, the team used their knowledge of the industry and insights found in their dataset to further provide recommendations for Microsoft’s market entry plan. 
 
Through the team's exploratory data analysis, they identified that the best risk/reward for Microsoft would be to invest in a horror, myster, or thriller movie due to the mean ROI for all three genres to be over 750% from 2000 - 2018. Then the team identified experienced studios in Lionsgate and WB to collaborate with for their first movie. And finally, the team identified Jason Blum (owner of Blumhouse Productions) to be their producer for this potential horror movie.
 
This project assumes that Microsoft will take the findings from the team's dataset and implement a plan to create their first movie as a horror movie working with Lionsgate or WB with Jason Blum as the movie's producer. 
 
## Data Analysis - Initial Setup
The following datasets were used to start the teams exploratory data analysis:
 
Bom.movie_gross.csv
Im.db
Rt.movie_info.tsv
Rt.reviews.tsv
Tmdb.movies.csv
Tn.movie_budgets.csv
 
These datasets each provided unique information, which was helpful when the team started their initial data exploration. As the team explored the ~238,000 entries, it was realized that a few datasets were more valuable for some of the trends they were discovering. The datasets primarily used for this analysis were tn.movie_budgets, bom.movie_gross.csv, and im.db. These dataframes contained information such as unique movie ID’s, release dates, production budgets, domestic gross revenue (United States), worldwide gross revenue, studio, genres, average IMDB rating, number of votes from IMDB, category (job title), and name of the person who held that category.
 
That being said, there are a few limitations that this dataset has. The first is the depth of the information. For example there is no budget breakdown showing how much is spent on director, producer, actors, staff, and etc. Another example is the quality of the data, which had several missing entries that had to be dropped from the main dataset completely. Lastly, the team noticed a definitive bias towards blockbuster films. A shallow exploration of the data revealed that several top foreign and independent films were missing data for our final analysis.
 
## The Notebooks
Each team member created a separate branch to help facilitate data analysis without creating any issues to the original data set. The branches created were labeled with the team members name. Inside of those branches similar naming schemes were used to identify what part of the project the file was for. The main files are the “clean/cleaning dataset” for the finalized data cleaning product. “Recommendations” to create visualizations for the team's recommendations. And finally, “movie_data_erd.jpeg”, which is an Entity Relationship Diagram for im.db.
 
# Methods
## microsoft_main
The first major section of the microsoft_main.ipynb includes the creation and cleaning of the movie_profession dataframe which was read from the im.db and converted to a csv file to make the merging and cleaning processes easier.  
 
Within the IM database, the most pertinent columns include movie_id, primary_title, genres, and the movie professions categories and person’s names.  The movie ID’s were used as the primary and foreign keys to allow the merges of columns. 
 
The other relevant dataframe created was the movie_revenue dataframe using information including release date, gross revenue, and the production budget gathered from the tn.movie_budgets.csv and bom.movie_gross.csv files. An important column, “ROI” (Return on Investment)  was created in the movie_revenue dataframe by calculating the gross revenue minus the production budget and then dividing that difference by the production budget. This result is then multiplied by 100 to give us the ROI percentage. It is important to note that the ROI column was separated by the different genres. 
 
Ultimately, the movie_revenue dataframe will merge with the movie_profession dataframe to create the master_movie dataframe. In the master_movie dataframe, the team removed rows with NULL values, removed duplicate entries, and dropped all unnecessary columns. 
 
The studio and producer recommendations were filtered by experience in terms of the number of movies made in the recommended genre as well as their history of ROI success. 
 
### Gross Revenue by Genre
![graph1](./images/gross_revenue_by_genre.png)

Here the team explored what types of films are currently doing the best at the box office by using the worldwide gross revenue metric and separating the movies into their respective genres. Adventure, action, comedy led the genres in world wide gross revenue, however this initial analysis does not paint the whole picture because the team need to look at other factors such as the production cost metric amongst genres to make the best business decision. 
 
### Production Budget by Genre
 ![graph2](./images/production_budget_mean.png)

This visual is conveying that the highest grossing genre movies such as adventure, action, comedy often require a higher production budget. The team wants to recommend the genres that have the best proportion of low production budget with a high gross revenue to maximize the return on investment. 

### ROI by Genre
![graph3](./images/roi_mean.png)

ROI was used because it gives Microsoft the highest return with the lowest risk, especially considering this will be Microsoft’s first movie. The best performing genres in terms of ROI are horror, mystery, and thriller, which leads to the recommendation of the horror genre with a ROI mean of 1200%.

### Horror Studios
![graph4](./images/horror_studios.png)

Lionsgate Films and Warner Bros. Pictures were the two studios chosen for Microsoft to approach when trying to collaborate for their first movie. This is due to their experience with making horror movies over the last 20 years with making 8+ horror movies during that time in this dataset. The reason why Universal, Paramount, and Screen Gems are not recommended for a collaboration movie is due to their connections with NBC, CBS, and Sony respectively. The team identified large business conglomerates with adjacent movie/tech/streaming involvements to be competitors and hostile to Microsoft’s market entry.
 
### Horror Producers
![graph5](./images/horror_producers.png)

After looking at a studio experienced with horror movies, the team then sorted producers by the number of horror movies they’ve made. The team decided to recommend Jason Blum for a few reasons. After further analysis Jason Blum has his own production company “Blumhouse Productions”, which focuses on creating horror movies. It also helps that in terms of ROI he is one of the best in the business, with being credited for producing Paranormal Activity on a budget of $15,000 and grossing over $200 million worldwide. 
 
# Conclusions
The movie genres that have the highest ROI are horror, myster, or thriller. These projects will give Microsoft the most bang for their buck and won’t cause their pockets to feel too light if the movie flops, due to the low budget of each of these movie types. The focus is to gain as much movie making experience as possible, so a partnership with either Lionsgate or WB is advised. And finally, hiring or partnering with Jason Blum as the producer of Microsoft’s first film will help further increase the experience they gain from this market entry.
 
## Future Investigations
Analysis on movie runtimes and how they affect box office revenues. If possible, this should also be done by genre.
Investigating movie ratings (G , PG, PG-13, R, and NC-17) and how they affect revenue. Again preferably done through the lenses of genre.
Market analysis on if Microsoft should develop their venture into the movie industry for the box office or for streaming. Potentially through their own service.
 
## For More Information
Please review our full analysis in our [our Jupyter Notebook](./microsoft_main.ipynb) or our [presentation](./presentation.pdf).
 
For any additional questions, please contact **Juana Tavera | tvrjuana@gmail.com, Henry Shin | hjshin386@yahoo.com Mackoy Staloch | mackoy.staloch@gmail.com**
 
## Repository Structure
```
├── README.md                        <- The top-level README for reviewers of this project
├── microsoft_main.ipynb             <- Narrative documentation of analysis in Jupyter notebook
├── presentation.pdf                 <- PDF version of project presentation
├── data                             <- Both sourced externally and generated from code
└── images                           <- Both sourced externally and generated from code
```
