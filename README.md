<H3>ENTER YOUR NAME:Dhivya DharshiniB</H3>
<H3>ENTER YOUR REGISTER NO.21223240031</H3>
<H3>DATE:30/08/25</H3>
<H1 Align="center">Project Based Experiment<H1>
<H3>Objective:<H3>
 Perform sentiment analysis and filter for negative feedback
<H3>Program:</H3>
 
```
import nltk
from nltk.sentiment import SentimentIntensityAnalyzer
nltk.download('vader_lexicon')
sia = SentimentIntensityAnalyzer()
facebook_data = [
  "We lost the match",
  "I hope you live happily",
  "The person is so beautiful",
  "The service was so bad"
]
negative_feedback = []

for message in facebook_data:
  sentiment_score = sia.polarity_scores(message)['compound']
  if sentiment_score < 0:  # Negative sentiment
      negative_feedback.append(message)
print("Negative Feedback:")
for feedback in negative_feedback:
  print(feedback)

```
<H3>Output:</H3>

<img width="686" height="72" alt="image" src="https://github.com/user-attachments/assets/126ed893-a082-4fa9-adde-a81052aab886" />

<H3>Inference:</H3>
 Thus sentiment analysis to filter the negative feedback in facebook is executed successfully
