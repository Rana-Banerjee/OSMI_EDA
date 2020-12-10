# OSMI_EDA
<B> Exploratory analysis of the OSMI Mental Health in Tech Survey from 2014 to 2019 </B>

<B> Project Motivations </B>:

  It is widely believed that technology jobs is among the most stressful of all jobs. Could this also be leading to more mental health issues among the tech-workers as opposed to the non-tech workers? This github repo is create to explore the following questions using the OSMI Mental Health Survey results collated for 2014, 2016, 2017 and 2018 and published in kaggle.
  Q1) Are people working in Tech reporting higher mental health issues than non-Tech workers?
  Q2) Do people working in smaller organisations have better or worse mental health than those working in larger organisations?
  Q3) What type of role do people with mental health issues have?

<B>About Dataset:</B>

  This data is from Open Source Mental Illness (OSMI) using survey data from years 2014, 2016, 2017, 2018 and 2019 and available at https://www.kaggle.com/anth7310/mental-health-in-the-tech-industry Each survey measures and attitudes towards mental health and frequency of mental health disorders in the tech workplace.
  The raw data consists of a SQLite database containing 3 tables. Survey, Question, and Answer.
1) Survey (PRIMARY KEY INT SurveyID, TEXT Description)
2) Question (PRIMARY KEY QuestionID, TEXT QuestionText)
3) Answer (PRIMARY/FOREIGN KEY SurveyID, PRIMARY KEY UserID, PRIMARY/FOREIGN KEY QuestionID, TEXT AnswerText)

  SuveyID are simply survey year ie 2014, 2016, 2017, 2018, 2019.
  The same question can be used for multiple surveys
  Answer table is a composite table with multiple primary keys. SurveyID and QuestionID are FOREIGN KEYS.
  Some questions can contain multiple answers, thus the same user can appear more than once for that questionid.

<B>Dependencies and Libraries</B>


<B>File descriptions:</B>
1) OSMI_EDA.ipynb: The step by step exploration is captured in this jypyter notebook
2) data: folder that contains the raw kaggle data in sqllite format and the intermediate enriched data in csv format
3) images: graphs generated by the notebook code and other images used in the medium post

<B>Summary of result:</B>

Followign the EDA done on the data one could conclude the following:
1) Based on the quality and quantity of the data available, it will be difficult to assume any correlation between the type of work and mental health challenges.
2) One might however derive the insight that people facing mental health challenges find it better to work in large companies due to the support system provided by them.
3) Also, one may also conclude that roles that does not involve social interactions are more favourable for people facing mental health issues.


<B>More details of the analysis can be found in the following post:</B>

https://rana1224.medium.com/is-your-job-affecting-your-mental-health-1cda47871a8

