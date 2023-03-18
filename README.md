# QUT and Community Information Exchange Project

##### Note:
##### CIE.pbix - Power BI visualisation for the analysis.
##### N11096837_Final_report.pdf - the report itself.
##### exploratory.ipynb - Python code for exploratory analysis.
##### preprocess.ipynb - Python code for Jan-2020 subset.
##### preprocess_202202.ipynb - Python code for Feb-2022 subset.
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------
Reflection:
1. Nothing is impossible. I had a big headache due to large amount of missing value especially the missing of user's location, but our research team eventually used API to track back each user's location, that was a very good lesson to me.
2. If I have more time on this, two way hierachical clustering seems like a good way to cluter the community services, but it definitely need more preprocess such as manual clustering firstly and use machine learning to do a final clustering.   
3. I should do another subset such as Mar-2022 and Apr-2022 to check if there is any special trends that caused by the flood.


This project was made in IFN704-Advanced Project 2, which is a research unit in the final semester, unit coordinator is professor David Lovell. This is also my second practical project. A nonprofit organisation called Community Information Exchange(CIE) provided their data and asked us if we can dig some insights from it. CIE has a website that allows people to search for coummunity services near by them, the data are the search records that made by the website. This data is extremly large, each subset has over ten million rows and over 60 columns such as time, IP address, whatText(what have been searched), postcode and column types. I mainly focused on the Jan-2020 and Feb-2022 subset because I wonder if there is any difference between a flood year(Brisbane flood happened in Feb 2022) and a normal year. This data is a big chanllenge due to its size, non of our personal computers can deal with such big chunk of data. Another problem is the large existance of missing value, we spent a lot of time on recovering information in a reasonable way. Also, this piece of data contains a lot of unuseful information, thus we did a data cleaning and filtering in order to relieve the burden on memory usage in the first place.  

We eventually summarised a series of questions to three main questions, which is where were the users, what have they searched and when they did a search. Time can answer when did the user search, IP address and postcode can give us a clue of where were the users(We had to use some IP address API to recover most of the user's geographic location), I used path(the user's path on the website) and whatText(what has been searched) to approximately understand what was the intention of the user. 

Eventually, we spent most of the time on data engineering in order to recover the missing information. I tried to use Latent Dirichlet Allocation(LDA) to categorise those search queries into several category such as "townsville_aboriginal_and_islander_health_service" -> "aboriginal health services", so that it would be much easier to understand people's demand, but it didn't perform well because the name of those coummnity services are too short for clustering, and LDA think it's hard to associate services's name with category. In the end, I categorised two-thirds of search queries one by one(tedious), the remaining one-third of search queries are some missing values, services with low demands, and some services that located at the remote area. Power BI was used to visualise those demands to further understand the relation between when, where and what. In terms of the result, I didn't see significant trends that was caused by big flood, but I found there is a big difference between weekdays and weekend in terms of search frequency. 
