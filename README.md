# BookBuddy - A Book Recommendation System
BookBuddy is a book recommedation system built using jupyter notebook. It uses Flask API to connect to a Dialogflow chatbot interface.

Chatbot Web Demo: 
https://bot.dialogflow.com/91473327-4242-4820-ae3a-663174a2071e
## About
BookBuddy is a book recommendation system powered by a chatbot. The user can ask the chatbot for recommendations based on a book they prefer or a book they've recently read. Based on the book name and knowledge about the book's summary, the chatbot recommends the top 3 or 4 books which are similar in context to the user preference.
The book summary is retrieved from the dataset and the similar books are recommended through clustering and cosine similarity computation. The books with the highest cosine similarities are the top recommended books.

## Features

- Input book preferences to chatbot
- Get 3 or 4 book recommendations based on preferred book

## Usage

Clone the following github repository [Book-Recommender-System](https://github.com/HadyKh/Book-Recommender-System.git).

The repository includes the jupyter notebook and the book summary dataset used.

```sh
git clone https://github.com/HadyKh/Book-Recommender-System.git
```

The following python package needs to be installed:

```sh
pip install Flask
```
Run the notebook.

Install [Ngrok](https://ngrok.com/). Ngrok will provide a public URL on which the POST requests from the Dialogflow chatbot will be sent and received. Run the ngrok app and create a connection tunnel:

```sh
ngrok http 5000
```

The ngrok link generated is then used in the fulfillment tab in Dialogflow to connect the chatbot to the backend system.