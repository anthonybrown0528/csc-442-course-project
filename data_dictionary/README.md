# Data Dictionary

## Netflix IMDb Scores Data Dictionary

| Field Name | Data Type | Attribute Type | Description | Missing Values | Example |
| :---- | :---- | :---- | :---- | :---- | ----- |
| index | int | ordinal | Index in the Netflix IMDb scores dataset. | No | 4811 |
| id | String | ordinal | Id associated with the media. | No | ts304058 |
| title | String | nominal | Title of the media. | No | Ganglands |
| type | String | nominal | Either "SHOW" or "MOVIE" defining the media as a show or movie respectively. | No | SHOW |
| description | String | nominal | Brief description of the what the media is about. | Yes | Mehdi, a qualified robber, and Liana, an apprentice thief, get involved in a turf war between drug dealers, and have to collaborate in order to save their loved ones. |
| release\_year | int | interval, discrete | Year the movie was initially released. | No | 2021 |
| age\_certification | String | ordinal | Content rating. | Yes | TV-MA |
| runtime | int | interval, discrete | Runtime for the movie or for a singluar episode if the media is a show. | No | 46 |
| imdb\_id | String | ordinal | IMDb score ID. | No | tt13278100 |
| imdb\_score | float | interval, continuous | IMDb score of the media. | No | 7 |
| imdb\_votes | int | ratio, discrete | Number of IMDb votes for the media. | Yes | 2460 |

## Netflix Movies and Shows


| **Field Name**  | **Data Type** | **Attribute Type**      | **Description** | **Missing Values** | **Examples** |
|---------------|------------|--------------------|-------------|---------------|-----------|
| show_id      | Object     | Ordinal           | A unique ID given to every show/movie in the dataset. | No | s2 |
| type         | Object     | Nominal           | Represents whether the recording is a movie or show on Netflix. | No | TV Show |
| title        | Object     | Nominal           | The title of the movie or show listed on Netflix. | No | Blood & Water |
| director     | Object     | Nominal           | Director(s) of the movie or show. | Yes | Haile Gerima |
| cast         | Object     | Nominal           | Actors involved in the movie or show. | Yes | Ama Qamata, Khosi Ngema, Gail Mabalane, Thaban... |
| country      | Object     | Nominal           | The country where the movie or show was made. | Yes | South Africa |
| date_added   | Object     | Ordinal, Discrete | Date the movie or show was added to Netflix. | Yes | September 24, 2021 |
| release_year | int64      | Interval, Discrete | Year the show/movie was officially released to the public. | No | 2021 |
| rating       | Object     | Nominal           | Appropriate age restriction/recommendation for the show/movie. | Yes | TV-MA |
| duration     | Object     | Interval, Discrete | Length of the movie/show. Movies are represented in minutes, and shows are represented with the season count. | Yes | 90 min |
| listed_in    | Object     | Nominal           | Categories on Netflix where the show/movie is listed. | No | International TV Shows, TV Dramas, TV Mysteries |
| description  | Object     | Nominal           | Paragraph description of the show/movie. | No | As her father nears the end of his life, filmm... |


## Merged Dataset Dictionary

| **Field Name**        | **Data Type**            | **Attribute Type**         | **Description**                                                                 | **Missing Values** | **Example** |
|----------------------|------------------------|---------------------------|-----------------------------------------------------------------------------|-------------------|-------------|
| title               | String                 | Nominal                   | Title of the media.                                                        | No                | Ganglands   |
| description_x       | String                 | Nominal                   | Brief description of the media (Netflix Movies and Shows dataset).         | No                | To protect his family from a powerful drug lord, skilled thief Mehdi and his expert team of robbers are pulled into a violent and deadly turf war. |
| release_year        | Int                    | Interval, Discrete        | Year the movie was initially released.                                     | No                | 2021        |
| runtime             | Int                    | Interval, Discrete        | Runtime for the movie or for a single episode if the media is a show.      | No                | 46          |
| imdb_id             | String                 | Ordinal                   | IMDb score ID.                                                             | No                | tt13278100  |
| imdb_score          | Float                  | Interval, Continuous      | IMDb score of the media.                                                   | No                | 7.0         |
| imdb_votes          | Int                    | Ratio, Discrete           | Number of IMDb votes for the media.                                        | No                | 2460        |
| show_id             | String                 | Ordinal                   | Unique ID for the show/movie. Primary key for this dataset.                | No                | s3          |
| type                | String                 | Nominal                   | Either "SHOW" or "MOVIE" defining the media type.                          | No                | SHOW        |
| director            | String                 | Nominal                   | Director name.                                                             | Yes               | Julien Leclercq |
| cast                | String                 | Nominal                   | List of actor names cast in the movie.                                     | No                | Sami Bouajila, Tracy Gotoas, Samuel Jouy, etc. |
| country             | String                 | Nominal                   | Country of production.                                                     | No                | United States |
| date_added          | String                 | Interval                  | Date the media was added to Netflix.                                       | No                | 2021-09-07  |
| age_certification   | String                 | Ordinal                   | Content rating.                                                            | No                | TV-MA       |
| num_releases        | Int                    | Ratio, Discrete           | Number of releases (seasons for shows, 1 for movies).                      | No                | 2           |
| listed_in           | String                 | Nominal                   | Genres that the media is listed in.                                        | No                | Crime TV Shows, International TV Shows, TV Action & Adventure |
| description_y       | String                 | Nominal                   | Brief description from the Netflix IMDb Scores dataset.                    | No                | Mehdi, a qualified robber, and Liana, an apprentice thief, get involved in a turf war between drug dealers, and have to collaborate in order to save their loved ones. |
| num_listed_in       | Int                    | Ratio, Discrete           | Number of genres the entry is in.                                          | No                | 3           |
| first_cast          | String                 | Nominal                   | The first listed cast member (most popular).                               | No                | Graham Chapman |
| cast_freq_mean      | Float                  | Interval, Continuous      | Average frequency of actors in other films (popularity measure).           | No                | 10.888889   |
| genre_freq_mean     | Float                  | Interval, Continuous      | Average frequency of genres that this movie is associated with.            | No                | 831         |
| desc_character_count     | Int                 | Nominal      | Number of characters in the description            | No                | 500         |
| desc_word_count      | Int                  |Nominal    |Number of words in description            | No                | 250       |
| twoWord      |Boolean                |Nominal    |If description contains two or more of the top 50 most common words in descriptions          | No                | True    |
| threeWord      |Boolean                |Nominal    |If description contains three or more of the top 50 most common words in descriptions          | No                | True    |
| fourWord      |Boolean                |Nominal    |If description contains four or more of the top 50 most common words in descriptions          | No                | True    |
