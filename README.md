# Finding weak signals through NLP
This project was focused on finding weak signals in the gaming industry to understand what consumers were talking about the most and also to understand their sentiments towards related topics.

I initiated the process by selecting relevant subreddits dedicated to discussions on modding. Once the subreddits were identified, I extracted the data using API library praw in Python. I selected essential post attributes for my analysis, such as titles, bodies, authors, scores, and replies. To have better control and meaningful results in our data, I limited the time window from October 5th to November 5th, 2023. The data was then stored in a JSON file, and I proceeded to cleanse it by removing superfluous symbols and rectifying spelling errors that could potentially impact the data analysis. I also created a separate dictionary that included certain gaming-related words and jargon so that I could retain them during the data cleansing process.

With my refined dataset in hand, I employed Term Frequency-Inverse Document Frequency Analysis (TF-IDF). TF-IDF is a recognized method for assessing the significance of words within a given document. The mod-related keywords were crucial for conducting a sentiment analysis, which I accomplished using the TextBlob library, which then classified the
data into polarity to determine its sentiment. Finally, to be able to detect weak signals, I used topic modeling to identify thematic patterns in the entire corpus of the data. This would help me understand the topics discussed on corpus-level, and how they are related to the words resulting from the TF-IDF analysis results.

![image](https://github.com/Aditya17k/Finding-weak-signals-with-NLP/assets/119431183/ccdda71e-c52d-4a8e-8395-b3f5b28af22e)

When analyzing the results of the TF-IDF analysis (refer to Appendix 2), we can identify numerous trends that could be regarded as weak signals. Firstly, the high scores of the TF-IDF analysisindicate that the words that derived from the analysis are both frequently used in the dataset, but that they are also unique, in the sense that they are meaningful. Additionally, words like “crash”, “issue”, and “problem” indicate that users are using mods to solve bugs and other technical difficulties in games. This suggests that mods are a means to troubleshoot and overcome issues with specific games. Moreover, my results reflect my theory about users modifying games as a means to gain enhanced control over the game. This is highlighted in my output by words like “armor”, “weapon”, and “texture”. 

Both of these results are aligned with my theory that modding serves utilitarian purposes, such as addressing in-game issues, along with psychological needs, as it gives users an enhanced sense of control. The importance of specific in-game features was also highlighted in my results, with words like “quest”, “overhaul”, and “npc” having notable TF-IDF scores. These elements indicate additional topics discussed within the gaming communities.
