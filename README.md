# Implementation-of-Sentimental-Analysis
The process of sentiment analysis using VADER model can be described as follows:

1.Read the input text: The first step is to read the input text. This can be done using a variety of methods, such as reading a file, receiving input from a user, or scraping text from a website.

2.Clean the text: Once the text has been read, it is important to clean it. This involves removing any punctuation, stop words, or other noise that could interfere with the sentiment analysis process.

3.Calculate the sentiment scores: The next step is to calculate the sentiment scores for the text. This is done by using a sentiment analysis model, such as VADER.

4.Interpret the results: The final step is to interpret the results of the sentiment analysis. This involves understanding the meaning of the sentiment scores and how they relate to the text.

5.VADER is a lexicon- and rule-based sentiment analysis tool that is specifically designed to work with social media text. It is a free and open-source tool that can be used to analyze text in a variety of languages. VADER is a popular choice for sentiment analysis because it is easy to use and produces accurate results.
## Program:
```
### Developed By: Siva Balan S
### Reg.No:212222240100
```
```
import pandas as pd
import vaderSentiment as vs

# Read the Excel file
df = pd.read_excel('output.xlsx')

# Create a VADERSentiment object
analyzer = vs.vaderSentiment.SentimentIntensityAnalyzer()

# Calculate the sentiment scores for each text
sentiment_scores = []
for text in df['Text']:
    sentiment_scores.append(analyzer.polarity_scores(text))

# Create a list of the texts
texts = list(df['Text'])

# Display the sentiment scores for each text
for text, sentiment_score in zip(texts, sentiment_scores):
    print("\n\nText:", text)
    print("Positive:", sentiment_score['pos'])
    print("Negative:", sentiment_score['neg'])
    print("Neutral:", sentiment_score['neu'])
    print("Compound:", sentiment_score['compound'])
```

## Output:
![image](https://github.com/sivabalan28/Implementation-of-Sentimental-Analysis/assets/113497347/97839e5f-385f-4cca-b1cc-f0583ad65e10)


