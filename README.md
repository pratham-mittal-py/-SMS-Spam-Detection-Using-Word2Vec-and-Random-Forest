Project: SMS Spam Detection Using Word2Vec and Random Forest

This project classifies SMS messages as spam or ham using Word2Vec embeddings and a Random Forest classifier.

Dataset:

SMSSpamCollection.txt: A tab-separated file with two columns — 'label' (spam/ham) and 'message' (SMS text).
Dependencies:

pandas
numpy
scikit-learn
gensim
nltk
tqdm
Setup:

Install required packages:
pip install pandas numpy scikit-learn gensim nltk tqdm
Download NLTK data:
import nltk
nltk.download('punkt')
nltk.download('wordnet')
Steps:

Load and preprocess the SMS dataset.
Clean messages by removing non-alphabetic characters, converting to lowercase, and lemmatizing.
Tokenize messages into sentences and words using NLTK and Gensim.
Train a Word2Vec model on the tokenized corpus.
Generate document vectors using average Word2Vec embeddings.
Prepare features (X) and labels (y), where labels are encoded as 1 for 'ham' and 0 for 'spam'.
Split data into training and testing sets.
Train a Random Forest classifier.
Evaluate model using accuracy and classification report.
Usage:
After training, the system accepts a new SMS message from the user, preprocesses it identically to the training data, converts it to a Word2Vec average vector, and predicts whether it is spam or ham.

Input Example:
Enter an SMS message: Congratulations! You've won a free iPhone.

Output Example:
Prediction: spam

Model Performance:

Accuracy and classification metrics are printed after evaluation on the test set.
Note:

The Word2Vec model uses min_count=5 and vector_size=100.
Messages with no words in the Word2Vec vocabulary are represented as zero vectors.
Ensure consistent preprocessing between training and prediction.