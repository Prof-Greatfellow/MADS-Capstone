# Capstone Project: <br> &nbsp; &nbsp; What Remains of the Apocalypse
**Presented to you by Haizhou Liu, Di Lin and Li Zhou**

Welcome to the repo for our MADS Capstone project! In this repo, we are dedicated to **revealing the nature of disaster-related tweets** from different perspectives, including trend, network and the tweet contents themselves. With numerous data mining skills that MADS has imparted us, we are able to come up with many interesting findings. Enjoy!

![](./figs-for-readme/cover-photo.jpg)

*Figure Source: [Top 5 Business Continuity and Disaster Recovery Twitter Follows](https://solutionsreview.com/backup-disaster-recovery/top-5-business-continuity-and-disaster-recovery-twitter-follows/).*
<br>
**Table of Contents**

[TOC]

# On Code Reproducibility
Most of our codes are written in Jupyter Notebook for easier demonstration, and only a few are in the form of python scripts. All codes SHOULD BE reproducible, though, as long as you

1. Correctly install the packages as enumerated in the *requirements.txt* of each folder;

2. Download the dataset from [here](https://drive.google.com/file/d/1lB5yFMmiCVX0BPEh8EkUF4j3B2eE42JP/view?usp=sharing) (which contains both our original and cleaned data), unzip it and put it under the [./assets](./assets)  folder.

3. Run the desired notebook in Google Colab (Pro preferred), if you see this line at the beginning of the notebook: "**Google Colab Required. Google Colab Pro Preferred.**".

# A. Tweet Preprocessing

![](./figs-for-readme/preprocessing.png)

#### Introduction
Our disaster-related tweet corpus comes from the [HumAID dataset on CrisisNLP](https://crisisnlp.qcri.org/humaid_dataset.html), which contains a total of 77,196 tweets covering 19 worldwide disasters. For each tweet there is an also additional label indicating the category of the tweet content.

We further scraped additional information on the tweets (including time of tweet creation, number of likes/retweets, etc.) using [Tweepy](https://www.tweepy.org/) and the [Twitter API](https://developer.twitter.com/en/docs). 

#### Output
- Final datasets: *df_train_scraped_final.csv*, *df_valid_scraped_final.csv*, and *df_test_scraped_final.csv*.
Please also refer to Part B of our [BlogPost]() (!!请更新) for details.

#### Related Codes
- [./Preprocess-Tweet/Preprocess-tweet.ipynb](Preprocess-Tweet/Preprocess-tweet.ipynb): Merge and clean the massive source datasets.
- [./Preprocess-Tweet/Scrape-tweet.ipynb](Preprocess-Tweet/Scrape-tweet.ipynb): Scrape for more info of the tweets.

# B. Trends and Networks

![](./figs-for-readme/trends-and-network.png)

#### Introduction
In this section, we aim to focus on **the statistical and network properties of the tweets**, while not relying on modern natural language analysis toolkits. More specifically, we attempt to answer the following questions:

1. What are the **temporal trends** of disaster tweets under different topics? Are there any similarities between tweet trends of the same/different disasters?

2. What are the **statistical properties** (e.g. number of words/ sentences/ likes/ retweets) of these tweets? Are these properties related to each other, and is there a trend for these properties?

3. Are there any **interesting patterns in the twittersphere network**?

#### Output
Please refer to Parts C and D of our [BlogPost]() (!!请更新) for our research findings.

#### Related Codes
- [./Trends-And-Network/Trends-And-General-Properties.ipynb](./Trends-And-Network/Trends-And-General-Properties.ipynb): Explore the temporal trends and statistical properties of the disaster-related tweets.

- [./Trends-And-Network/Network-Analysis.ipynb](./Trends-And-Network/Network-Analysis.ipynb): Perform network analysis on the tweets.

# C. Supervised Learning

![](./figs-for-readme/supervised-learning.png)

#### Introduction
In this section, we are looking for ways to efficiently predict the human-labeled categories of topic provided by CrisisNLP, by leveraging NLP-based machine learning techniques. 

In [Supervised-Learning-Explore](./Supervised-Learning-Explore), we briefly compared the performance of 3 different ML algorithms: multi-label logisitic regression, LSTM/Bi-LSTM, and BERT.

In [Supervised-Learning-Deeper](./Supervised-Learning-Deeper), we conducted a deeper analysis on two state-of-the-art ML branches: (1) LSTM-based classification, including plain LSTM and BERT-based LSTM, and (2) transformer-based classification, including AlBert, Bert, ConvBERT, DistilBert, FlauBERT, Funnel Transformers, and RoBERTa.

#### Output
The highest accuracy score we have reached so far is **77.3% (BERT)**(!!请确认). Please refer to Part E of our [BlogPost]() (!!请更新) for the ML methods we have used and compared.

#### Related Codes
- In [Supervised-Learning-Explore](./Supervised-Learning-Explore):

&nbsp; [Supervised-Classification-sklearn.ipynb](./Supervised-Learning-Explore/Supervised-Classification-sklearn.ipynb): Logistic regression.

&nbsp; [Supervised-Classification-LSTM.ipynb](./Supervised-Learning-Explore/Supervised-Classification-LSTM.ipynb): LSTM. **Google Colab Required.**

&nbsp; [Supervised-Classification-BiLSTM.ipynb](./Supervised-Learning-Explore/Supervised-Classification-BiLSTM.ipynb): LSTM. **Google Colab Required.**

&nbsp; [Supervised-Classification-BERT.ipynb](./Supervised-Learning-Explore/Supervised-Classification-BERT.ipynb): BERT. **Google Colab Required.**

&nbsp; [See-BERT-embedding.ipynb](./Supervised-Learning-Explore/See-BERT-embedding.ipynb): Visualize the BERT embedding fined-tuned by the tweet content. **Google Colab Required.**

- In [Supervised-Learning-Deeper](./Supervised-Learning-Deeper):

&nbsp; [Lin-Preprocess/](./Supervised-Learning-Deeper/Lin-Preprocess/): Additional tweet preprocessing conducted specially for this section.

&nbsp; [LSTM/](./Supervised-Learning-Deeper/LSTM/): LSTM-based classification, including LSTM, BERT-LSTM and GloVe-Embedding analysis.

&nbsp; [Transformers/](./Supervised-Learning-Deeper/Transformers/): BERT-based classification, including AlBert, Bert, ConvBERT, DistilBert, FlauBERT, Funnel Transformers, and RoBERTa.

# D. Unsupervised Learning
(!!请更新图片)

#### Introduction
(!!请加上Intro)

#### Output
Please refer to Part F of our [BlogPost]() (!!请更新) for our research findings.

#### Related Codes
(!!请按照上述模版添加对Codes的描述)

# Acknowledgements
As our Capstone Project and the MADS program come to a close, we would like to give our sincerest thanks to the entire teaching group of UMSI-MADS. Your well-prepared courses and professional guidance have equipped us with the invincible power to conquer the world of big data. Thank you all, let's keep calm and go blue!