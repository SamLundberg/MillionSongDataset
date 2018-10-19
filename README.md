# ![](https://labrosa.ee.columbia.edu/millionsong/sites/default/files/millionsong2-128.jpg)&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;The Million Song Dataset

## Can the genre of a song be predicted based off of a few audio features? What if more artist-based features are included?

## Can a song be identified as hot or not off of the same set of variables?

Using a 10,000 song sample, from the Million Song Dataset (https://labrosa.ee.columbia.edu/millionsong/), these questions will attempt to be answered.

This dataset contains a million songs from 1922-2011, with artist tagged information from Echonest (now part of Spotify), along with audio measurements, and other relevant information.

### Citation:
Thierry Bertin-Mahieux, Daniel P.W. Ellis, Brian Whitman, and Paul Lamere.
The Million Song Dataset. In Proceedings of the 12th International Society
for Music Information Retrieval Conference (ISMIR 2011), 2011.

## In this repository you will find:
-The extraction of HDF5 source files and some initial EDA:<br/>
  [01_Extract_HDF5_Files_to_a_CSV_File.ipynb](https://github.com/SamLundberg/MillionSongDataset/blob/master/01_Extract_HDF5_Files_to_a_CSV_File.ipynb)

-Web-scraping the Billboard Top 100 charts from 1958-2011, to determine if a song was popular or not:<br/>
  [02_Scrape_Billboard_top_100.ipynb](https://github.com/SamLundberg/MillionSongDataset/blob/master/02_Scrape_Billboard_top_100.ipynb)

-Exploratory Data Analysis:<br/>
  [03_EDA.ipynb](https://github.com/SamLundberg/MillionSongDataset/blob/master/03_EDA.ipynb)

-Predicting if a song is hot/popular or not using information from the Billboard Top 100 charts:<br/>
  [04_Predict_Hot_Billboard Songs.ipynb](https://github.com/SamLundberg/MillionSongDataset/blob/master/04_Predict_Hot_Billboard_Songs.ipynb)

-Predicting if a genre can be found with audio features:<br/>
  [05_Genre_Identification.ipynb](https://github.com/SamLundberg/MillionSongDataset/blob/master/05_Genre_Identification.ipynb)

An Executive Summary is included in the Documents folder:<br/>
  [Summary](https://github.com/SamLundberg/MillionSongDataset/blob/master/Documents/Executive_Summary.md)

Below is a dictionary of audio terms and columns that are found in the 10k dataset file, for reference:<br/>

| ﻿Field name                  | Description                                  |
|-----------------------------|----------------------------------------------|
| artist familiarity          | algorithmic estimation                       |
| artist hotttnesss           | algorithmic estimation                       |
| artist id                   | Echo Nest ID                                 |
| artist latitude             | latitude                                     |
| artist location             | location name                                |
| artist longitude            | longitude                                    |
| artist name                 | artist name                                  |
| artist terms                | Echo Nest tags (genre classification)        |
| artist terms freq           | Echo Nest tags freqs (how often it shows up) |
| artist terms weight         | Echo Nest tags weight (genre weight)         |
| bars start                  | beginning of bars, usually on a beat         |
| beats start                 | result of beat tracking                      |
| duration                    | in seconds                                   |
| end of fade in              | seconds at the beginning of the song         |
| key                         | key the song is in                           |
| loudness                    | overall loudness in dB                       |
| mode                        | major or minor                               |
| release                     | album name                                   |
| sections start              | largest grouping in a song, e.g. verse       |
| segments loudness max       | max dB value                                 |
| segments loudness max time  | time of max dB value, i.e. end of attack     |
| segments loudness max start | dB value at onset                            |
| segments pitches            | chroma feature, one value per note           |
| segments start              | musical events, ~ note onsets                |
| segments timbre             | texture features (MFCC+PCA-like)             |
| song hotttnesss             | algorithmic estimation                       |
| start of fade out           | time in sec                                  |
| tatums start                | smallest rythmic element                     |
| tempo                       | estimated tempo in BPM                       |
| time signature              | estimate of number of beats per bar, e.g. 4  |
| title                       | song title                                   |
| year                        | song release year from MusicBrainz or 0      |


### Please note that the Data folder is not included because of size limitations of the repository
