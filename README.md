# Music-recommendation-system-using-API
The Music Recommendation System is designed to provide personalized music recommendations by leveraging the Spotify Web API. This system integrates various aspects of music data, such as track details, artist information, and audio features, to suggest songs that closely match the musical taste indicated by a user’s selected track. The recommendation process combines content-based filtering with a weighted popularity score to enhance the relevance and appeal of the suggested tracks.

**Key Components**
1.Authentication with Spotify API

2.The system requires authentication with the Spotify Web API using OAuth. This involves encoding the client ID and client secret into a base64 format and obtaining an access token. This token is essential for making authenticated requests to Spotify’s endpoints.

3.Data Retrieval:
The system extracts data from a Spotify playlist, including track name, artists, album name, and other metadata. Additionally, it retrieves audio features for each track, such as danceability, energy, key, loudness, mode, speechiness, acousticness, instrumentalness, liveness, valence, and tempo. These features are critical for content-based filtering.
Content-Based Filtering:

4.This technique involves analyzing the audio features of the input song and comparing them with the features of other songs in the dataset. By calculating the cosine similarity between the feature vectors, the system identifies tracks with similar characteristics, thus offering recommendations that align with the user's musical preferences.
Popularity Score Calculation:

5.To account for the general appeal and recognition of songs, the system incorporates a popularity score. This score is adjusted based on the song's release date, acknowledging that newer songs might naturally have a different popularity trajectory compared to older ones.

**Hybrid Recommendation Engine:**
1.The core of the recommendation system is its hybrid nature. It merges the results from content-based filtering with the adjusted popularity scores to generate a final list of recommendations. This combination ensures that the suggestions are not only musically similar but also popular and potentially more engaging for the user.

**User Interaction:**
Users interact with the system by providing the name of a song they like. The system then processes this input and outputs a list of recommended tracks. The recommendations include detailed information about each track, such as the track name, artists, album, release date, and a popularity score.

**Example Workflow**

User Input:
The user inputs the name of a song, for example, "Aise Kyun".
Data Processing

The system fetches the necessary data for the input song and compares it with other songs in the dataset using the content-based filtering technique.

**Recommendation Output:**
The system outputs a list of songs that are similar to the input song, ordered by a combination of content similarity and popularity. The result is a curated list of recommendations that are likely to appeal to the user's tastes.

**Use Cases**
1.Music Discovery: Ideal for users looking to explore new music similar to their favorite tracks.
2.Personalized Playlists: Can be used by music streaming services to generate personalized playlists for users.
3.Music Analytics: Useful for analyzing trends in music preferences and identifying popular songs based on various audio features.

This detailed description outlines the comprehensive approach taken by the Music Recommendation System to provide accurate and engaging music suggestions, leveraging advanced data retrieval and machine learning techniques.

**Features**
1.Access Token Generation: The system generates an access token using Spotify API credentials.
2.Playlist Data Extraction: Fetches and extracts data from Spotify playlists, including track name, artists, album name, release date, and popularity.
3.Content-Based Filtering: Provides recommendations based on the similarity of musical features.
4.Popularity-Based Recommendations: Weights recommendations based on the popularity of the songs.
5.Hybrid Recommendations: Combines content-based and popularity-based methods for a comprehensive recommendation system.


**API Details**

Spotify API: The system uses Spotify's Web API to fetch track information and audio features.
