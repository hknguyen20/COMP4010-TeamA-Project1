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

### Reasons to choose the dataset
Taylor Swift has revolutionized the music industry with her timeless and relatable songwriting, winning numerous prestigious prizes and becoming one of our time's most influential and beloved artists. In light of this, we hope that analyzing a dataset about Taylor Swift's songs can provide valuable insights into the strategies behind her success. The dataset offers comprehensive features related to her albums and songs, so we expect to unveil interesting undiscovered patterns that contribute to her widespread appeal. This knowledge can provide valuable lessons in music production, marketing, and cultural impact, which benefits aspiring artists and music industry professionals.

### Questions for analysis
1. **How do audio features such as `danceability`, `energy`, `valence`, and `tempo` correlate with Taylor Swift's albums' critical and public reception?** This question seeks to uncover how the aforementioned audio features correlate with the critical and public reception of Taylor Swift's albums, as indicated by Metacritic scores and user scores. It aims to identify trends that may influence an album's success.
2. **How has Taylor Swift’s musical style evolved over her career?** By examining the changes in audio features (such as `acousticness`, `instrumentalness`, and `tempo`) and lyrical themes across different albums and time periods, we can analyze trends and shifts in her musical style. For instance, we could investigate how her switch from country to pop (and beyond) is reflected in her music's audio characteristics and how this transition has influenced her artistic identity.

### **Analysis plan:**
- **Data Preparation and Cleaning**: Begin by merging and cleaning the relevant datasets to ensure data quality and compatibility for analysis. This includes handling missing values and standardizing formats.
- **Variables**:  
    - Question 1: `danceability`, `energy`, `key`, `loudness`, `mode`, `speechiness`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`, `time_signature`, `explicit`.
    - Question 2: `danceability`, `energy`, `key`, `loudness`, `mode`, `speechiness`, `acousticness`, `instrumentalness`, `liveness`, `valence`, `tempo`, `time_signature`, `explicit`, `album_release`, `single_release`, `track_release`.
- **Toolset**: The project will primarily use `R` for data manipulation and analysis, focusing strongly on the tidyverse suite for data processing and `ggplot2` for creating visualizations. Taylor Swift-inspired color palettes will maintain thematic consistency and enhance visual appeal.
- **Interpretation and Conclusion**: The final phase will involve interpreting the results to conclude the musical characteristics that correlate with album success and the impact of explicit content on song popularity. This will include a discussion of potential implications for music production and marketing strategies.
