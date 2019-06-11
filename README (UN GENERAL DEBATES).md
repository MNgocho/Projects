Abstract

* Every year since 1947, representatives of UN member states gather at the annual sessions of the United Nations General Assembly. 
* The centerpiece of each session is the General Debate. This is a forum at which leaders and other senior officials deliver statements that present their government’s perspective on the major issues in world politics. These statements are akin to the annual legislative state-of-the-union addresses in domestic politics. The dataset, the UN General Debate Corpus (UNGDC), includes the corpus of texts pertaining  to the General Debate statements from 1970 (Session 25) to 2016 (Session 71). It was uploaded to the Kaggle website by the UN organization. It includes the text of each country’s statement from the general debate, separated by country, session and year and tagged for each.
* This dataset includes over forty years of data from different countries, which allows for the exploration of differences between countries over time. This allows to ask both country-specific and longitudinal questions. In exploring the general structure of data of this dataset, I attempt to generate insights into the UN member countries 

Strategy
* Explore similarity in interests of African countries.
* Topic distribution over the years. 
* Sentiment analysis of the African continent.

Cleaning and Preparation
* Data preparation involved adding a few columns for easier analysis,  removing stop words and digits:. Since the project is  also only interested in Africa , data from  African content was filtered.
* To adequately observe the trends in country relational analysis, grouping data by country and  into five year periods allows easier analysis while creating a list of term infrequency-inverse document frequency(TF-IDF) features.

Algorithms Used
* The main algorithms used in this project were: tf-idf (for comparison purposes), word and sentence tokenizine (to remove unhelpful ubiquitous words), lemmatizer( to remove inflectional endings and get the root word), LDA tool kit (for retrieving topics) ,pylDavis( an interactive way to visualize topics and showcase overlap between topics), Word Cloud ( for displaying tag clouds)  and VADER( a sentiment analysis tool) .

Similarity
* In this case, determining engagement among countries based on the similarity of words they use in UN General Debates speeches. After cleaning the data( removing tags, irregular characters and Unicode characters), grouping data by country and  into five year periods allows easier analysis while creating a list of term infrequency-inverse document frequency(TF-IDF) features.
* In creating the comparison algorithm, the interest lay in finding out the most similar countries and least similar countries in a lustrum. 

Topic Modelling and  Distribution 
* By removing words that appear in less than 10 speeches, the remainder is a more manageable remainder of less than 4000 words. 
* While creating the LDA model, the use of genism creates a unique ID for each corpus. The produced corpus is a mapping of the “word id” and “word frequency”. Also the results are very sensitive to the number of topics chosen. However choosing 14 topics or 15  topics results in similar results. In this case, there are 12 topics.
* PyLDavis  is an interactive way to view overlap in topics. LDA’s main purpose  is to classify documents based on topics, hence overlaps are best avoided. However, in this situation, the interest lies in what is being discussed.

Sentiment Analysis
* VADER(Valency Aware Dictionary and Sentiment Reasoner), a lexicon and rule-based  python sentiment analysis tool was used to fish out the most emotionally-loaded( hence, potentially important) issues.
* Pooling out sentences from all speeches together and giving each a score based on the sentiments expressed on the sentence, consequently, classifying the sentences with the highest score as positive and the ones with the lowest score as negative. Finally using word cloud to generate text clouds.


