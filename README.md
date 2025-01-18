# Recommending Similar Movies using Collaborative Filtering

This project explores the implementation of a basic movie recommendation system using collaborative filtering in Python. The system leverages user-item interaction data to suggest movies similar to a user's preferred choices. We'll delve into the data processing, exploratory data analysis (EDA), and the core recommendation logic.

**1. Data Acquisition and Preprocessing**

The system utilizes the MovieLens 100K dataset, containing user ratings for movies. The data is loaded into Pandas DataFrames for manipulation. Two key files are used:

Data Contains user ID, movie ID, rating, and timestamp.
Movie_Id_Titles: Maps movie IDs to their corresponding titles.
These DataFrames are merged to associate movie titles with ratings.

**2. Exploratory Data Analysis (EDA)**

EDA is performed to understand data characteristics. Histograms and joint plots visualize the distribution of ratings and the number of ratings per movie. This analysis helps in identifying popular movies and understanding rating patterns.

Key observations from EDA:

Certain movies have significantly more ratings than others.
Average ratings tend to follow a normal distribution.

**3. Building the Recommendation System**

The core of the recommendation system lies in creating a user-item matrix (moviemat). This matrix stores user ratings for each movie, with NaN values representing unrated movies.

The system utilizes the corrwith() method to calculate correlations between user ratings for different movies. This identifies movies with similar rating patterns, suggesting similarity in user preferences.

**4. Recommendation Logic**

To recommend similar movies, the following steps are taken:

Select a target movie (e.g., 'Star Wars (1977)').
Obtain user ratings for the target movie.
Calculate correlations between the target movie's ratings and ratings for other movies using corrwith().
Create a DataFrame containing movie titles and their correlations with the target movie.
Filter out movies with fewer than a specified number of ratings (e.g., 100) to improve recommendation quality.
Sort the DataFrame by correlation in descending order to identify the most similar movies.

**5. Example Recommendations**

The notebook demonstrates recommendations for two movies: 'Star Wars (1977)' and 'Liar Liar (1997)'. The system identifies movies with high correlations, suggesting similarity in user preferences.

**6. Limitations and Future Improvements**

This implementation is a basic recommendation system. It could be enhanced by incorporating more advanced techniques such as:

User-based filtering: Recommending movies based on ratings from similar users.
Matrix factorization: Decomposing the user-item matrix to identify latent factors influencing preferences.
Hybrid approaches: Combining collaborative and content-based filtering for more robust recommendations.

**Conclusion**
This project presented a basic movie recommendation system using collaborative filtering in Python. The system effectively leverages user-item interaction data to identify and recommend similar movies. While this implementation has limitations, it provides a foundation for exploring more advanced recommendation techniques. By incorporating these advancements, the system can be further refined to provide more accurate and personalized recommendations to users. 
