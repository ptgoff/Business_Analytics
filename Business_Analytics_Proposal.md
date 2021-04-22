# Business Analytics Proposal
Peter Goff

## Question/need:
    
Netflix needs to expand their offerings to viewers, which means making decisions on which movies & shows to integrate into their catalogue. Anime has a strong viewership base in Asia and modest and 
[growing viewership among Western viewers](https://www.grandviewresearch.com/industry-analysis/anime-market). Exploration of expansion into the anime market seems timely.<br>

One challenge in the acquisition of movies and shows lies in making out-of-sector recommendations for viewers who have not seen - and therefore have not rated - these selections. A potential solution to this challenge lies in the integration of an external data-source that contains rated media within the Netflix library and media beyond the Netflix library. By linking movies across these databases, I can identify how ratings among the sub-section of anime movies within the Netflix catalogue correspond to those beyond the catalogue. <br>

The challenge at this point lies in reconciling rating differences. The Anime Movie Database is populated by anime enthusiasts, who may well have different tastes and preferences than the do general Netflix viewers (picture the rating differences between audience ratings and critic ratings on [Rotten Tomatoes](https://www.rottentomatoes.com/about)). <br>
Ideally, I would like to build a clustering model using NLP movie/show descriptions coupled with salient movie/show variables. This approach would allow me to take movies that are highly rated by Netflix and provide out-of-catalogue recommendations based on similar movies within the same cluster. Such an approach would avoid a naive recommendation of all highly-rated movies from the Anime Movie Database. <br>

Lastly, the person-level data of the Netflix database can be further leveraged by modeling alignment between external ratings and their own ratings. Netflix viewers with a strong alignment between their ratings of anime media and those from the Anime Movie Database could be identified - counted and described. More importantly, recommendations for these individuals can be directly informed by ratings from the Anime Movie Database. <br>

For those viewers whose tastes diverge from anime cannon, we can again draw from the clustering model to select movies/shows that, although having low-ratings from the Anime Movie Database, are apt to be appealing to this segment of viewers. <br>
In sum, this project will (a) provide descriptive overview of anime viewership within Netflix, (b) facilitate the selection of out-of-sample anime media, and (c) inform recommendations of out-of-sample shows across a latent, heterogenous anime viewership.

## Data Description:
* [User-level Netflix data](https://www.kaggle.com/netflix-inc/netflix-prize-data) is available through Kaggle (updated 2020).
* [Movie-level Anime data](https://www.kaggle.com/thomaskonstantin/top-10000-anime-movies-ovas-and-tvshows) contains the top 10,000 anime movies and shows with a short synopsis for each record. 
* [User-level Anime data](https://www.kaggle.com/CooperUnion/anime-recommendations-database) contains data from 73,516 users on 12,294 anime movies/shows along with genre tags.

All three databases are available for download and can be linked via the movie/show name. 

## Tools:
The Netflix database appears to be prohibitively large for manipulation in Excel (480,000 across 17,780 movies/shows). My goal is to:
* Load the Netflix database into Python and restructure the data to have a person-level dataset where an observation is person-movie specific.
* Merge the Netflix movie names (using Netflix provided movie ids)
* Merge the Anime movies and related data.

At this point I can cull the data to only those records with X or more anime movies. This will be the dataset I will import into Excel. Importantly, this decision will omit all viewers who have never viewed/rated an anime movie/show. This omitted group consists of individuals who haven't watched/rated anime because they don't like it and those individuals who haven't watched/rated anime and may like it. Subsequent analyses should seek to differentiate these groups to provide the later with appropriate recommendations. 

Within Excel I will:
* Construct summary statistics and descriptive visualizations of Netflix anime viewership. 
* Calculate the rating alignment between the subsample of anime movies/shows that are in the Netflix database.
* Present a naive recommendation for anime acquisition using this rating alignment. 
    * Use features of the anime movies/shows (genre tags, keywords) to classify movies/shows and recommend those with both high ratings and high alignment.

With Tableau I will:
* Construct an interactive visualization that will allow users to drill-down into the recommendations. For example, the base visualization may be a caterpillar plot of anime movie/show ratings by index. Using radio-buttons, the viewer could then view a slice of this graphic that identifies which of these data-points are in the Netflix library. Another option would allow the viewer to scale the data points in accordance with the Netflix rating. Another option would allow the viewer to subset by genre. 

## MVP Goal:
* A descriptive summary of Netflix anime viewership. Specifically:
    * Average number of anime ratings per person and changes over time
    * Internal rating consistency: Alignment between a viewer's rating of Netflix anime movies/shows and their ratings of other Netflix media. 
    * External rating consistency: Alignment between a viewer's rating of Netflix anime movies/shows and those available from other sources. 
    * Average Netflix rating of anime movies/shows and changes over time.

* A recommendation of out-of-sample movies/shows
* An interactive graphic of movie/shows ratings



```python

```
