# ada-2023-project-adapowerup2023

File containing the detailed project proposal (up to 1000 words). Your README.md should contain:

1. Title
2. Abstract: A 150 word description of the project idea and goals. What’s the motivation behind your project? What story would you like to tell, and why?
3. Research Questions: A list of research questions you would like to address during the project.
4. Proposed additional datasets (if any): List the additional dataset(s) you want to use (if any), and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you’ve read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible.
5. Methods
6. Proposed timeline
7. Organization within the team: A list of internal milestones up until project Milestone P3.
8. Questions for TAs (optional): Add here any questions you have for us related to the proposed project.

# TITLE: The Beer Mood Matcher
**Alternatives:** 
* The Emotional Brewer: Aligning Beers with Your State of Mind
* Brewed Feelings: A Beer-to-Mood Experience / Crafting the Perfect Mood-Based Beer Experience

## Abstract (will be written lastly)

## Research Questions
opt1.1. "How do the characteristics of different beers align with the moods identified in reviews?"
- more broad, we can focus on both characteristics (flavor, aroma, color, etc) and types of the reviews.
- consider how to have one characteristic for one beer or should we analyze each review separately?
  
opt1.2. "Does a specific correlation exist between beer styles and the range of emotions identified in consumer reviews?"
- more specific, narrowing the focus to the styles of beer (like IPA, stout, lager, etc.) and examining whether these styles have a distinct relationship with the emotions reviewers express.

optional related subquestions
What kinds of moods do the best-selling beers tend to match?
In what moods do users tend to write comments?
Is there any relationship between the mood corresponding to beer and its rating?
Are the moods people perceive toward a certain beer consistent, or are there multiple differences?
Are there any regional distribution characteristics of users’ moods towards beer?
“What is the perfect beer for any mood?”


## Methods

**1. Data Cleaning, Preparation and Preliminary Analysis**

1.1. Preprocessing the main dataset
* Merging datasets and eliminating the ones without reviews **(check)**
* list of features and their quantity
* descriptive statistics - charts (10 

1.2. Preparing emotions table and related words (table/dataset)


**2. Determining Emotions of Reviews using NLP**


* Analysis of the review dataset and visualization
   - Calculating wordcount of each review and each beer
   - Finding frequent n-grams(n=1,2,3) after removing the stopwords
     
* Semantic Similarity Estimation using SBERT or Spacy **?**
  - The reviews paragraphs will be the inputs and a similarity score will be obtained calculated by the word list of each mood/emotion


**3. Deciding a Mood/Emotion for Each Beer**


## Proposed timeline
* Gannt Chart?
  
## Organization within the team
**A list of internal milestones**
+ Working on the analysis
  - obtaining final results
  - ensuring the quality of code and explanations
+ Coding the webpage
+ Writing the final report

+ Planning and monitoring the meetings
