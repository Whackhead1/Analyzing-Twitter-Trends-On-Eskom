# Analyzing Twitter trends on Eskom

## TABLE OF CONTENTS

* [Background](#background)
* [Objective](#objective)
* [Tools and Packages](#tools)
* [Data Collection](#data-collection)
* [Data Pre-Processing](#data-preprocessing)
* [Data Modeling](#data-modeling)
* [Data Visualization](#data-visualization)
* [Results](#results)


<hr>

## BACKGROUND 
With 2022 on track to be the worst year for South Africa for load shedding, the highest stage ever being implemented, and Eskom workers striking, conversations on social media has increased dramatically, with dissent towards Eskom growing.

<hr>

## OBJECTIVE 
<li>To extract information from tweets (between 09 March and 15 July) related to Eskom vaccine where opinions are highly unstructured, heterogeneous and are either positive or negative, or neutral</li>
<li>To explore conversations and abstract "topics" that occur in the collected tweets using topic modeling and text analytics</li> 
<li>To visualize the trends in sentiments of Twitter users and popularity associated with the discovered topics</li> 

<hr> 

## TOOLS

<table style="width:100%">
  <tr>
    <th>Task</th>
    <th>Technique</th> 
    <th>Tools/Packages Used</th>
  </tr>
  <tr>
    <td>Data Collection</td>
    <td>Tweet extraction from Twitter</td> 
    <td>snscrape</td>
  </tr>
  <tr>
    <td>Data Pre-processing</td>
    <td>Remove punctuation, stopwords, URLs, emojis, , mentions, lemmatization</td> 
    <td>re, nltk, pandas, numpy</td>
  </tr>
  <tr>
    <td>Topic Modeling</td>
    <td>Unsupervised LDA</td> 
    <td>LatentDirichletAllocation, sklearn, pyLDAvis.sklearn</td>
  </tr>
  <tr>
    <td>Text Analytics</td>
    <td>Sentiment Analysis</td> 
    <td>vaderSentiment</td>
  </tr>
  <tr>
    <td>Data Visualization</td>
    <td>Multi-attribute plots</td> 
    <td>matplotlib, seaborn</td>
  </tr>
  <tr>
    <td>Environments &amp Platforms</td>
    <td></td> 
    <td>Jupyter Lab, Twitter</td>
  </tr>
</table><br>

<hr>

## DATA-COLLECTION 

<b> Data Collection: Identifying Eskom Content </b>

<li> Package used: snscrape</li>
<li>Language: English</li>
<li>Keywords: eskom</li>
<li>Timeframe: 09 March 2022 to 16 July 2022</li>
<li>Number of tweets collected = 310689</li>

<b> Data Coverage: </b>
With eskom as the search terms, I believe that the keyword provides reasonable coverage and is representative of tweets communicating about eskom and loadshedding <br>

<hr>

## DATA-PREPROCESSING

<b> Data Cleaning </b> 

<li> Removed puctuation, URLS, mentions, emojis using library re</li> 
<li> Removed stopwords using nltk </li> 
<li> Lemmatization of Tweets using nltk.WordNetLemmatizer() </li>

<hr>

## DATA-MODELING

<b> Unsupervised LDA </b>
To understand the abstract topics hidden in the tweets unsupervised LDA technique was implemented using the library 'pyLDAvis'. 8 different topics were discovered with similar cluster sizes and slight overlapping in clusters.
<b> Sentiment Analysis </b>
Sentiment analysis is a supervised machine learning problem with different types of analysis. I considered a fine-grained sentiment classification with five levels of sentiments - overly positive, positive, neutral, negative, and overly negative. VADER (Valence Aware Dictionary for Sentiment Reasoning) was used as a rule-based model to examine the impact of loadshedding on the attitude of Twitter users. 

<hr>

## DATA-VISUALIZATION 

<b> Sentiment Distribution </b>
<img src="" style="width:500px;height:200px;">
<hr>

<b> Sentiment volume by day </b>
<img src="" style="width:500px;height:200px;">
<hr>

<b> Sentiment volume by week </b>
<img src="" style="width:500px;height:200px;">
<hr>

<b> Topic Distribution </b>
<img src="" style="width:500px;height:200px;">
<hr>

<b> Topic volume by day </b>
<img src="" style="width:500px;height:200px;">
<hr>

<b> Topic volume by week </b>
<img src="" style="width:500px;height:200px;">
<hr>

## RESULTS 
<li> Discovered 8 distinct topics from the tweets</li>
<li>Negative sentiment contributed the most in overall sentiments of Twitter users, followed by positive and neutral sentiments</li>
<li>The most discussed topics were loadshedding times, loadshedding lasting longer than scheduled, and ANC state capture.</li>