# LSTM Market Sentiment Analysis

## Summary
This LSTM-based sentiment analysis model processes market-related comments to classify them as positive, negative, or neutral. The model dynamically adjusts based on the number of detected sentiment classes.

## Key Steps in the Code

### Text Preprocessing
- Converts text to lowercase.
- Removes punctuation and numbers.
- Tokenizes words and removes stopwords (in Russian).

### Tokenization & Padding
- Converts words into numerical sequences.
- Ensures all comments have the same length using `pad_sequences()`.

### Building the LSTM Model
- Uses Bidirectional LSTM for better text understanding.
- Includes Dropout layers to prevent overfitting.
- The output layer dynamically adjusts to the number of sentiment classes.

### Training the Model
- Trained for 100 epochs using categorical cross-entropy loss.
- Training accuracy is visualized using matplotlib.

### Model Evaluation
- Confusion Matrix Heatmap is generated for test results.
- A classification report provides precision, recall, and F1-score.

### Sentiment Prediction Function
- Predicts the sentiment of new comments after text processing.

### Example Predictions
- 10 sample comments in Russian with English translations are tested.

## Outcome
- This model automatically classifies market-related comments into sentiment categories.
- It adapts to different sentiment class distributions dynamically.
- Visualization techniques like heatmaps and accuracy curves help in performance evaluation.

## Dataset
The dataset used can be found [here](https://github.com/Mosaad2010-star/lstm-market-sentiment-analysis/blob/main/market_comments.csv).