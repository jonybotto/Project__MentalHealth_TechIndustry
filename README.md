# Mental Health: Is it still a Taboo? | Insights from the Tech Industry

&nbsp;

## Motivation and Objectives
It is important for people living with a mental health disorder (and everyone around them) to have the **proper awareness** level and the **means for prevention and treatment** in all spheres of their lives, including at the workplace (since it is there that individuals spend a large amount of their lifetime). Hence, an interesting question arises: **How exactly does the workplace fare on these issues?**

The intent with this project is to draw insights from the technology industry, considering the period from 2014 to 2019, on the level of awareness of mental health disorders, and how these are handled in a working environment context. However, having these evaluations done, the real endgoal is to **provide solutions for a healthier and more sustainable workplace** on a mental health perspective.

&nbsp;

## Requirements

To run the notebook, first install dependencies using pip:

```Python
pip install -r requirements.txt
```

&nbsp;

## Source of the Data
The datasets used for this project were retrieved from [Kaggle](https://www.kaggle.com/datasets/anth7310/mental-health-in-the-tech-industry/data). However, the primary source of the data was [Open Sourcing Mental Illness (OSMI)](https://osmihelp.org).

&nbsp;

## Datasets Descriptions
The SQLite database contains 3 tables: **Survey**, **Question**, and **Answer**.

* Survey (PRIMARY KEY INT SurveyID, TEXT Description)
* Question (PRIMARY KEY QuestionID, TEXT QuestionText)
* Answer (PRIMARY/FOREIGN KEY SurveyID, PRIMARY KEY UserID, PRIMARY/FOREIGN KEY QuestionID, TEXT AnswerText)

SurveyID are simply survey years i.e. 2014, 2016, 2017, 2018, 2019.
The same question can be used for multiple surveys.
Answer table is a composite table with multiple primary keys. SurveyID and QuestionID are FOREIGN KEYS.
Some questions can contain multiple answers, thus the same UserID can appear more than once for a particular QuestionID.