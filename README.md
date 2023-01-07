# Cricket Commentary Sentiment Analysis and Generation
- NLP Project which aims to dissect cricket commentary data, find the sentiment of cricket commentary and aim to generate cricket commentary automatically givem some keywords
- We have Asia cup data which is smaller which we use for sentiment analysis and we have IPL ball by ball data for 3 years which is bigger for training a model for automatic commentary generation
- All data is from Kaggle
- Sentiment analysis is performed to see if commentary given is neutral in sentiment or slightly positive
- Up to now websites like cricbuzz provide commentary for matches by manual typing. I aim to automate this process with a commentary generator given keywords of events obtained by some manner (eg image processing)

# Algorithms used

### Sentiment Analysis
- We try out and compare 2 algorithms
- VADER (Valence Aware Dictionary and Sentiment Reasoner) lexicon and rule based bag of words model
- Roberta Pre-trained model (transform based)

### Commenrary Generation
- GPT-2 (Generative Pretrained Transform)

## Sentiment Analysis (Cricket_Commentary_Sentiment_Analysis.ipynb)
- Dataset link : https://www.kaggle.com/datasets/balabaskar/asia-cup-2022-ball-by-ball-data-and-commentary
- I first load and learn about the dataset
- I reduce the dimensionality of the dataset by picking only the required features
- I then pre-process by performing spelling correction, stopwords removal, tokenization and text encoding.
- I then apply both algorithms and obtain the polarity/sentiment scores
- Comparison of the models is done by a plot and conclusions are drawn (in depth in the notebook)

## Commentary Generation
 Commentary Generator is done in google colab platform as we require google drive for storage and GPU for fast model training
 We perform 3 steps to produce a model for automatic commentary generation
 1. Dataset preparation and pre-processing
 2. Model training
 3. UI creation to display model to the user
 
### Data pre-processing (CommentaryGeneration_DatasetPreperation.ipynb)

- Datasets link: https://www.kaggle.com/datasets/mhemendra/cricinfo-ipl-commentary
- Datasets are stored in drive and is mounted to colab
- Datasets are loaded and manipulated, columns are renamed and bowler/batsman names are extracted and put into seperate columns
- Only required rows are retained which reduces dimensionality and finally datasets are combined
- The batsman and bowler names are nouns which our model should not learn hence they are identified in the commentary text and substituted by generic terms like batsman and bowler so generated commentary is generic and does not suprise you with a pre learned cricketers name
- Spelling correction is done then data is split to train and test
This split data is then manipulated to the form which is accepted by GPT-2 algorithm and the data is now ready
- The pre-processed data can be found in the Data folder of the Sentiment Analysis section in this repository

###

###

# Demo

# Conclusion
