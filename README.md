# -Movie-Recommendation-System-with-Python-and-Machine-Learning
This code is an implementation of a movie recommendation system using content-based filtering. Let's go through the code and its steps:

Data Collection and Pre-Processing:

The code imports the necessary libraries, including numpy, pandas, difflib, TfidfVectorizer, and cosine_similarity.
It loads the movie data from a CSV file into a pandas DataFrame.
The first five rows of the DataFrame are printed.
The shape of the DataFrame (number of rows and columns) is displayed.
The selected features for recommendation are defined, which include 'genres', 'keywords', 'tagline', 'cast', and 'director'.
The selected features are combined into a single column called 'combined_features'.


Converting Text to Feature Vectors:

The code initializes an instance of the TfidfVectorizer class.
It replaces any np.nan values in the 'combined_features' column with an empty string.
The feature vectors are obtained by fitting and transforming the 'combined_features' data using the TfidfVectorizer.


Calculating Similarity Scores:

The cosine similarity scores are computed using the feature vectors obtained in the previous step.


Getting the User's Input:

The code prompts the user to enter their favorite movie name.


Finding Close Matches:

A list of all movie titles from the dataset is created.
The difflib library is used to find the closest match to the movie name entered by the user.
If a close match is found, it is stored in the 'close_match' variable.


Retrieving Similar Movies:

The index of the movie with the closest match is obtained from the DataFrame.
The similarity scores of the movies are retrieved from the cosine similarity matrix.
The similarity scores are sorted in descending order.
The titles of similar movies are printed based on the index.


Movie Recommendation System:

The code prompts the user again to enter their favorite movie name.
The previous steps of finding close matches and retrieving similar movies are executed again.
That's the overall flow of the code. It takes a movie name as input from the user and suggests similar movies based on the content features like genres, keywords, tagline, cast, and director.
