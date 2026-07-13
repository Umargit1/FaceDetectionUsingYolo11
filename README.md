# OSS Sentiment & Social Network Analysis

## 🎯 Overall Goal
This research project aims to analyze open-source software (OSS) projects to uncover the relationships between developer communication patterns (sentiment and emotion), social network structures, and organizational anti-patterns (social smells). 

Ultimately, the goal is to understand how these socio-technical factors impact project success and health, evaluated through metrics such as bug rates, bug resolution time, and feature velocity. The analysis pipeline utilizes the [Kaiaulu](https://github.com/sailuh/kaiaulu) toolkit.

## 📊 Target Projects
We are collecting and processing JIRA and code review data for the following prominent Apache projects:
* **Kafka**, **HBase**, **Camel**, **Flink**, **NiFi**, **Solr**, and **Ignite**

## 💻 Sentiment Analysis & Interactive Colab Notebooks
For the sentiment analysis phase of this research, we utilize the [SEntiMoji](https://github.com/SEntiMoji/SEntiMoji) framework. We trained the models directly on the datasets provided within the SEntiMoji repo. 

After training, We performed sentiment analysis testing across distinct datasets downloaded via Kaiaulu:

* **JIRA related Model of SEntiMoji (Trained on `JIRA.txt`):** 
  * Tested on the Kaiaulu issue comments dataset, which I downloaded using [`download_github_issue_comments.Rmd`](https://github.com/sailuh/kaiaulu/blob/master/vignettes/download_github_issue_comments.Rmd).
  * Also applied to the Kafka JIRA comments dataset, downloaded using [`download_jira_issues.Rmd`](https://github.com/sailuh/kaiaulu/blob/master/vignettes/download_jira_issues.Rmd).
* **Code Review Model of SEntiMoji (Notebook 1):** 
  * Tested on Pull Request (PR) comments from the Kaiaulu repository, which I downloaded using [`download_github_pull_request_comments.Rmd`](https://github.com/sailuh/kaiaulu/blob/master/vignettes/download_github_pull_request_comments.Rmd).

To make the analysis easily accessible, these core workflows have been uploaded as interactive Google Colab notebooks. By cloning and running these Colab notebooks, you can:

Code Review  related Notebook of SEntiMoji:
SEntiMoji_Notebook_Kaiaulu_PR_Analysis.ipynb



JIRA related Notebook of SEntiMoji:

SEntiMoji_Notebook_Jira_Analysis.ipynb



* Test the sentiment analysis pipeline using the custom-trained SEntiMoji models.
* Automatically generate and view bar graphs of the sentiment distributions (0/1 polarities) for a clear visual understanding of the project data.

All necessary environment setups and dependency installations are handled seamlessly within the notebook cells. 

## 🔗 Key Links & Deliverables

### Published Sentiment Networks (RPubs)
* **Kaiaulu Core Network:** [View on RPubs](https://rpubs.com/Umar-Mazhar/1445719)
* **Kafka Project Network:** [View on RPubs](https://rpubs.com/Umar-Mazhar/1445857)




