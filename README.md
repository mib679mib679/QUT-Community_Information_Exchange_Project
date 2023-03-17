# QUT_and_Community_Information_Exchange_Project

This project was made in IFN704-Advanced Project 2, which is a unit in the final semester, unit coordinator is professor David Lovell. This is also my second practical project. A nonprofit organisation called Community Information Exchange(CIE) provided their data and asked us if we can dig some insights from it. CIE has a website that allows people to search for coummunity services near by them, the data are the search records that made by the website. This data is extremly large, each subset has over ten million rows and over 60 columns such as time, IP address, whatText(what have been searched), postcode and column types. I mainly focused on the Jan-2020 and Feb-2022 subset because I wonder if there is any difference between a COVID year and a normal year. This data is a big chanllenge due to its size, non of our personal computers can deal with such big chunk of data. Another problem is the large existance of missing value, we spent a lot of time on recovering information in a reasonable way. Also, this piece of data contains a lot of unuseful information, thus we did a data cleaning and filtering in order to relieve the burden on memory usage in the first place.  

We eventually summarised a series of questions to three main questions, which is where were the users, what have they searched and when they did a search. Time can answer when did the user search, IP address and postcode can give us a clue of where were the users(We had to use some IP address API to recover most of the user's geographic location), I used path(the user's path on the website) and whatText(what has been searched) to approximately understand what was the intention of the user.   


to be continued...
