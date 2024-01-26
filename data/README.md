# About the data
We've brought here some initial data to get you started for convinience. Check out the originals in Kaggle if you like:

* [Movie Dialog Corpus](https://www.kaggle.com/datasets/Cornell-University/movie-dialog-corpus)
* [IMDB Movies Dataset](https://www.kaggle.com/datasets/harshitshankhdhar/imdb-dataset-of-top-1000-movies-and-tv-shows?select=imdb_top_1000.csv)

Our recommendation would be to keep an 'additional' and 'processed' folders here as well, but it'll be up to how you want to manage the dependency between groups.

## Movie Dialog Corpus
This corpus comes from the paper, "Chameleons in imagined conversations: A new approach to understanding coordination of linguistic style in dialogs" by Cristian Danescu-Niculescu-Mizil and Lillian Lee.

The paper and up-to-date data can be found here: http://www.cs.cornell.edu/~cristian/Cornell_Movie-Dialogs_Corpus.html

This corpus contains a metadata-rich collection of fictional conversations extracted from raw movie scripts:

* 220,579 conversational exchanges between 10,292 pairs of movie characters
* involves 9,035 characters from 617 movies
* in total 304,713 utterances
* movie metadata included:
  * genres
  * release year
  * IMDB rating
  * number of IMDB votes
  * IMDB rating
* character metadata included:
  * gender (for 3,774 characters)
  * position on movie credits (3,321 characters)

### Content
In all files the original field separator was " +++$+++ " and have been converted to tabs (\t). Additionally, the original file encoding was ISO-8859-2. It's possible that the field separator conversion and decoding may have left some artifacts.

* 'movie_titles_metadata.txt' contains information about each movie title
  * movieID,
  * movie title,
  * movie year,
  * IMDB rating,
  * no. IMDB votes,
  * genres in the format ['genre1','genre2',É,'genreN']

* 'movie_characters_metadata.txt' contains information about each movie character
  * characterID
  * character name
  * movieID
  * movie title
  * gender ("?" for unlabeled cases)
  * position in credits ("?" for unlabeled cases)

* 'movie_lines.txt' contains the actual text of each utterance
  * lineID
  * characterID (who uttered this phrase)
  * movieID
  * character name
  * text of the utterance

* movie_conversations.txt the structure of the conversations
  * characterID of the first character involved in the conversation
  * characterID of the second character involved in the conversation
  * movieID of the movie in which the conversation occurred
  * list of the utterances that make the conversation, in chronological order: ['lineID1','lineID2',É,'lineIDN'] has to be matched with movie_lines.txt to reconstruct the actual content

* raw_script_urls.txt the urls from which the raw sources were retrieved

---

## IMDB Movies Dataset
IMDB Dataset of top 1000 movies and tv shows.

### Content
* **Poster_Link:** Link of the poster that imdb using
* **Series_Title:** Name of the movie
* **Released_Year:** Year at which that movie released
* **Certificate:** Certificate earned by that movie
* **Runtime:** Total runtime of the movie
* **Genre:** Genre of the movie
* **IMDB_Rating:** Rating of the movie at IMDB site
* **Overview:** mini story/ summary
* **Meta_score:** Score earned by the movie
* **Director:** Name of the Director
* **Star1,Star2,Star3,Star4:** Name of the Stars
* **No_of_votes:** Total number of votes
* **Gross:** Money earned by that movie