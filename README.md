[![Use this document under the CC BY-SA 4.0 license](https://i.creativecommons.org/l/by-sa/4.0/80x15.png)](http://creativecommons.org/licenses/by-sa/4.0/)

# A Comparison of Machine Learning Platforms

Machine Learning (ML) Platforms are services which help Data Scientist
to build, test, deploy and/or monitor ML models.
Companies often build, buy or rent ML Platforms because they want to

* increase their deployment speed of ML models, 
* improve the productivity of their Data Scientist,
* standardize their ML practices and
* reduce the operational complexity of ML models.

ML Platform are a relatively new concept, and our collective understanding of what exactly 
they are and what they should do is still evolving. The goal of this document is to give an 
overview over the current state of ML Platforms by comparing the capabilities of different 
platforms. It is written for ML practitioners and assumes that readers are familiar with ML 
terminology. If you are new to the topic, I highly recommend to read the 
[TWIML Machine Learning Platforms Report][TWIML Report] as introduction.


## Capabilities and Components of ML Platforms

Here is a non exhaustive collection of possible capabilities of ML Platforms.

### Data Acquisition and Feature Management 
  - Centralized Data Access 
  - Data Pipelines 
  - Manual Labeling 
  - Label generation (e.g. via week supervision) 
  - Feature Repository 
  - Feature provenance 
  - Backfills
  - Data versioning 

### Experiment Management & Model Development 
  - Experiment Tracking 
  - Model Versioning
  - Distributed Training 
  - Automated Feature Generation 
  - Automated Hyper-parameter Optimization 
  - AutoML 
  - Model partitioning 
  - Workflows 
  - Hosted Notebooks 
  - Model building GUI 

### Model Deployment and Performance Monitoring 
  - Model Deployment 
  - Model Serving 
  - Basic Model Monitoring 
  - Concept Drift Detection 
  - Online Experiments
  - Phased Deployments 
  - Feedback Collection
  - Scheduled Retraining
  - Dynamic Retraining 
  - Batch Scoring 



## Proprietary ML Platforms

Proprietary ML Platforms are developed by large companies for in-house use. 
As outsiders, we often only have an incomplete and possibly outdated picture of their 
capabilities from blog posts and conference talks.
Nonetheless, it is useful to compare their features, because this group contains 
some of the most mature and heavily used platforms.


### Known Capabilities

|                          | BigHead | FBLearner | Michelangelo | Overton | Pro-ML   |
| ------------------------ | :-----: | :-------: | :----------: | :-----: | :----:   |
| Company                  | Airbnb  | Facebook  | Uber         | Apple   | LinkedIn |
| Productive since         |         |           |              |         |          |
| **Data Acquisition and Feature Management** |
| Centralized Data Access  | ✓       | ✓         | ✓            |         |          |
| Data Pipelines           | ✓       | ✓         | ✓            |         |          |
| Manual Labeling          |         |           |              |         |          |
| Label Generation         |         |           |              | ✓       |          |
| Feature Repository       | ✓       | ✓         | ✓            |         | ✓        |
| Feature Provenance       | ✓       |           |              |         |          |
| Backfills                | ✓       |           |              |         |          |
| Data Versioning          | ✓       | ✓         |              |         |          |
| **Experiment Management and Model Development** |
| Experiment tracking      | ✓       | ✓         | ✓            | ✓       | ✓        |
| Model Versioning         | ✓       | ✓         | ✓            | ✓       | ✓        |
| Distributed training     |         |           | ✓            |         | ✓        |
| Auto Feature Generation  |         |           |              |         |          |
| Auto Hyperparameter opt. | ✓       |           | ✓            | ✓       |          |
| AutoML                   |         |           |              | ✓       |          |
| Model Partitioning       |         |           | ✓            | ✓       |          |
| Workflows                | ✓       | ✓         |              | ✓       |          |
| Hosted Notebooks         | ✓       |           |              |         |          |
| Model building GUI       |         |           |              |         |          |
| **Model Deployment and Performance Monitoring** |
| Model Deployment         | ✓       | ✓         | ✓            |         | ✓        |
| Model Serving            | ✓       |           |              |         |          |
| Basic Model Monitoring   | ✓       | ✓         | ✓            |         | ✓        | 
| Concept Drift Detection  | ✓       |           | ✓            |         |          |
| Online Experiments       |         | ✓         |              |         | ✓        |
| Phased Deployments       |         | ✓         |              |         | ✓        |
| Feedback Collection      |         | ✓         | ✓            |         |          |
| Scheduled Retraining     |         |           | ✓            |         |          |
| Dynamic Retraining       |         |           |              |         |          |
| Batch scoring            | ✓       |           |              |         |          |

**Sources:**
+ BigHead: 
  - [TWIML Machine Learning Platforms Report][TWIML Report]
  - [Zipline: Airbnb’s Machine Learning Data Management Platform (Slides)](https://www.slideshare.net/databricks/zipline-airbnbs-machine-learning-data-management-platform-with-nikhil-simha-and-andrew-hoh)
  - [Bighead: Airbnb’s Machine Learning Platform (Podcast)](https://twimlai.com/twiml-talk-198-bighead-airbnbs-machine-learning-platform-with-atul-kale)
+ FBLearner:
  - [TWIML Machine Learning Platforms Report][TWIML Report]
  - [Introducing FBLearner Flow: Facebook’s AI backbone](https://engineering.fb.com/core-data/introducing-fblearner-flow-facebook-s-ai-backbone/)
  - [Facebook’s FBLearner Platform (Podcast)](https://twimlai.com/twiml-talk-197-facebooks-fblearner-platform-with-aditya-kalro/)
+ Michelangelo:
  - [Meet Michelangelo: Uber’s Machine Learning Platform](https://eng.uber.com/michelangelo-machine-learning-platform/)
+ Overton:
  - [Overton: A Data System for Monitoring and Improving Machine-Learned Products](https://arxiv.org/abs/1909.05372)
+ Pro-ML:
  - [TWIML Machine Learning Platforms Report][TWIML Report]
  - [Scaling Machine Learning Productivity at LinkedIn](https://engineering.linkedin.com/blog/2019/01/scaling-machine-learning-productivity-at-linkedin)
  - [AI: The LinkedIn Way (Slides)](http://research.baidu.com/Public/ueditor/upload/file/20181015/1539593235969371.pdf)


[TWIML Report]: https://twimlai.com/mlplatforms-ebook/
