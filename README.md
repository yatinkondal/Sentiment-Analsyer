
# 😊😐😠 Sentiment Analyser

A simple Python project that reads customer sentences from a CSV file, labels each one as **Positive**, **Negative** or **Neutral**, saves the result to Excel, and builds a **Word Cloud** of the most common words in the negative feedback.

## ✨ Features

- Loads a dataset of sentences from a CSV file
- Finds the feeling of each sentence using **TextBlob** (polarity score)
- Adds a new `Sentiment` column to the table
- Saves the final table as an Excel file
- Filters only the **negative** sentences
- Creates a **Word Cloud** to show the most used words in negative feedback

## 🛠️ Built With

| Library | Use |
|---------|-----|
| `pandas` | Reads the CSV, filters rows, saves to Excel |
| `textblob` | Finds the sentiment (polarity) of each sentence |
| `wordcloud` | Creates the word cloud picture |
| `matplotlib` | Displays the word cloud |
| `openpyxl` | Lets pandas write `.xlsx` files |
| `seaborn` | Imported for future charts |

## 🚀 How to Run

1. Install Python 3 and Jupyter Notebook.
2. Install the libraries:
   ```bash
   pip install pandas matplotlib seaborn wordcloud textblob openpyxl
   ```
3. Keep the dataset file `Sentiment_Analysis .csv` in the same folder as the notebook. It needs one column named `Sentences`.
4. Open the notebook and run all the cells from top to bottom.

## 🧠 How It Works

1. Load the CSV file into a pandas DataFrame.
2. For every sentence, TextBlob gives a **polarity** score from -1 to +1.
   - Above 0 → **Positive**
   - Below 0 → **Negative**
   - Exactly 0 → **Neutral**
3. Save all sentences with their sentiment to `SentimentAnalysisbyYatin.xlsx`.
4. Keep only the negative sentences and join them into one paragraph.
5. Generate a Word Cloud where common words look bigger.

## 📊 Sample Result

| Sentence | Sentiment |
|----------|-----------|
| The product's exceptional quality and performa... | Positive |
| Poor customer support and the product's subpar... | Negative |
| Outstanding customer service accompanied the p... | Positive |

In the word cloud, the biggest words were **purchase, product, frustration, service, customer** and **regret**. This shows that unhappy customers mostly complain about product quality and customer support.

## ⚠️ Limitations

- TextBlob works only for English.
- It judges by words, so average sentences like "The service was average, meeting minimum requirements" can be wrongly marked Negative.
- It cannot understand sarcasm.

## 🔮 Future Ideas

- Bar or pie chart of Positive, Negative and Neutral counts
- Word cloud for positive sentences too
- Remove common stop words from the word cloud
- Try better models like VADER or BERT
- Small app where the user types a sentence and gets its sentiment

## 📄 License

This project is for learning purposes.
