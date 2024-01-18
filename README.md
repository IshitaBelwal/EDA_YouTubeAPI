# EDA_YouTubeAPI

# Exploratory Data Analysis Using Youtube Video Data 

## 1. Introduction
Established in 2005, YouTube has evolved into the world's second-largest search engine, handling over 3 billion searches monthly, trailing only behind Google. Despite its immense popularity, the inner workings of the YouTube algorithm remain shrouded in mystery, making it challenging for content creators to decipher the factors influencing a video's success and recommendation. YouTube boasts one of the most expansive and sophisticated industrial recommendation systems globally.

For newcomers to content creation, unraveling the reasons behind a video's popularity can be perplexing. Numerous myths circulate, such as the belief that higher likes or comments, or a specific video duration, guarantee success. It is essential for aspiring creators to experiment and discern trends within their niche.

Having recently entered the content creation realm with a new YouTube channel focused on data analytics and data science, I sought to gain insights that could benefit fellow creators. This project's focus is exclusively on data science channels, excluding other niches with distinct characteristics and audience bases. The exploration will delve into the statistics of approximately 10 highly successful data science YouTube channels.

## 2. Aim & Objective
In the course of this project, my objectives include:

#### 1. Understanding the YouTube API:
- Delving into the YouTube API to grasp its functionalities and procedures for obtaining video data.

#### 2. Video Data Analysis:
- Verifying common "myths" associated with video performance on YouTube:
    - Investigating if the number of likes and comments correlates with higher   views.
    - Assessing the impact of video duration on views and user interaction (likes/comments).
    - Examining whether title length influences the number of views.
    - Analyzing the number and relevance of tags in well-performing videos.

#### 3. Content Creator Patterns:
- Investigating upload frequency and preferred days for uploading videos across the selected creators.

#### 4. NLP Techniques for Trend Analysis:
- Utilizing Natural Language Processing (NLP) techniques to discern trending topics:
    - Employing word clouds to identify prevalent themes in video titles.

#### 5. Comment Section Exploration:
- Scrutinizing the comment sections of videos to answer questions like:
    - What questions are frequently asked by viewers?
    - What engagement patterns emerge from the comments?


By combining these approaches, the project aims to offer a comprehensive understanding of factors influencing the success of data science YouTube channels, debunking or confirming common myths and shedding light on patterns that can guide content creators in the data science niche.

## 3. Steps of the project

##### 1. Obtain video meta data via Youtube API for the top 10-15 channels in the data science niche (this includes several small steps: create a developer key, request data and transform the responses into a usable data format)
##### 2. Prepocess data and engineer additional features for analysis
##### 3. Exploratory data analysis
##### 4. Conclusions

## 4. Dataset
### Data Selection
As this project is particularly focused on data science channels, I found that not many readily available datasets online are suitable for this purpose. The 2 alternative datasets I found are:

- [The top trending Youtube videos on Kaggle](https://www.kaggle.com/rsrishav/youtube-trending-video-dataset): This dataset comprises data spanning multiple months, documenting the daily occurrence of trending YouTube videos in various countries, with each day featuring up to 200 such videos. Regrettably, this dataset does not align with the objectives of this project. The reason lies in the diverse array of topics covered by the trending videos, which may not necessarily pertain to the field of data science.

- Another dataset is obtained from this [Github repo](https://gitlab.com/thebrahminator/Youtube-View-Predictor) of Vishwanath Seshagiri, containing metadata for over 0.5 million YouTube videos and associated channel information, was discovered. While the dataset lacks explicit documentation detailing its creation methodology, a preliminary examination of the repository indicated that the data was likely gathered through keyword searches encompassing popular terms like "football" or "science." Notably, there were pertinent keywords like "python" as well. Despite the dataset's breadth, it was deemed unsuitable for my purposes, as it did not encompass data pertinent to the specific channels I am focusing on.

I created my own dataset using the [Google Youtube Data API version 3.0](https://developers.google.com/youtube/v3). The exact steps of data creation is presented in section 2. Data Creation below.

### Data Limitation
The dataset chosen for this research is derived from real-world data, making it suitable for analysis. However, it is essential to note that the selection of the top 10 YouTube channels for inclusion in the study is solely based on my familiarity with channels in the data science field, and this may not be entirely accurate. The criterion for defining "popularity" is currently limited to subscriber count, neglecting other pertinent metrics such as views and engagement. Additionally, the choice of the top 10 channels might appear arbitrary, considering the vast number of channels on YouTube. There is a possibility that smaller channels could present valuable insights, thus potentially constituting the next phase of this project.

### Ethics of data source
According to [Youtube API's guide](https://developers.google.com/youtube/v3/getting-started), utilizing the API is cost-free as long as your application adheres to specified quota limits. The purpose of implementing a quota is to ensure developers utilize the service appropriately, preventing the creation of applications that might compromise service quality or hinder access for others. By default, each application is allocated 10,000 units per day, and if this limit is reached, developers can request additional quota by completing a form accessible through YouTube API Services.

It's noteworthy that all data obtained from the YouTube API pertains to public information, accessible to anyone on the internet through YouTube. Consequently, there are no privacy concerns associated with the data. Furthermore, it's essential to emphasize that the data is exclusively gathered for research purposes and not for any commercial interests.
