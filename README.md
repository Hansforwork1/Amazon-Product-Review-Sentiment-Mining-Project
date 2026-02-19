# Amazon Reviews Sentiment Analysis 🛍️📊

This is a project for sentiment analysis of Amazon product reviews using Python.
It utilizes Natural Language Processing (NLP) techniques to deeply analyze customer reviews, aiming to identify sentiment tendencies (Positive, Negative, Neutral) and explore the relationships between review length, rating distribution, and time trends.

## 🎯 Project Goals

- **Sentiment Identification**: Automatically determine the sentiment polarity of customer reviews.
- **Trend Analysis**: Observe changes in reviews over different time periods.
- **Rating Correlation**: Analyze the relationship between review length and ratings.
- **Keyword Extraction**: Identify important information in reviews (via preprocessing).

## 🛠️ Technologies & Libraries

This project uses the following Python libraries:

- **[Pandas](https://pandas.pydata.org/)**: For data manipulation and analysis.
- **[NLTK (Natural Language Toolkit)](https://www.nltk.org/)**: For text preprocessing (removing stopwords).
- **[TextBlob](https://textblob.readthedocs.io/en/dev/)**: For sentiment analysis (calculating Polarity and Subjectivity).
- **[Matplotlib](https://matplotlib.org/)**: For plotting data charts (plotting logic included in the code).

## ⚙️ Installation Guide

Please ensure your environment has Python 3.x installed, and run the following command to install the required packages:

```bash
pip install pandas nltk textblob matplotlib
```

Additionally, you need to download the NLTK stopwords database:

```python
import nltk
nltk.download('stopwords')
```

## 🚀 Usage

1. **Prepare Data**: Ensure the `Amazon_Reviews.csv` file is in the directory.
2. **Run Script**:
   
   ```bash
   python amazon_reviews.py
   ```

3. **Process Flow**:
   - **Load Data**: Loads the CSV file with basic error handling.
   - **Data Cleaning**: Removes duplicates, missing values, and filters out HTML tags, URLs, and punctuation.
   - **Sentiment Calculation**: Uses `TextBlob` to calculate a sentiment score (-1 to 1) for each review.
   - **Result Output**: After execution, a new CSV file `Amazon_Reviews_with_Sentiment.csv` will be generated.

## 📊 Output File Description

The generated `Amazon_Reviews_with_Sentiment.csv` will contain the original data plus the following new columns:

| Column Name | Description |
| :--- | :--- |
| `sentiment_score` | Sentiment polarity score, ranging from -1 (Extremely Negative) to 1 (Extremely Positive). |
| `sentiment_label` | Sentiment label classification: **Positive** (> 0.1), **Negative** (< -0.1), **Neutral** (Others). |

## ⚠️ Notes

- This code originated from a Google Colab environment. If running locally, please note that `google.colab` related import statements may need to be removed or commented out.
- The `on_bad_lines='warn'` parameter is used during raw data reading to skip malformed lines.

---
*Created by Tzu Heng Su*
