There are basically **three** types of recommender systems:-

**Demographic Filtering** - They offer generalized recommendations to every user, based on movie popularity and/or genre. The System recommends the same movies to users with similar demographic features. Since each user is different , this approach is considered to be too simple. The basic idea behind this system is that movies that are more popular and critically acclaimed will have a higher probability of being liked by the average audience.

**Content Based Filtering** - They suggest similar items based on a particular item. This system uses item metadata, such as genre, director, description, actors, etc. for movies, to make these recommendations. The general idea behind these recommender systems is that if a person liked a particular item, he or she will also like an item that is similar to it.

**Collaborative Filtering** - This system matches persons with similar interests and provides recommendations based on this matching. Collaborative filters do not require item metadata like its content-based counterparts.

In this repository I have made three python kernels explaining and implementing the different types of movie recommender systems.

A webapp built using streamlit to display movie recommendation based on content based filtering using cosine similarity. 

- It gives recommendations based on movie content.
- One can give the movie title or director's name to get appropriate movie recommendations.


After preprocessing the datasets I decided to keep these columns in order to proceed further

| Column | Description |
| --- | --- |
| Movie ID | Unique ID for identification of movie and fetch appropriate poster for the same |
| Title| Title was used to get recommendations |
| Tags | Tags column was made using 'Overview','Cast','Genres','Keywords','Crew'|
| crew | Kept it to fetch recommendations based on Directors |

## Built With

* Python 3.10
* nltk.stem.porter
* CountVectorizer
* cosine_similarity


https://user-images.githubusercontent.com/60546202/161950725-29351f71-2dd9-4c10-a112-4ebe3c92d29c.mp4


## Similarity Score : 

   How does it decide which item is most similar to the item user likes? Here come the similarity scores.
   
   It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.
   
## How Cosine Similarity works?
  Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.
  
  ![image](https://user-images.githubusercontent.com/36665975/70401457-a7530680-1a55-11ea-9158-97d4e8515ca4.png)

  
More about Cosine Similarity : [Understanding the Math behind Cosine Similarity](https://www.machinelearningplus.com/nlp/cosine-similarity/)


## How to run the project

1. Clone this repository to your local machine.
2. Install all the libraries mentioned in the [requirements.txt](https://github.com/santanukumar666/Movie-Recommendations-System/blob/main/requirements.txt) file with the command `pip install -r requirements.txt`
3. Open your terminal/command prompt from your project directory and run the file `app.py` by executing the command `streamlit run app.py`.

## What I plan to do next

- Make some changes in the UI and also shift it to flask webapp.
- Improve my predictions and also implement collabrative,demographic and hybrid filtering based recommendations.

Datasets - [The Movie Dataset](https://www.kaggle.com/rounakbanik/the-movies-dataset) , [TMDB Movie Dataset](https://www.kaggle.com/tmdb/tmdb-movie-metadata)
