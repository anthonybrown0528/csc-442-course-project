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

