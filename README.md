ABSTRACT
Every year since 1947, representatives of UN member states gather at the annual sessions of the United Nations General Assembly. The centerpiece of each session is the General Debate. This is a forum at which leaders and other senior officials deliver statements that present their government’s perspective on the major issues in world politics. These statements are akin to the annual legislative state-of-the-union addresses in domestic politics. The dataset, the UN General Debate Corpus (UNGDC), includes the corpus of texts of General Debate statements from 1970 (Session 25) to 2016 (Session 71).  It was uploaded to the Kaggle website by the UN organization .   It includes the text of each country’s statement from the general debate, separated by country, session and year and tagged for each. The text was scanned from PDFs of transcripts of the UN general sessions. 
This dataset includes over forty years of data from different countries, which allows for the exploration of differences between countries and over time. This allows you to ask both country-specific and longitudinal questions. 
In exploring the general structure of data of this data set, I attempt to generate insights into the UN member countries and, when possible, verify that these insights are consistent with real world geopolitical events and positions.  
The goals of this project are to:
1.	Explore similarity in interests of African  countries. 
2.	Topic distribution over the years.
3.	How do economic partnerships  affect topics discussed by countries?
4.	How have previously African war-torn countries faired over the years socioeconomically according to on the debates?
5.	Sentiment analysis of the African continent
To accomplish these goals, well-known machine learning and text analytics techniques will be using, including LDA (Latent Dirichlet Analysis), word frequency and term co-occurrence along with other visualization techniques. 


1 Project Description

Exploring similarity involves evaluating word similarity among countries in the speeches. Using the term infrequency-inverse document frequency(TF-IDF) features and LDA should enable categorizing the speeches topically and semantically, allowing a relational analysis of the countries. Creating visualized presentations in the form of bar graphs, pie charts and Venn graphs will be sufficient for this kind of analysis.

Topics discussed throughout the years give a general overview of member countries socio-economic climatic overview. They are a good indicator of their (member countries) political and economic infrastructure throughout the years. Topic distribution first  involves fishing  for topics in the dataset. Latent Dirichlet Allocation is a popular type of topic modeling. LDA is an unsupervised learning model that takes as input our speeches and the number of topics that we wish to find. It assumes that documents are created by picking a small number of topics which then "generate" words with certain probabilities as output: 
1.For each of the speeches, it enables us to view the topics it is composed of, and to what extent. 
2.For each topic, we see a bag of words that describe it. These are the words that the topic is most likely to "generate" and their corresponding probabilities.
This can help by manually deciding that, e.g. words present in >80% documents will be discarded. Similarly, one can remove words present in too few documents. Hence, LDA will point out the topics that should be assessed for similarity across the African continent. Especially insightful is to explore the state of affairs over the years of previously war-torn countries. It will be helpful to learn from their methods and strategies if they have been successful or on the other hand learn from their mistakes.

Africa of course has a short history since its member countries’ border allocation and  independence The path to African integration has been marked by a series of major initiatives and political decisions to accelerate it and to integrate variables of new imperatives in international economic relations. In particular, there are eight regional economic communities recognized by the African Union Heads of State and Government as constituting the building blocks of the African Union:
1.	The Arab Maghreb Union (AMU)
2.	The Common Market for Eastern and Southern Africa (COMESA)
3.	The Community of Sahel-Saharan States (CEN-SAD)
4.	The East African Community (EAC)
5.	The Economic Community of Central African States (ECCAS)
6.	The Economic Community of West African States (ECOWAS)
7.	The Intergovernmental Authority on Development (IGAD)
8.	The Southern African Development Community (SADC)
Having grouped African countries according to this eight economic unions, the goal is to gain insights and inferences from the debates over the years, on the socioeconomic climate of these organizations based on the five key pillars derived from treaties and protocols of the African Union and the regional economic communities:
a)      Trade and market integration
b)      Macroeconomic policy convergence
c)      Free movement of persons
d)      Peace, security, stability and governance 
e)      Harmonization of sectoral policies

Finally, it will be interesting to not only find similarity in topics discussed by countries that fall in the same geographical region (latitudinally and longitudinally) but to also analyze the sentiment of that specific geographical region. Sentiment analysis will include inferring whether  positive or negative outlooks are applied to the  topics raised. Again, a relevant visual representation will be presented in the form of line graphs.

2 Software
The data analysis is entirely executed in python with the following python libraries in use.
 
 In order to describe the software artifact adequately and clearly the code descriptions are grouped based on the goals of the project. 

i.	Preparing data set  for analysis
To begin with, a peak into the data shows as the state of the data,  especially of interest is noting the column context.
 
 
So far, we have established columns include:  an index column, session, year, country( in ISO-alpha3 Codes) and the text(which represent the actual speeches given by a specified  country).  However, the  focus is only on African countries. Categorizing the countries continentally by merging the data set with second data set( includes the columns: country name, region, ISO-alpha codes) establishes an  easy way to filter the African countries. This is possible by performing a  left merge of the ISO-alpha codes. The data set is  retrieved from https://unstats.un.org/unsd/methodology/m49/overview/.
 

Consequently, limiting the countries of interest to the African continent. The function nunique() proves that only the values of interest are part of the analysis process.
  

ii.	Explore similarity in interests of African  countries. 
First and foremost, considering how to deduce similarity is key to attaining an accurate summarization of relations between African countries. In this case, determining engagement among countries based on the similarity of words they use in UN General Debates speeches. After cleaning the data( removing tags, irregular characters and Unicode characters), grouping data by country and  into five year periods allows easier analysis while creating a list of term infrequency-inverse document frequency(TF-IDF) features.
 
 
Creating  5000 (TF-IDF) features columns is fitting for this particular comparison algorithm, using an ngram_range of (1,3) . 


 
 
A look at the features generated from the TF-IDF confirms that they are in accordance with UN discourse:
 
 

Finally, in creating the comparison algorithm, the interest lay in finding out the most similar countries and least similar countries in a lustrum. The following method is created for that particular purpose:
 
Since the grouping is done for every 5 years, i.e:
[1970-1974]: 

[1975-1980]:
 
[1981-1985]:
 
[1986-1990]:
 
[1991-1995]:
 

[1996-2000]:
 
[2001-2005]:
 

[2006-2010]:
 


[2011-2015]: (Reminder: the data is from 1970-2017)
 

