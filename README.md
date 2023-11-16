# ada-2023-project-adapowerup2023

# The Beer Mood Matcher

## Abstract (will be written lastly- A 150 word description of the project idea and goals. What’s the motivation behind your project? What story would you like to tell, and why?)

## Research Questions
- How do the characteristics of different beers align with the moods identified in reviews?
    * In what moods do users tend to write comments?
    * Does a specific correlation exist between beer styles and the range of emotions identified in consumer reviews?
    * Is there a pattern between higher-rated beers and positively=scored reviews?
    * What kinds of moods do the best-selling beers tend to match?
    * Are there any regional distribution characteristics of users’ moods towards beer?
    * What is the perfect beer for any mood?

## Additional Information
### Deciding on emotion list and map
The list of emotions in the list below will be used to score the reviews under these headings. It is selected by analyzing the researchs of emotion detection, and these emotions are found to be the main headings of emotions.

After applying Text-Based Emotion Detection (TBED)[^1], emotion scores of the beer styles will be mapped to a mood according to the research [^2]

![image](https://github.com/epfl-ada/ada-2023-project-adapowerup2023/assets/80288512/4783bb5a-33d8-48c4-ad01-cfd266eae77a)

* **Explain** the Hourglass model of emotions is shown in Fig. 3b, and consists of 20 categories (half positive and half negative) in four independent dimensions 

[^1]: S. Zad, M. Heidari, J. H. J. Jones and O. Uzuner, "Emotion Detection of Textual Data: An Interdisciplinary Survey," 2021 IEEE World AI IoT Congress (AIIoT), Seattle, WA, USA, 2021, pp. 0255-0261, 
doi: 10.1109/AIIoT52608.2021.9454192. https://ieeexplore.ieee.org/abstract/document/9454192
[^2]: E. Cambria, A. Livingstone and A. Hussain, "The hourglass of emotions" in Cognitive behavioural systems, Springer, pp. 144-157, 2012.

## Methodology

### 1. Data Cleaning, Preparation and Preliminary Analysis

#### 1.1. Preprocessing the main dataset
* Merging datasets
* Eliminating the ones without reviews **(check)** (lowest %20)
* Descriptive statistics: List of features and their quantity
* Selection of feautures - Eliminating some parts of the dataset
#### 1.2. Visualization of the dataset by charts to better understand our data

#### 1.3. Preprocessing the textual review data
* Analysis of the review dataset and visualization
  - Stemming, lemmitization, stopword removal (NLTK library)
  - Calculating wordcount of each review and each beer
  - Visualizing the most frequent n-grams (n=1,2,3)

#### 1.4. Preparing emotions table and related words
- As mentioned in the additional information part above, we will use the list and we will use the wordlist above for the future work in the semantic similarity part.

### 2. Emotion Detection using Natural Language Processing 

#### 2.1. Scoring the Reviews Using Semantic Similarity Estimation

  - The reviews paragraphs will be the inputs and a similarity score will be obtained calculated by the word list of each mood/emotion
  - A model in SBert will be applied and determination of the model **(manual reading explain)**
    SentenceTransformers[^3] will be implemented

    [^3]: Reimers, N., & Gurevych, I. (2019). Sentence-bert: Sentence embeddings using siamese bert-networks. arXiv preprint arXiv:1908.10084.
    https://www.sbert.net/
#### 2.2. for beers

### 3. Determining a Mood for Each Beer Style
#### 3.1. Obtaining a vector for each beer style

#### 3.2. Mapping the Styles to the Mood Board
Based on the mood vector of each beer style, we will map the styles to the mood board to label every beer style with a most representative mood.  
(Create a mood board with corresponding beer styles labels on the map)

### 4. Methods for the Results Section

#### 4.1. Analysis for Reviews' Emotion Scores
Based on the emotion scores, we can study further on the relationship between mood and other potential variables, for example, there might be some regional distribution patterns of user’s mood towards beer. Besides, we can relate mood to beer characteristics and test the correlation of them, to explore whether beer’s appearance, aroma, or taste would influence drinker’s mood?

- Regional distribution of reviews’ moods
   - Create a geographical heat map or histogram to visualize the emotion scores for different regions, to show the regional distribution of moods. 
   - Perform statistical tests, such as t-tests or ANOVA, to compare whether there are significant differences in emotion scores across regions. 
   - Try to explain the regional differences in moods from aspects such as cultural background, environment, climate, etc.

- Correlation between mood and beer’s characteristics (appearance, aroma, taste)
   - Create a scatter plot to show the relationship between different beer characteristic scores and emotion scores.
   - Perform hypothetical tests to test the correlation between mood and different beer characteristics. 
   - Use correlation analysis such as Pearson's correlation coefficient to quantify the linear relationship between them. If there is a linear correlation, use linear regression to fit the model.

#### 4.2. Analysis for Beers' Emotion Scores
For different beers, there could be interesting study on the potential relationship between mood and some beer attributes. Normally, users are expected to review a beer with positive emotions when they give high ratings, so we will explore the correlation between mood and beer ratings, then try to discover the “top-rated moods”. Moreover, drunkenness usually leads to mood swings, so do we get anger after getting high, or feel really relaxed? We will study the correlations between mood and ABV to find the answer.

- Correlation between mood and beer ratings
   - Create a scatter plot to show the relationship between the emotion scores of different beers and their ratings.
   - Apply statistical tests to further understand the correlation between mood and beer ratings, perform correlation analysis to quantify the linear relationship between them, and if there is a linear correlation, use linear regression to fit the model.
   - Discover the moods corresponding to the top-rated beers, then there could be some marketing strategy for brewers, for example, creating an atmosphere with a related “top-rated mood” when marketing the beer.

- Correlation between mood and ABV
   - Create scatter plots to show the relationship between the emotion scores of different beers and their ABV.
   - Perform correlation analysis to try to quantify the linear relationship between them, and apply statistical tests to further understand the correlation between mood and beer concentration.

#### 4.2. Final Analysis Comparing Mood of the Beer Styles and

### 5. Concluding the Project by the Recommandations for Different Moods
   * The negative emotions will be eliminated for the final recommandation list since we would not want to recommend any beer in those moods
   * We will provide a list of beer styles and a their moods matched according to the methodology above of mapped emotions
   * If there are many beer styles appointed to a particular mood, the highest rated ones on avarage will be recommended firstly.

For abstract?:
To sum up, we will have scores of emotions for each beer and then a mood for each beer style will be explained according to the emotion map.

## Proposed timeline

![image](https://github.com/epfl-ada/ada-2023-project-adapowerup2023/assets/80288512/f9e72abb-0255-4cd5-8870-b4c77fe54726)
  
## Organization within the team
**A list of internal milestones**

| Milestones | Nil | Yiwei | Yunong | Victor | Zimu | 
|--- | --- | --- | --- | --- | --- |
| `Obtaining Semantic Similarity Scores of Reviews` |  |  |  |  |  |
| `Working on the Emotion Map`                      |  |  |  |  |  |
| `Analysis of the Results`                         |  |  |  |  |  |
| `Coding the webpage`                              |  |  |  |  |  |
| `Data Story`                                      |  |  |  |  |  |

