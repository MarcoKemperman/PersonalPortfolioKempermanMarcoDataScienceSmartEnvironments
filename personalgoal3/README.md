# Personal Learning Goal 3 – Statistical analysis

## Background
My third learning goal is to become better at analysing data by applyign more statistical methods. Currently often when I analyse results I put the results into easily made bar graphs or pie charts. By the end of the course, I want to be able to use more advanced statistical approaches to analyse our projects data results. As this might also becomes useful later for my thesis. To demonsstrate this I will practice analysing the datasets used in the group project and apply more advanced statistical methods when creating graphs. My progress will be measured by the quality and clarity of the graphs in the final project and feedback from my group members and the teacher on whether the graphs effectively support our analysis.

## Methodology and Data Source
### Methodology
- Calculated basis statistics such as mean, median, count, min, max, and standard deviation.
- Create histogram for each country
- Created boxplot and violin plots to show distribution of sentiment. 
- Created a temporal plot to show average sentiment over the last two weeks for top five countries
- I computed correlation between sentiment and different weather variables such as cloud cover, precipitation, average temperature, maximum temperature, and minimim temperature. 
- I computed coeficient of determination (R2) between sentiment and different weather variables such as cloud cover, precipitation, average temperature, maximum temperature, and minimim temperature.
- I created a temporal graph to show sentiment, rainfall, and temperature for a chosen country, for the last two weeks.

### Packages that I used
- Geopandas
- Matplotlib.pyplot
- Folium
- Numpy
- Seaborn
- Math

## Results
First I calculated the base statisitcs such as the average, median, maximum and minimum. When I had these statistics I could analyse our data more. One of the first plots I created was a histogram of all the countries combined. Here we could easily see that some of the results were distorted due to bot accounts. Some websites automatically posted about the weather online. To decrease this noise I created a code that forbids certain words such as https, wwww, .nl, VesselAlert etc. So in the image below you can see the histogram sentiment distribution before and after filtering out these forbidden words. Furthermore, I added the red drawings to make the visualisation of this statistics more clear as it was not clear to everyone from my group. 
 
<img width="1440" height="552" alt="image" src="https://github.com/user-attachments/assets/18e77f9d-657c-4679-be2e-0070884dab80" />

For the second statistics I created histograms again but this time seperated for each country. With a continuous colour ranging from red negatively to green positively. Also after feedback from the presentation I made sure that for all the histograms the x-as were the same. 
<img width="1990" height="1990" alt="image" src="https://github.com/user-attachments/assets/d078e6bf-a2fc-4266-a255-2a5516c8d6a1" />

For the third statistics I created boxplots for each country. In these plots it shows the median, the 25e percentile and the 75 percentile. I also added a black dash line to clearly see better the zero neutral sentiment. To classify countries based on more positively or negatively leaning. Below the boxplots you can see the violinplots that does show the same results only in a different visualisation. 
<img width="1238" height="543" alt="image" src="https://github.com/user-attachments/assets/0a950514-5977-4485-a1cc-5cdb5202131a" />
<img width="1389" height="590" alt="image" src="https://github.com/user-attachments/assets/75d7c5d4-a4ff-4c93-9b1f-6e87c2280be4" />

Next, I choose to make a temporal graph to see if the sentiment changed over time. At first, I had all the countries in the same plot. But as this was quite chaotic I choose to only visualise the top 5 countries with the most weather posts. 

<img width="1254" height="622" alt="image" src="https://github.com/user-attachments/assets/847e89f1-35e7-41fa-b035-04ff08bdab71" />

After we connected the weather data from Meteostat we also wanted to show the correlation and R2 for the weather and sentiment data. To do this I used seaborn together with numpy and pandas. Together with GenAI I created these nice graphs to show the correlation and the coefficient of determination. I choose to visualise the variables: cloud cover, precipitation, average temperature, maximum temperature and minimum temperature. 

<img width="1934" height="613" alt="image" src="https://github.com/user-attachments/assets/086c0283-0b0a-471f-9a28-fd4e877df8d7" />

At last, I also created our most important final time series graph. In these graphs the average daily sentiment for a certain country (capital) is shown together with the corresponding weather (temperature and precipitation) of that capital. For some of these graphs it was a nice visualisation to indeed see that there is some correlation such as Ukraine-Temperature, France-Precipiation and Belgium-Temperature. But most of the countries did not have such as nice visualisation. 
<img width="932" height="463" alt="image" src="https://github.com/user-attachments/assets/9c46fd96-bf7d-49bb-b2ee-37a04b931f94" />
<img width="913" height="465" alt="image" src="https://github.com/user-attachments/assets/93d105f9-d5a9-4b4e-8ea6-15d71a33a00d" />
<img width="936" height="465" alt="image" src="https://github.com/user-attachments/assets/a897efca-da64-4cf8-b969-fecb3a7cde87" />

**Bonus:** I also want to show the interactive maps that I created. The timeslider map is not fully correct as it shows Northern Island as UK, French Guyana as France, and Ceuta as Spain. However, I did not have the time anymore to fix this. 
https://marcokemperman.github.io/DataScienceSmartEnv/europe_weather_sentiment_map1.html 
https://marcokemperman.github.io/DataScienceSmartEnv/europe_weather_sentiment_timeslider%20(11).html

## Conclusions
### Conclusions on Results
Overall, I am very happy with our statistics and visualisations. It went very well, and was easily created together with aid from GenAI. Also due to the presentations that we had during week 1 and 2, we could also already get some feedback on the statistics and visualisations, which was nice, ase we had the opportunity to improve them. Moreover, in the last week, I asked Jelle multiple times some questions about if the visualisations that I created were quite okay. 

### Conclusions on Accomplishment of the Goal
Overall, I am very satisfied about this goal, and I think I fully accomplished this goal, as I did not make boring bar graphs what I would usually do. For the first time, I used Python to create statistics, therefore I learned a lot of new skills. For the clarity of the graphs and statistics, I think it is quite okay, although some of the visualisations could still use some improvements. 

So what did I learn:
- I learned how to do statistics with Python.
- I learned how to combine weather and sentiment data to calculate the correlation and R2. 
- I learned how to improve visualisations based on feedback from team members and teachers. 

Remaining challenges:
- Improve some visualisations.
- Use more advanced statistics that I have never used before. 
