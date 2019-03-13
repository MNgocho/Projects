ABSTRACT
Every year since 1947, representatives of UN member states gather at the annual sessions of the United Nations General Assembly. The centerpiece of each session is the General Debate. This is a forum at which leaders and other senior officials deliver statements that present their government’s perspective on the major issues in world politics. These statements are akin to the annual legislative state-of-the-union addresses in domestic politics. The dataset, the UN General Debate Corpus (UNGDC), includes the corpus of texts of General Debate statements from 1970 (Session 25) to 2016 (Session 71).  It was uploaded to the Kaggle website by the UN organization (https://www.kaggle.com/unitednations/un-general-debates).   It includes the text of each country’s statement from the general debate, separated by country, session and year and tagged for each. The text was scanned from PDFs of transcripts of the UN general sessions. 
This dataset includes over forty years of data from different countries, which allows for the exploration of differences between countries and over time. This allows you to ask both country-specific and longitudinal questions. 
In exploring the general structure of data of this data set, I attempt to generate insights into the UN member countries and, when possible, verify that these insights are consistent with real world geopolitical events and positions.  
The goals of this project are to:
1.	Explore similarity in interests of various countries. 
2.	How do economic partnerships  affect topics discussed by countries?
3.	How does latitude position of each country affect sentiment?
4.	How have previously war-torn countries faired over the years socioeconomically according to on the debates?
5.	Heat maps

1 Project Description
Exploring similarity in interests of various countries can be inferred from finding the most discussed issues by each country, which will be determined by a created dictionary of “possible issues discussed by the UN”.  For accuracy purposes (to ensure that the dictionary reflects the discussed topics), a comparison of the word total word count to the issues highlighted will be surveyed. Creating visualized presentations in the form of bar graphs, pie charts and Venn graphs will be sufficient for relational analysis.

Geographical positions of the member countries are mostly determinant of issues raised by member countries. It will be interesting to not only find similarity in topics discussed by countries that fall in the same geographical region (latitudinally and longitudinally) but to also analyze the sentiment of that specific geographical region. Sentiment analysis will include inferring whether  positive or negative outlooks are applied to the  issues raised. Again, a relevant visual representation will be presented in the form of line graphs.

Topics discussed throughout the years give a general overview of member countries socio-economic climatic overview. They are a good indicator of their (member countries) political and economic infrastructure throughout the years. Especially insightful is to explore the state of affairs over the years of previously war-torn countries. It will be helpful to learn from their methods and strategies if they have been successful or on the other hand learn from their mistakes.

2 Software
Jupyter libraries pandas, NumPy, matplotlib.pyplot ,operator and  were useful in the metadata analysis of the data set and visual representation. Generating, word count, character counter and sentence count produced the state of the data set. Getting a uniform data set was accomplished by setting  uppercase letters to lowercase to simplify the extraction process.

Most significant at this juncture is creating a dictionary of the most possible discussed 
topics at the UN General debates from 1971 to 2016. The following factors were considered while creating the dictionary: historical events (e.g. Rwanda genocide, Afghan war), global issues that spanned within those years and member countries interests.

Throughout the project there are varied methods created to enhance the analysis of data:
I.	FreqMentioned method
This method’s function is to sum up the number of times each topic is mentioned by a  specific country within a list and return the results in both  tabular form and in a plotted horizontal bar. 
Outside the method, a list of  a country or countries should be created so that it can sum up the frequency of the topics from the originally created dictionary (most possible discussed topics dictionary). In addition to this, a for loop of the sorted dictionary is also ran to append the topics.
II.	textFreq method
First, this is a parent method. It returns frequency of data in tabular form. The table displays a word count of included topics in a list within a subset of countries( created outside the method). 
III.	groupFreq method
This is a child to the textFreq (previously mentioned) method. It allows us to create a grouping column of the already collected data. The grouping column allows us to group the distribution of the topics yearly in tabular form. The function; plot()  can be added to plot a linear graph for optimal visual analysis.






3 Topics raised by UN Member Countries
At the core of this project, is creating a dictionary of the most possible discussed topics at the UN General debates from 1971 to 2016. The following factors were considered while creating the dictionary: historical events (e.g. Rwanda genocide, Afghan war), global issues that spanned within those years and member countries interests.

4 Exploring Relational Analysis

In approaching regional analysis, it is significant to note that each region has got its own particular historical and geographical context. This is the reason why the  approach for each region is on either of or both of these bases (history, geography).

This is particularly due to the relevance of the insights from the results.  For example, It would be unrealistic to relate  Australia and Uganda in a similar purview as both have a different contextual array of issues that would affect them or be of interest to them. To begin with, Australia does not have immediate neighboring countries to deal with (New Zealand, New  Guinea  and Fiji are separated by water). Uganda on the other hand is a landlocked country with five countries surrounding its borders. Uganda is obviously a developing country ( in regard to its GDP per capita) while Australia is not. Uganda has had a civil war [add a reference]and Australia has not had one so far.  However, countries that are in different geographical regions but have had a recent history of civil war would be fit to run a relational analysis. In that regard, in order to optimize the relational analysis process, I will categorize relationships based on the following features:

	Regional trade partnerships.
	Countries with a recent history of civil war
	Security council  countries interest in developing countries
	Positive and negative sentiment towards regional neighbours

AFRICA
 

i.	Regional Trade Partnerships.

Africa of course has a short history since its member countries’ border allocation and  independence. Also, the path to African integration has been marked by a series of major initiatives and political decisions to accelerate it and to integrate variables of new imperatives in international economic relations. In particular, there are eight regional economic communities recognized by the African Union Heads of State and Government as constituting the building blocks of the African Union:
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
c)       Free movement of persons
d)      Peace, security, stability and governance 
e)      Harmonization of sectoral policies
 
1.	The Arab Maghreb Union (AMU)
The AMU consist of the following countries: Algeria, Libya , Mauritania, Morocco and Tunisia. Geographically located in North Africa the AMU was founded February 1989 in Marrakech with the approval of the Treaty Instituting the Arab Maghreb Union. [add reference] . As per the results of the frequently discussed topics, there seems to be equality in frequency of  most topics brought up in the debates. The following are the exceptions:
A.	Child mortality and sanitation are not discussed by any member country
B.	The following topics are brought up by one or two member countries:
•	Depression- Mauritania
•	Communicable diseases – Mauritania and Libya
•	North Korea – Algeria and Tunisia
•	Ozone – Tunisia and Libya
•	Communism- Tunisia and Libya
•	Extinction- Mauritania
•	Toxic waste – Libya and Tunisia
•	Totalitarian – Mauritania and Tunisia
•	Rape – Libya and Mauritania
•	Nuclear war – Libya
•	Pollution – Libya and Tunisia
•	Dictator – Libya and Tunisia
•	Cancer – Libya and Tunisia
C.	The following topics are discussed substantially in comparison to the other member countries.
•	Cuba – Libya 
•	Drought – Mauritius
•	Water – Libya
•	Mass destruction – Libya
•	Overthrow – Libya
•	Communicable diseases – Mauritania
•	Ozone – Tunisia
•	Terror – Libya
The negative economic topics brought up at the UN debates seem to be minimal except for sanctions. Sanctions seem to be prevalent throughout the years with a notable sharp incline and decline in the early 1970s and early 1980s,1990s and  finally early 2000s. Inflation, inequality and recession  are other topics  that lends to the credence of the economic climate of the region. Of interest to note, is that these topics seem to take a seat in the early 2000s. Both communism and capitalism are dormant.

When it comes to topics regarding peace and stability: terror,  war and weapons are consistent and seem to inclining and declining at the same rate.  There is a striking  sharp incline and immediate decline in the early 1970s and late 2000s. Tribalism is an inert topic in this region.
 
Geographical positions of AMU member countries 
 
 


Visual results of the frequently discussed topics

 
 





