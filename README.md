# ada-2023-project-adapowerup2023

File containing the detailed project proposal (up to 1000 words).
4. Proposed additional datasets (if any): List the additional dataset(s) you want to use (if any), and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you’ve read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible.
5. Methods
6. Proposed timeline
7. Organization within the team: A list of internal milestones up until project Milestone P3.
8. Questions for TAs (optional): Add here any questions you have for us related to the proposed project.

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
### Deciding on emotions and mapping the scores
After applying Text-Based Emotion Detection (TBED)[^1], emotion scores of the beer styles will be mapped to a mood according to the research [^2]

![image](https://github.com/epfl-ada/ada-2023-project-adapowerup2023/assets/80288512/4783bb5a-33d8-48c4-ad01-cfd266eae77a)

* **Explain** the Hourglass model of emotions is shown in Fig. 3b, and consists of 20 categories (half positive and half negative) in four independent dimensions 

[^1]: S. Zad, M. Heidari, J. H. J. Jones and O. Uzuner, "Emotion Detection of Textual Data: An Interdisciplinary Survey," 2021 IEEE World AI IoT Congress (AIIoT), Seattle, WA, USA, 2021, pp. 0255-0261, 
doi: 10.1109/AIIoT52608.2021.9454192. https://ieeexplore.ieee.org/abstract/document/9454192
[^2]: E. Cambria, A. Livingstone and A. Hussain, "The hourglass of emotions" in Cognitive behavioural systems, Springer, pp. 144-157, 2012.

<!-- Polish all -->

## Methodology

### 1. Data Cleaning, Preparation and Preliminary Analysis

#### 1.1. Preprocessing the main dataset
* Merging datasets
* Eliminating the ones without reviews **(check)** (lowest %20)
* Descriptive statistics: List of features and their quantity
* Visualization of the dataset by charts to better understand our data
* Selection of feautures

#### 1.2. Data Cleaning for textual data
* Analysis of the review dataset and visualization
  - Stemming, lemmitization, stopword removal (NLTK library)
  - Calculating wordcount of each review and each beer
  - Visualizing the most frequent n-grams (n=1,2,3)

#### 1.3. Preparing emotions table and related words
- As mentioned in the additional information part above, we will use the list and we will use the wordlist above for the future work in the semantic similarity part.

### 2. Emotion Detection using Natural Language Processing 

#### 2.1. Scoring the Reviews Using Semantic Similarity Estimation

  - The reviews paragraphs will be the inputs and a similarity score will be obtained calculated by the word list of each mood/emotion
  - A model in SBert will be applied and determination of the model **(manual reading explain)**
  - 
#### 2.2. for beers

### 3. Determining a Mood for Each Beer Style
#### 3.1. Obtaining a vector for each beer style

#### 3.2. Mapping the Styles to the Mood Board

### 4. Methods for the Results Section

#### 4.1. Analysis for Reviews' Emotion Scores

#### 4.2. Analysis for Beers' Emotion Scores

#### 4.2. Final Analysis Comparing Mood of the Beer Styles and

### 5. Concluding the Project by the Recommandations for Different Moods
   * The negative emotions will be eliminated for the final recommandation list since we would not want to recommend any beer in those moods
   * We will provide a list of beer styles and a their moods matched according to the methodology above of mapped emotions
   * If there are many beer styles appointed to a particular mood, the highest rated ones on avarage will be recommended firstly.

For abstract?:
To sum up, we will have scores of emotions for each beer and then a mood for each beer style will be explained according to the emotion map.

## Proposed timeline
* Gannt Chart?
  
## Organization within the team
**A list of internal milestones**
+ Working on the analysis
  - obtaining final results
  - ensuring the quality of code and explanations
+ Coding the webpage
+ Writing the final report and conclusion

+ Planning and monitoring the meetings
