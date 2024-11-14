# Sentiment-RoBERTa: An Unsupervised Approach to Sentiment Analysis on App Reviews

This project provides an unsupervised method for sentiment analysis on app reviews from platforms such as Netflix, Facebook, and Spotify. Using pretrained models, **VADER** and **RoBERTa**, this approach captures sentiment trends without requiring labeled data, making it efficient for large-scale text data analysis.

## Project Structure

- **`Sentiment Analysis - RoBERTa.ipynb`**: Jupyter Notebook that contains the code for processing app reviews and conducting sentiment analysis using VADER and RoBERTa models.

## Models Used

1. **VADER (Valence Aware Dictionary and Sentiment Reasoner)**: A rule-based sentiment analysis model specifically tuned for social media and review texts. VADER provides positive, negative, and neutral sentiment scores.
  
2. **RoBERTa (A Robustly Optimized BERT Pretraining Approach)**: A pretrained transformer model fine-tuned for sentiment analysis, capable of capturing contextual nuances in language for more accurate sentiment classification.

## Dataset

The project utilizes app reviews from popular platforms (Netflix, Facebook, and Spotify). Ensure that review data is in the appropriate format for input to the notebook.

## Requirements

To run this project, install the necessary packages by running:

```bash
pip install -r requirements.txt
```

## Usage

1. **Run the Jupyter Notebook**: Open and execute `Sentiment Analysis - RoBERTa.ipynb` to preprocess the data and perform sentiment analysis.

   ```bash
   jupyter notebook "Sentiment Analysis - RoBERTa.ipynb"
   ```

2. **Sentiment Analysis Workflow**:
   - Load app review data into the notebook.
   - Process the text data for compatibility with VADER and RoBERTa.
   - Perform sentiment analysis using each model and compare the results.

## Example

Below is an example code snippet for using the RoBERTa model to analyze sentiments within the notebook:

```python
from transformers import pipeline

# Load pretrained RoBERTa model for sentiment analysis
roberta_sentiment = pipeline("sentiment-analysis", model="roberta-base")

# Example text
review_text = "I absolutely love the new update on Netflix!"

# Perform sentiment analysis
sentiment = roberta_sentiment(review_text)
print(sentiment)
```

## Results

The project outputs sentiment scores for each app review, allowing users to understand overall sentiment trends across different applications. Both models provide insights into the polarity and intensity of user feedback, aiding in feature improvement and user satisfaction analysis.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
