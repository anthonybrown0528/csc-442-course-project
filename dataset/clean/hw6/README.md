## Merged Dataset Dictionary

| **Field Name**        | **Data Type**            | **Attribute Type**         | **Description**                                                                 | **Missing Values** | **Example** |
|----------------------|------------------------|---------------------------|-----------------------------------------------------------------------------|-------------------|-------------|
| title               | String                 | Nominal                   | Title of the media.                                                        | No                | Ganglands   |
| description_x       | String                 | Nominal                   | Lemmatized description of the media with some text encoding errors removed (Netflix Movies and Shows dataset).         | No                | King Arthur accompany squire recruit Knights Round Table include Sir Bedevere Wise Sir Lancelot Brave Sir Robin Not-Quite-So-Brave-As-Sir-Lancelot Sir Galahad Pure On way Arthur battle Black Knight despite limb chop insist still fight They reach Camelot Arthur decide enter silly place |
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
