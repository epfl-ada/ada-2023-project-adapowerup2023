# ada-2023-project-adapowerup2023

# The Beer Mood Matcher

## Abstract
Our daily decisions tend to be influenced by our mood, and this concept is applied to beer selection. Our research is focused on determining how different beers relate to various moods expressed in reviews on popular platforms of BeerAdvocate and RateBeer. We will analyze and score reviews using advanced Natural Language Processing techniques, specifically Sentence-Bert, based on primary emotions including joy, sadness, anger, fear, love, and surprise. Furthermore, we will determine the relationship between the characteristics of various beers and the moods they evoke, as identified in user reviews which can be beneficial for the marketing industry. In the last part of the study, based on the mapped emotion score we will create a mood-based recommendation of beer styles.

## Research Questions
- How do the characteristics of different beers align with the moods identified in reviews?
    * In what moods do users tend to write comments?
    * Does a specific correlation exist between beer styles and the range of emotions identified in consumer reviews?
    * Is there a pattern between higher-rated beers and positively=scored reviews?
    * What kinds of moods do the best-selling beers tend to match?
    * Are there any regional distribution characteristics of users’ moods towards beer?
    * What is the perfect beer for any mood?

## Additional Information
### Selection of Emotions for Review Analysis
The primary emotions listed in Figure 1 below will be used to score the reviews. It is selected by analyzing the literature of emotion detection, and these emotions are found to be the main headings of emotions known as Parrot's emotion model.

![image](https://github.com/epfl-ada/ada-2023-project-adapowerup2023/assets/80288512/4783bb5a-33d8-48c4-ad01-cfd266eae77a)

Figure 1:  Parrot’s emotions model [^1]

After applying text-based emotion detection, we will use an emotion map to obtain the moods of the beer styles[^2]

[^1]: S. Zad, M. Heidari, J. H. J. Jones and O. Uzuner, "Emotion Detection of Textual Data: An Interdisciplinary Survey," 2021 IEEE World AI IoT Congress (AIIoT), Seattle, WA, USA, 2021, pp. 0255-0261, 
doi: 10.1109/AIIoT52608.2021.9454192. https://ieeexplore.ieee.org/abstract/document/9454192
[^2]: E. Cambria, A. Livingstone and A. Hussain, "The hourglass of emotions" in Cognitive behavioural systems, Springer, pp. 144-157, 2012.

## Methodology

### 1. Data Cleaning, Preparation and Preliminary Analysis

#### 1.1. Preprocessing the main datasets
* Working on two different dataset of different websites: BeerAdvocate and RateBeer
* Excluding beers with a minimal number of reviews to have a more represantative data.
* Descriptive statistics: List of features and their quantity

#### 1.2. Visualization of the dataset by charts to better understand our data
* Utilizing charts to enhance understanding of the data.

#### 1.3. Preprocessing the textual review data
* Analysis and visualization of the review dataset
  - Stemming, lemmitization, stopword removal (NLTK library)
  - Calculating wordcount of each review and each beer
  - Visualizing the most frequent n-grams (n = 1, 2, 3)

### 2. Emotion Detection using Natural Language Processing 

#### 2.1. Implementing Semantic Similarity Estimation for Review Scoring

  - Inputs will be review paragraphs, and similarity scores will be calculated based on a designated word list for each emotion, using the SentenceTransformers framework within an SBert model [^3].

    [^3]: Reimers, N., & Gurevych, I. (2019). Sentence-bert: Sentence embeddings using siamese bert-networks. arXiv preprint arXiv:1908.10084. https://www.sbert.net/
    
#### 2.2. Scoring the Emotions of Beers
* By averaging the scores from reviews for the same beer, we will generate a list of average scores across six emotions for each type of beer.

### 3. Determining a Mood for Each Beer Style
#### 3.1. Obtaining an Emotion Vector for Each Beer Style
* We will obtain a vector of 6 emotions by averaging the scores of all beers under the same style.
  
#### 3.2. Mapping the Styles to the Mood Board
Based on the emotion vector of each beer style, we will map the styles onto mood board, assigning the most representative mood to each beer style.  

### 4. Methods for the Results Section

#### 4.1. Analysis for Reviews' Emotion Scores
Based on the emotion scores, we can study further on the relationship between mood and other potential variables, for example, there might be some regional distribution patterns of user’s mood towards beer. Besides, we can relate mood to beer characteristics and test the correlation of them, to explore whether beer’s appearance, aroma, or taste would influence drinker’s mood.

- Regional distribution of reviews’ moods
   - Creation of a geographical heat map or histogram to visualize the emotion scores for different regions, to show the regional distribution of moods. 
   - Performing statistical tests, such as t-tests or ANOVA, to compare whether there are significant differences in emotion scores across regions.

- Correlation between mood and beer’s characteristics (appearance, aroma, taste)
   - Creating a scatter plot to show the relationship between different beer characteristic scores and emotion scores.
   - Performing hypothetical tests to test the correlation between mood and different beer characteristics. 
   - Using correlation analysis such as Pearson's correlation coefficient to quantify the linear relationship between them. If there is a linear correlation, use linear regression to fit the model.

#### 4.2. Analysis for Beers' Emotion Scores
For different beers, there could be interesting study on the potential relationship between mood and some beer attributes. As some examples; normally, users are expected to review a beer with positive emotions when they give high ratings, so we will explore the correlation between mood and beer ratings, then try to discover the “top-rated moods”. Moreover, drunkenness usually leads to mood swings, so do we get anger after getting high, or feel really relaxed? We will study the correlations between mood and ABV to find the answer.

- Correlation between mood and beer ratings
   - Creating a scatter plot to show the relationship between the emotion scores of different beers and their ratings.
   - Applying statistical tests to further understand the correlation between mood and beer ratings, perform correlation analysis to quantify the linear relationship between them, and if there is a linear correlation, use linear regression to fit the model.
   - Discovering the moods corresponding to the top-rated beers, then there could be some marketing strategy for brewers, for example, creating an atmosphere with a related “top-rated mood” when marketing the beer.
 
- Correlation between mood and ABV
   - Creating scatter plots to show the relationship between the emotion scores of different beers and their ABV.
   - Performing correlation analysis to try to quantify the linear relationship between them, and apply statistical tests to further understand the correlation between mood and beer concentration.

     
### 5. Concluding the Project by the Recommandations for Different Moods
   * The negative emotions will be eliminated for the final recommandation list since we would not want to recommend any beer in those moods.
   * We will provide a list of beer styles and a their moods matched according to the methodology above of mapped emotions.
   * If there are many beer styles appointed to a particular mood, the highest rated ones on avwrage will be recommended firstly.

## Proposed timeline

![image](https://github.com/epfl-ada/ada-2023-project-adapowerup2023/assets/80288512/f9e72abb-0255-4cd5-8870-b4c77fe54726)
  
## Organization within the team

| Team Member | Role |
|--- | --- |
|Yiwei | NLP for emotions + |
|Yunong | 	|
|Victor| |
|Zimu| Analysis of the Results + |
|Nil | NLP for emotions + Data Story |

