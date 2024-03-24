#### COMP4010 - DATA VISUALISATION


## Project Proposal: Analyzing Taylor Swift's Discography


Prepared by Group A  
- Nguyen Trong Nhan SIS ID: V202000224  
- Hoang Khoi Nguyen SIS ID: V202000222  
- Nguyen Duy Minh SIS ID: V202000205  

Under the supervision of  
**Professor Le Duy Dung**  

Date: March 12th, 2024  

---

### Dataset description
The selected dataset comprises comprehensive data on Taylor Swift's discography, including three subsets: `taylor_album_songs`, `taylor_all_songs`, and `taylor_albums`. These subsets provide a detailed look at Taylor Swift's studio albums, EPs, singles, and re-releases, covering audio features, album release dates, Metacritic scores, and user scores. This dataset originates from the Genius lyrics database and Spotify's API, offering a rich field for exploring the relationship between musical elements and album reception. Dataset link [here](https://tinyurl.com/yc2axk9f).

### Data Dictionary

# `taylor_album_songs.csv`

|variable            |class     |description         |
|:-------------------|:---------|:-------------------|
|album_name          |character |Album name         |
|ep                  |logical   |Is it an EP                  |
|album_release       |double    |Album release date       |
|track_number        |integer   |Track number        |
|track_name          |character |Track name          |
|artist              |character |Artists             |
|featuring           |character |Artists featured           |
|bonus_track         |logical   |Is it a bonus track         |
|promotional_release |double    |Date of promotional release |
|single_release      |double    |Date of single release      |
|track_release       |double    |Date of track release       |
|danceability        |double    |Spotify danceability score. A value of 0.0 is least danceable and 1.0 is most danceable.        |
|energy              |double    |Spotify energy score. Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity.        |
|key                 |integer   |The key the track is in.                 |
|loudness            |double    |Spotify loudness score. The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track.        |
|mode                |integer   |Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.               |
|speechiness         |double    |Spotify speechiness score. Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.          |
|acousticness        |double    |Spotify acousticness score. A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.        |
|instrumentalness    |double    |Spotify instrumentalness score. Predicts whether a track contains no vocals. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.   |
|liveness            |double    |Spotify liveness score. Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.            |
|valence             |double    |Spotify valence score. A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).             |
|tempo               |double    |The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.          |
|time_signature      |integer   |An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".     |
|duration_ms         |integer   |The duration of the track in milliseconds.       |
|explicit            |logical   |Does the track have explicit lyrics.           |
|key_name            |character |The key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1.         |
|mode_name           |character |Modality of the track.           |
|key_mode            |character |The key of the track.       |
|lyrics              |list      |Track lyrics. These values are all NA. To get the lyrics in nested tibbles, `install.packages("taylor")` and use the source data.|

# `taylor_all_songs.csv`

|variable            |class     |description         |
|:-------------------|:---------|:-------------------|
|album_name          |character |Album name         |
|ep                  |logical   |Is it an EP                  |
|album_release       |double    |Album release date       |
|track_number        |integer   |Track number        |
|track_name          |character |Track name          |
|artist              |character |Artists             |
|featuring           |character |Artists featured           |
|bonus_track         |logical   |Is it a bonus track         |
|promotional_release |double    |Date of promotional release |
|single_release      |double    |Date of single release      |
|track_release       |double    |Date of track release       |
|danceability        |double    |Spotify danceability score. A value of 0.0 is least danceable and 1.0 is most danceable.        |
|energy              |double    |Spotify energy score. Energy is a measure from 0.0 to 1.0 and represents a perceptual measure of intensity and activity.        |
|key                 |integer   |The key the track is in.                 |
|loudness            |double    |Spotify loudness score. The overall loudness of a track in decibels (dB). Loudness values are averaged across the entire track.        |
|mode                |integer   |Mode indicates the modality (major or minor) of a track, the type of scale from which its melodic content is derived. Major is represented by 1 and minor is 0.               |
|speechiness         |double    |Spotify speechiness score. Speechiness detects the presence of spoken words in a track. The more exclusively speech-like the recording (e.g. talk show, audio book, poetry), the closer to 1.0 the attribute value.          |
|acousticness        |double    |Spotify acousticness score. A confidence measure from 0.0 to 1.0 of whether the track is acoustic. 1.0 represents high confidence the track is acoustic.        |
|instrumentalness    |double    |Spotify instrumentalness score. Predicts whether a track contains no vocals. The closer the instrumentalness value is to 1.0, the greater likelihood the track contains no vocal content. Values above 0.5 are intended to represent instrumental tracks, but confidence is higher as the value approaches 1.0.   |
|liveness            |double    |Spotify liveness score. Detects the presence of an audience in the recording. Higher liveness values represent an increased probability that the track was performed live. A value above 0.8 provides strong likelihood that the track is live.            |
|valence             |double    |Spotify valence score. A measure from 0.0 to 1.0 describing the musical positiveness conveyed by a track. Tracks with high valence sound more positive (e.g. happy, cheerful, euphoric), while tracks with low valence sound more negative (e.g. sad, depressed, angry).             |
|tempo               |double    |The overall estimated tempo of a track in beats per minute (BPM). In musical terminology, tempo is the speed or pace of a given piece and derives directly from the average beat duration.          |
|time_signature      |integer   |An estimated time signature. The time signature (meter) is a notational convention to specify how many beats are in each bar (or measure). The time signature ranges from 3 to 7 indicating time signatures of "3/4", to "7/4".     |
|duration_ms         |integer   |The duration of the track in milliseconds.       |
|explicit            |logical   |Does the track have explicit lyrics.           |
|key_name            |character |The key the track is in. Integers map to pitches using standard Pitch Class notation. E.g. 0 = C, 1 = C♯/D♭, 2 = D, and so on. If no key was detected, the value is -1.         |
|mode_name           |character |Modality of the track.           |
|key_mode            |character |The key of the track.       |
|lyrics              |list      |Track lyrics. These values are all NA. To get the lyrics in nested tibbles, `install.packages("taylor")` and use the source data.|

# `taylor_albums.csv`

|variable         |class     |description      |
|:----------------|:---------|:----------------|
|album_name       |character |Album name      |
|ep               |logical   |Is it an EP       |
|album_release    |double    |Album release date    |
|metacritic_score |integer   |Metacritic score |
|user_score       |double    |User score       |


### Reasons to choose the dataset
Taylor Swift has revolutionized the music industry with her timeless and relatable songwriting, winning numerous prestigious prizes and becoming one of our time's most influential and beloved artists. In light of this, we hope that analyzing a dataset about Taylor Swift's songs can provide valuable insights into the strategies behind her success. The dataset offers comprehensive features related to her albums and songs, so we expect to unveil interesting undiscovered patterns that contribute to her widespread appeal. This knowledge can provide valuable lessons in music production, marketing, and cultural impact, which benefits aspiring artists and music industry professionals.

### Questions for analysis
1. **How do audio features such as `danceability`, `energy`, `valence`, and `tempo` correlate with Taylor Swift's albums' critical and public reception?** This question seeks to uncover how the aforementioned audio features correlate with the critical and public reception of Taylor Swift's albums, as indicated by Metacritic scores and user scores. It aims to identify trends that may influence an album's success.
2. **How has Taylor Swift’s musical style evolved over her career?** By examining the changes in audio features (such as `acousticness`, `instrumentalness`, and `tempo`) and lyrical themes across different albums and time periods, we can analyze trends and shifts in her musical style. For instance, we could investigate how her switch from country to pop (and beyond) is reflected in her music's audio characteristics and how this transition has influenced her artistic identity.

### **Analysis plan:**
- **Data Preparation and Cleaning**: Begin by merging and cleaning the relevant datasets to ensure data quality and compatibility for analysis. This includes handling missing values and standardizing formats.
- **Variables**:  
    - Question 1: `danceability`, `energy`, `key`, `loudness`, `mode`, `speechiness`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`, `time_signature`, `explicit`, `metacritic_score`, `user_score`.
        - `metacritic_score` and `user_score` are taken from metacritic (they represent the official and user-given scores respectively) and are only available for albums. Since we mainly want to look at albums' performance, we intend to drop singles that are not part of any album (the dataset already has a version only with singles that are part of an album, taylor_album_songs).
        - We can derive an album's audio characteristics by aggregating the corresponding features of its singles. Ideally, comparisons should be drawn between multiple aggregations (e.g. mean vs median). For values with large ranges/outliers, it's possible to explore splitting an album's songs into clusters and comparing them.
    - Question 2: `danceability`, `energy`, `key`, `loudness`, `mode`, `speechiness`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`, `time_signature`, `explicit`, `album_release`, `single_release`, `track_release`.
    - By combining features with high correlation (found through the use of a correlation matrix), it is possible to create compound features to simplify visualization. A more ambitious method would be to use a dimensionality reduction technique such as PCA. 
- **Toolset**: The project will primarily use `R` for data manipulation and analysis, focusing strongly on the tidyverse suite for data processing and `ggplot2` for creating visualizations. Taylor Swift-inspired color palettes will maintain thematic consistency and enhance visual appeal.
- **Intended visual elements**:
- **Interpretation and Conclusion**: The final phase will involve interpreting the results to conclude the musical characteristics that correlate with album success and the impact of explicit content on song popularity. This will include a discussion of potential implications for music production and marketing strategies.
