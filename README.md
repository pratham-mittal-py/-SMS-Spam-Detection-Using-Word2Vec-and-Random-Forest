Here is the properly formatted `README.md` content in Markdown format, ready for copy-paste:

```markdown
# SMS Spam Detection Using Word2Vec and Random Forest

This project classifies SMS messages as spam or ham using Word2Vec embeddings and a Random Forest classifier.

## Dataset

- `SMSSpamCollection.txt`: A tab-separated file with two columns — `'label'` (spam/ham) and `'message'` (SMS text).

## Dependencies

- pandas
- numpy
- scikit-learn
- gensim
- nltk
- tqdm

## Setup

1. Install required packages:
   ```bash
   pip install pandas numpy scikit-learn gensim nltk tqdm
   ```

2. Download NLTK data:
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('wordnet')
   ```

## Steps

1. Load and preprocess the SMS dataset.
2. Clean messages by removing non-alphabetic characters, converting to lowercase, and lemmatizing.
3. Tokenize messages into sentences and words using NLTK and Gensim.
4. Train a Word2Vec model on the tokenized corpus.
5. Generate document vectors using average Word2Vec embeddings.
6. Prepare features (X) and labels (y), where labels are encoded as 1 for 'ham' and 0 for 'spam'.
7. Split data into training and testing sets.
8. Train a Random Forest classifier.
9. Evaluate model using accuracy and classification report.

## Usage

After training, the system accepts a new SMS message from the user, preprocesses it identically to the training data, converts it to a Word2Vec average vector, and predicts whether it is spam or ham.

**Input Example:**
```
Enter an SMS message: Congratulations! You've won a free iPhone.
```

**Output Example:**
```
Prediction: spam
```

## Model Performance

- Accuracy and classification metrics are printed after evaluation on the test set.

> Note: Ensure consistent preprocessing between training and prediction.
```