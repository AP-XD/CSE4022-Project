# YouTube Description Generator: Flask Back-End Repository

## Frontend Demo

![](/readme_images/demo.png)

## Backend Demonstration

![](/readme_images/demonstration.gif)

## Abstract

Nowadays on YouTube, it is not something new to come across a misleading title or a click bait thumbnail. In order to gain views the creators often mislead the audience. The quality, popularity, and relevancy of the results returned by a search query are typically determined using a grading system. Due to more views and likes, a few occasionally bad and irrelevant videos will occasionally rank higher.
As for the previous approaches to these problems most of the existing projects do sentiment analysis on the comments. This does not necessarily clarify if the video is good or not. Also many papers convert video to wav format and then analyze.
Now in our project we directly take the video for analysis instead of comments for accurate results. And instead of converting video to wav format and performing machine learning algorithms which takes lots of space, we directly take transcript and analyze.

## Sending request to our API

The query (or API request) to our backend can be made using following three variables only. They are:

- **`id`** : Video ID of the YouTube Video. Each video has its own unique ID in its URL.\

- **`choice`** : Algorithm Choice for the summarizing the Transcript. There are only six accepted values in this variable.\
  These choices are written along with algorithm names as follows:
  - `gensim-sum` : Text Rank Algorithm Based using Gensim
  - `spacy-sum` : Frequency Based Approach using Spacy.
  - `nltk-sum` : Frequency Based Summarization using NLTK.
  - `sumy-lsa-sum` : Latent Semantic Analysis Based using Sumy.
  - `sumy-luhn-sum` : Luhn Algorithm Based using Sumy.
  - `sumy-text-rank-sum` : Text Rank Algorithm Based using Sumy.
- **`percent`** : The percentage is used to generate the description in approx. `X% lines` of the available transcript.
