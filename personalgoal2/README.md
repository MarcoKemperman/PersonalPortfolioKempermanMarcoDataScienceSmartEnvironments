# Personal Learning Goal 2 – API and Natural Language Processing models

## Background
My second learning goal is that I would like to learn more about API and natural language process (NLP) models, and how I can use them to answer research questions. I would like to learn this as I would like to use NLP models for my own master thesis. Currently, I have limited knowledge on API and NLP models. I have never used a NLP model before so I would like to use one of these models in this course. Furthermore, only once I used an API to access Google Earth Engine on python, but I did not really understood that well how it worked. So at the end of the course, I can use API and I have learned to use NLP models. I will demonstrate this by providing code of the API connection and by creating a Jupyter notebook on how I used a NLP model.

## Methodology and Data Source
### Methodology
- Work with BlueSky API to retrieve posts about weather sentiment
- Work with Meteostat API and retrieve daily weather data
- Connecting a Natural Language Processing (NLP) Model from Hugging Face with our code. 
- Studied the aspects of the NLP

### Programs used
- BlueSky
- MeteoStat
- OpenWeatherMap
- Hugging Face

## Results
The results are shown in the included Jupyter Notebook that has been stored within this folder. 

## Conclusions
### Conclusions on Results
Overall, I am pretty happy about our results. We got the code running with the BlueSky API and we connected this with the Natural Language Processing model and the Meteostat weather data. It was not easy to get everything working, for example the BlueSky API did have a lot of issues with limits on keywords, and limits in relation to date filtering and location. However, I am quite satisfied with our BlueSky connection. 

One thing that I would have liked to see differently is that we should filter more the data CSV file after retrieving this from BlueSky. Because now we tried to filter as much as possible already up front. But due to some mistakes in BlueSky API, sometimes some posts came through without including a weather keyword. 

In addition, I am quite happy about the Natural Language processing model that we used. Of course, it has not always been perfect, and some posts were assigned a wrong sentiment score, if you looked at the post manually. However, if you take the average of all posts, the mistakes are skewed out a bit. We also could not make our own Natural Language Processing model in such a short time, so to use one that is trained on a lot of post and languages, is the best that we could do. 

### Conclusions on Accomplishment of the Goal
To conclude I think I fully accomplished this goal. I have gained a lot more knowledge on how API's work. About that there are limitations to API's and that for some limitations it is possible to work around it, but it comes with some caveats. I also gained knowledge on how to connect a Natural Language Processing Model, and how these models work. As I have read the PDF about the creation of the Roberta model here: https://arxiv.org/pdf/2104.12250. 

So what did I learn:
- I learned how to connect the BlueSky API with python to retrieve posts from BlueSky.
- I learned how to use a online pre-made Natural Language Processing Model to assign sentiment values.
- I learned how the MeteoStat connection worked and how to combine this data with our sentiment scores. 

Remaining challenges:
- It has been difficult to retrieve date filtered post without getting timeout errors in our code.
- As I did not make the Natural Language Processing Model myself it is still a sort of a BlackBox for me, therefore it would also be nice to try develop my own, or reading more into how a NLP model functions. 

