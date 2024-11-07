# Spotify 2023 Data Analysis by Marc Wilson Flores from 2ECE-C
## Problem
In this program, I was tasked to create an extensive data analysis on the top charts of Spotify 2023

Here are the guide questions set to help analyze the dataset:

### **Overview of Dataset**

_-How many rows and columns does the dataset contain?_

The dataset contained 953 rows and 23 columns.

_-What are the data types of each column? Are there any missing values?_

The columns track_name,artist(s)_name,key, and mode are strings, while the rest of the dataset are integers. Yes, there are many missing values because the dataset has unique letters that could not be displayed and instead appear as NaN.

### **Basic Descriptive Statistics**

_-What are the mean, median, and standard deviation of the streams column?_

The mean, median, and standard deviation of the stream column are as follows:

Mean = 514137424.93907565

Median = 290530915.0

Standard Deviation = 566856949.03

_-What is the distribution of released_year and artist_count? Are there any noticeable trends or outliers?_

The year with the most releases is 2022. The artist count was noticeably low.

### **Top Performers**

_-Which track has the highest number of streams? Display the top 5 most streamed tracks._

The 5 tracks with the highest number of streams are Blinding Lights, Shape of You, Someone You Loved, Dance Monkey, Sunflower - Spider-Man: Into the Spider-Verse.

_-Who are the top 5 most frequent artists based on the number of tracks in the dataset?_

The top 5 frequent artists are Taylor Swift, The Weeknd, Bad Bunny, SZA, and Harry Styles.

 ### **Temporal Trends**

_-Analyze the trends in the number of tracks released over time. Plot the number of tracks released per year._

There was a steady increase of tracks released each year, decreasing in 2018 but spiking in 2022 and decreasing again in 2023.

_-Does the number of tracks released per month follow any noticeable patterns? Which month sees the most releases?_

Yes, the month with the most releases per year is January.

 ### **Genre and Music Characteristics**

_-Examine the correlation between streams and musical attributes like bpm, danceability_%, and energy_%. Which attributes seem to influence streams the most?_

The attribute of danceability_% seems to influence streams the most.

_-Is there a correlation between danceability_% and energy_%? How about valence_% and acousticness_%?_

Yes, there seems to be a correlation between danceability and energy, while valence and acousticness have little correlation
 
### **Platform Popularity**

_-How do the numbers of tracks in spotify_playlists, spotify_charts, and apple_playlists compare? Which platform seems to favor the most popular tracks?_

The number of tracks of spotify_charts and apple_playlists could not be compared to the overwhelmingly large number of tracks that spotify_playlists, which seems to favor the most popular tracks.

 ### **Advanced Analysis**

_-Based on the streams data, can you identify any patterns among tracks with the same key or mode (Major vs. Minor)?_

Yes, the mode would be major across all keys.

_-Do certain genres or artists consistently appear in more playlists or charts? Perform an analysis to compare the most frequently appearing artists in playlists or charts._

The most frequent artists that appear are The Weeknd, Taylor Swift, Ed Sheeran, Harry Styles, Eminem, Artic Monkeys, Coldplay, Avicii, Dr. Dre, Snoop Dogg, and Adele.

## Background

At the beginning of coding the program, I stumbled into a problem as the code would not import the .csv file due to the unique characters used in the dataset. I found a way to fix the error by adding the line "encoding='latin-1'" to the end of my code, as it
tells the program to use latin-1 character encoding when reading the .csv file.

After that, I consulted my notes as my memory of pandas was a bit rusty. I found the right functions to use but encountered another problem. There was an error when trying to read the dataset, and I had to use 
df['streams'] = pd.to_numeric(df['streams'], errors='coerce') so that it would read the unique characters. I used this line of code whenever the same problem appeared on the other parts of the program.

Aside from the aforementioned problems, it was smooth sailing as I had the internet to help me code the program, especially when dealing with the graphs, as I had difficulty setting up each one. In the end, I was able to achieve the intended output of the program
which helped me to answer the guide questions posted above.
