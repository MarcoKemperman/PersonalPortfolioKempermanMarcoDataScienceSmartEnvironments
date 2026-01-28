# Final reflection Marco Kemperman

### Reflection on Data quality and methods: 
For the methods I believe that the way we retrieved the information was about the right way to do it. BlueSky had its limitations and therefore for some limitation we could work around it, but for some it did not work out that well. We used the BlueSky API to retrieve posts. We retrieved a maximum of 8000 posts per keyword. This was the result of the fact that if you choose to receive more than 8000 posts per keyword, there is a big possibility that the code will result in a 501 error. Furthermore, as BlueSky limits only 100 post retrieval per time, we had to loop around it to retrieve it until a maximum of 8000 per keyword. 
For the weather data we used MeteoStat data. We accessed the packages and we retrieved weather data for all our capitals. We choose to only work with capitals for both our weather and sentiment data, because otherwise the data quality would be very low, as you cannot say that weather sentiment from the north of Norway, is the same as real weather data from weather station in Oslo. https://github.com/meteostat/meteostat
For the sentiment data we used the model from Roberta. We choose to work with this model as this model is trained on 198 million posts of Twitter (which has similar post structure as BlueSky). The model has been trained over more than 30 languages, making it suitable for our analysis. The model was created after running for 14 days on 8 Nvidia GPUs. It also costed more than 5000 euros to do so. We chose to work with it as it would not have been feasible to make a model in such a short time for ourselves. https://huggingface.co/cardiffnlp/twitter-xlm-roberta-base-sentiment

The eventual data quality of our results in pretty low. As I already wrote in our StoryMaps limitation, we have a lot of limitations. Limitations that I noticed were BlueSky API restrictions, including search caps, crashes after large post retrievals, and the inability to filter by date (although possible but terribly slow for more than 200 keywords) or user location. This made it very difficult to retrieve a high-quality dataset of temporal and spatial accurate weather sentiment posts. Moreover, there were issues with language (same words with different meanings across languages), multi-location posts, and posts referring to different days (such as next weekend) created some misclassification sentiment compared to the real weather. Duplication of some posts, bots, sarcasm, and informal language further disrupted our results. If we had more time and better hardware, the study could include more data, more countries, better date filtering, and additional social media platforms. However, for this project it was now out of our scope. 

I further want to point out that we could have done more data cleaning. At first, I thought that it was best to clean data before data retrieval. Therefore, we already filter quite a lot such as forbidden words, only retrieve posts with weather keywords, and only retrieve posts with capital cities. Only posts that met all three conditions are retrieved as I visualised in the table below. However, due to some mistakes most probably in BlueSky API sometimes posts were retrieved that did not satisfy all three conditions. Therefore, if I would do it again, I would also filter more after data retrieval to make sure that all the three conditions are met again. 
<img width="1138" height="666" alt="tableview" src="https://github.com/user-attachments/assets/a77976b1-a9eb-4a94-843d-72dc0e46ee7c" />

What I learned the last couple of weeks is that retrieving informal data from BlueSky and converting this data into something that you can quantify is pretty difficult. It would be impossible to get a code / model running that works perfectly without limitations. There will always be limitations, if not within the code, it could be within the API or in the Natural Language Processing Model. We tried to get data with some quality that we could work with. I think we did manage this, as we did have some nice graphs and statistics in the end. But still a lot of noise was still in the data that was not filtered out in these three weeks. For the limited amount of time, I am quite satisfied with what we achieved. Of course I can probably write a lot more about the limitations of our project or about the BlueSky API, but I think I have already written this in more detail within the StoryMaps. https://arcg.is/nurma 

----------------------------

### Reflection on societal implications of our project, and potenial use of application. 

This project helps to address the gap between objective weather data and how people subjectively experience and emotionally respond to weather conditions. While meteorological data provides detailed information on variables such as temperature and precipitation, it does not capture how these conditions influence people’s emotion, well-being, and daily experiences. By using sentiment analysis of weather-related social media posts, this study tried to add the human perspective to weather data. Some studies have already examined the relation between weather and sentiment such as the studies from Young et al. (2025), and Wang et al. (2025). These studies found that there is a relation between sentiment and weather, and that when temperature becomes above 35 it impacts the sentiment drastically. Moreover, the research examined that lower income countries express their negative sentiment far more prominently, as they also have more limited ways to cope with the weather. However, all these studies have been does using X (Twitter), while our study has examined BlueSky. 

Even though we examined the sentiment from a new platform, the societal benefit of this project is limited. Although the results show differences in sentiment under different weather conditions, these findings are mainly exploratory and do not directly translate into practical applications. Moreover, social media users tend to express negative opinions more than positive ones, which can bias the results. In addition, methodological limitations, such as restricted location and time filtering reduced our reliability of the findings. Despite these limitations, the project can be valuable as a concept. It demonstrates how subjective online expressions can be linked to weather data. With improved data access and methods, future studies could potentially be conducted to better understand how weather affect people’s perceptions and experiences in Europe.

- Young, J. C., Arthur, R., & Williams, H. T. P. (2025). The linguistic and emotional effects of weather on UK social media users. Scientific Reports, 15(1), 8009. https://doi.org/10.1038/s41598-024-82384-w
- Wang, J., Guetta-Jeanrenaud, N., Palacios, J., Fan, Y., Kakkar, D., Obradovich, N., & Zheng, S. (2025). Unequal impacts of rising temperatures on global human sentiment. One Earth, 8(10), 101422. https://doi.org/10.1016/j.oneear.2025.101422 

----------------------------
### Reflection on group
If I am being honest, the group work did not go as well as I had hoped. During the first week, Simen was still stuck in Norway due to snow issues at Schiphol. As a result, we mainly had to work with three people, and most of the collaboration was online. Because of this, communication did not go very smoothly. It was difficult to see what everyone was working on. Despite this, I tried to keep the group updated on my progress. For example, I already got some code working to retrieve Bluesky posts. At the end of the first week, Tom and I gave the presentation together.

In the second week, I continued working on the code, and Simen was now present and able to help me. Meanwhile, Jingxi and Tom worked on the ethics posters. During this week, I started to become a bit more dissatisfied with the group collaboration. Already in the first week, I felt that I had put in the most work, but I accepted this because it was an unusual week with working from home. However, in the second week, I hoped that we would work more together at the university. Unfortunately, this was not really the case. On Tuesday afternoon, for example, I was the only one working. On several other days, I also stayed later than the rest of the group. Additionally, on Friday, I created the PowerPoint for the presentation and presented again, this time together with Simen.

At this point, I should have communicated my dissatisfaction to the group, but I did not. This was a mistake on my part. I should have told them that I was not satisfied with the collaboration and that I would have preferred everyone to be more present at the university.

During weeks 2 and 3, Tom was often not at university and preferred to work from home due to the travel distance. I understand that driving every day can be difficult, and I accepted that he worked from home. However, I noticed that he did not seem to put as much time into the project. He did contribute to the posters and possibly some other tasks, but this likely did not take a large amount of time. He mentioned that I could text him if I wanted him to do something, but I did not do this. This is partly my mistake. I am not a natural leader, and I found it difficult to tell people what to do or to assign tasks.

Jingxi was more often at university and worked well when I gave her specific tasks. However, when I did not assign tasks, she did not do that much, and I think she found it difficult to know what to work on. This is also partly my responsibility. I should have checked more often whether she knew what to do and asked what she would like to work on. In the last week, I gave her a task to work on the StoryMaps, and she did this well. This showed me that if I had given her more tasks earlier, she probably would have contributed more.

Simen worked well with me on the code during weeks 2 and 3. However, on some afternoons he went home earlier or was not present. In the last week, he was sick one day. Because of this, I had to take over the task of combining the weather data with the sentiment data. Overall, I think Simen contributed well in the last two weeks and coded together with me, but I still spent significantly more time on the project.

As a result of me doing a large part of the work, I noticed that during all three presentations I had to answer all of the questions. While I was capable of doing this, I did not really like it, as it made it seem like I was the only one who fully understood the project. I also created the PowerPoint for the final presentation. When Tom wanted to help with it, I noticed that it was difficult for him to contribute because he was no longer fully aware of what the project was doing. For example, he still thought we were getting location data from the bio, while we had already switched to using location from the posts.

Again, this could partly be my fault for not communicating these changes clearly enough. However, I also expected a more proactive attitude from some of my group members, such as asking what I was working on or what still needed to be done. I do not enjoy being the leader of the group, but if I end up in that role, I expect people to take initiative and actively ask how they can contribute.

I am aware that many of these issues are also partly my responsibility. I do not want to say that my group members did nothing. Everyone contributed something and delivered parts of the project. However, the majority of the work for this group project was done by me. All of the visualisations, graphs, and maps were coded by me (together with AI). I understand that not everyone is comfortable with coding, and I do not expect everyone to code. However, I did hope for more collaboration and a more proactive attitude from the team.

Because I spent so much time on the group project, I now still have to create my entire personal portfolio in the fourth and final week, while I saw that others had already started working on theirs in week 3. I did not have time to do this earlier, as I was focused on completing our group project.

I am not writing this to blame others (I think it is miscommunication from all sides), but to give context. I would like this to be taken into consideration when grading both the group project and my personal portfolio, as I believe I have put in significantly more time and effort than others. At first, I did not mind, as I learned many new and interesting things related to coding, APIs, and natural language processing. However, in the last week, this situation became more frustrating for me.

To conclude, as this is a reflection, I could have done better in communicating my frustrations. In future group projects, I should divide tasks better so that the division is more equal. In addition, I should point out my personal preference of working on campus and I should point out if someone does not work that much for the group, even though I am a conflict avoidant person. 

----------------------------

### Reflection on Boundary Crossing Competences

#### Example 1: Working together with Jingxi

**Identification:**
I was working very hard on a lot of different things at the same time. Therefore, I could not also spend much time on the StoryMap that I started to make.
To complete the task of the StoryMap I needed someone that was creative, used StoryMaps before, and someone that could look at our results from a different perspective. 

**Coordination:**
As I already understood from Jingxi that she did not know the link to the Google Colab was on Whatsapp, I had to make sure that I was more clear in communication. 
I asked her if she could work on our StoryMaps. I saw her making beautiful drawings for our ethics posters, so I identified that Jingxi was a creative person. 

**Reflection:** 
When I think back at this project I think about that I often did too many things, and I did not ask for help. Therefore I think it was nice to see that the time I did ask for help from Jingxi that she did a great job in making the StoryMap more visual pleasing and also expanding it with some text. I learned that during the weeks that Jingxi is willing to help but is a bit shy to ask herselve. I also know that it can be quite difficult for her communicating with us, as she sometimes has difficulties with English. Therefore I think it is nice to see that she did well to finish the beautiful Storymap. 

**Transformation:**
Unfortunately this happened in the last week of our project. Therefore, I did not ask more help from my group in finishing some tasks. But I did learn some new perspectives that it is okay to ask for help, people are willing to help, and when I assign tasks to others, they can do a great job. So for the future, I think for me, it would be nice, that when I work in a group project, to identify strengthts of each person at the start of the project, so that people can work on assignments that they like and are good at. Also this experience shaped me in believing that I should ask for more help, and communicate more clearly to people what I would like to see from them. 

#### Example 2: Working on location

**Identification:**
My norms and values in group work is that you show up on university when there is groupwork assigned in the schedule. I know this is not always the case for everyone, so I try to be flexible by not restricting group members to be on campus all the time. What I also notice is that I do not work that well together remotely on different locations. I value working together. 

**Coordination:**
What would be needed is to discuss in group what everyone values in terms of working. If it should be flexible, or not. If it should be on location, or location independent. My biggest mistake in the coordination is that I did not discuss my preference for being at university and being there when group work is assigned in the schedule. 

**Reflection:** 
When I think about it when writing this, it feels a bit weird. About two years ago, me and a group also had a lot of reflection assignments about working together in a group. I got feedback from one of my groupmembers that I should be more flexible, with schedule and with group work. Now for this course, I think it came to a point that because it did not dicuss my personal preference, it became too flexible. Creating an environment where people stayed at home to work, limiting the progress of our group work. I allowed people to work from home, and I did not mind when people were leaving earlier. However, I did started to become more frustrated by this at the end of the course. Eventually I think it all came down to communication. If the communication went better the groupwork would have went better too. I also know that this is a weakness from my part, as this also came up in an earlier group reflection. 

**Transformation:**
So when talking about transformation, I do think I transformed from being an unflexible person, to a person that is more flexible to work with. However, I do also think that I could have done better in comminicating my preferences to my group mates. While they did tell me their preference of working from home, I was too shy or conflict avoidant to tell them my opinion. To conclude, I did try to be different this time, but I did not communicate well enough my preferences to my group members. 

#### How I am going to continue with BCC.
- Ask for more help when I am stuck. 
- Communicate more clearly my team mates and my own preferences
- Communicate better in general. 
- Discuss with my teammates better how we would like to work as a group.

**References used for support in making the BCC**
- Gulikers, J. (2020). Examples of boundary crossing learning activities. https://edepot.wur.nl/566880
- Fortuin, K. P. J., Gulikers, J. T. M., Uiterweer, N. C. P., Oonk, C., & Tho, C. W. S. (2023). Developing a boundary crossing learning trajectory: supporting engineering students to collaborate and co-create across disciplinary, cultural and professional practices. European Journal of Engineering Education, 49(2), 212–235. https://doi.org/10.1080/03043797.2023.2219234

----------------------------

### Reflection on what went well.
Of course, a lot of things did go well too. We have been able to retrieve weather posts from BlueSky, and connect this to real weather data. We have some statistical analysis that shows some correlation. Furthermore, I think we all learned a lot, as a result of the freedom we get in this course. I definetely learned a lot about coding, API, statistics and more. We also created some nice posters that were used for some interesting discussions in class. So overall, although I might sometimes sound negative in this reflection, I am actually really satisfied with what we achieved in these short three weeks. 

