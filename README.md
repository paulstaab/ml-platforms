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

- **Centralized Data Access**:
  Users can easily import data from a central data store, e.g. a Data Warehouse or a Data Lake.
- **Data Pipelines**:
  Users can create pipelines to transform data and generate features. 
  The pipelines are executed automatically.
- **Dataset Management**:
  Users can create an immutable snapshot of a particular state of their data. The snapshot
  is kept as a version and is the basis for running experiments in an reproducible manner.
- **Manual Labeling**:
  The platform offers a way to annotate labels for a dataset, e.g. via a user interface.
- **Label Generation**:
  The platform offers capabilities to automatically generate labels, e.g. via active learning
  or week supervision approaches like SNORKEL. 
- **Feature Repository**:
  User can publish their features in a catalog. It is possible to browse and reuse features
  developed by others.
- **Feature Provenance**:
  It is possible to trace back which data was used to calculate a feature and how much a
  particular feature contributes to model predictions .
- **Backfills**:
  It is possible to calculate new features retrospectively for old versions of the data
  or for previous points in time.

### Model Training and Experiment Management

- **Model Training**: 
  The platform offers a service to train ML models.
- **Distributed Training**: 
  The platform can train a ML model on multiple machines.
- **Experiment Management**: 
  The platform keeps track of experiments and their results.
  Experiments can be reproduced.
- **Model Versioning**:
  The platform keeps track of different versions a model.
- **Auto Feature Generation**:
  The platform can automatically derive new features to optimize the performance of a model.
- **Auto Hyper-parameter Optimization**:
  User can easily optimize the hyper-parameters of an ML algorithm. 
- **AutoML**:
  The platform can automatically select an ML algorithm with good performance.
- **Model Partitioning**:
  Users can define important subsets of the data. These subsets are subject to special treatment
  during model training to optimize the performance on them. 
- **Workflows**:
  Users can combine multiple data processing steps and ML models into a common workflow.
- **Hosted Notebooks**:
  The platforms offers notebooks for users for e.g. data processing and/or modeling. 
- **Model building GUI**:
  The platforms offers a graphical user interface to create ML models.

### Model Deployment and Performance Monitoring 

- **Model Deployment**: 
  The platform can deploy models into a production environment. 
- **Model Serving**: 
  The platform contains a production environment for models. 
  Models can be hosted directly on the platform for inference. 
- **Basic Model Monitoring**: 
  The platform offers basic monitoring for models, e.g. for failures 
  during inference.
- **Concept Drift Detection**:
  The platform can monitor the distributions of model inputs and outputs
  and detect significant changes.
- **Online Experiments**:
  The platform can be used to conduct experiments in the production environment
  like A/B tests.
- **Phased Deployments**:
  The platform execute gradual deployments, e.g. canaries or rolling updates. 
- **Feedback Collection**:
  Developers can confirm if a previously-made prediction was correct or not.
  The information is used to measure and monitor the actual performance of the 
  model in production.
- **Scheduled Retraining**:
  The platform can regularly retrain models with updated data based on a fixed
  schedule.
- **Dynamic Retraining**:
  The platform can detect that a model is outdated, and retrain it when needed. 
- **Batch Scoring**:
  User can easily generate predictions of an existing model for new datasets.  


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
| Productive since         |         | 2014-2016 |              |         |          |
| **Data Acquisition and Feature Management** |
| Centralized Data Access  | ✓       | ✓         | ✓            |         |          |
| Data Pipelines           | ✓       | ✓         | ✓            |         |          |
| Dataset Management       | ✓       |           |              |         |          |
| Manual Labeling          |         |           |              |         |          |
| Label Generation         |         |           |              | ✓       |          |
| Feature Repository       | ✓       | ✓         | ✓            |         | ✓        |
| Feature Provenance       | ✓       |           |              |         |          |
| Backfills                | ✓       |           |              |         |          |
| **Model Training and Experiment Management** |
| Model Training           | ✓       | ✓         | ✓            | ✓       | ✓        |
| Distributed Training     |         |           | ✓            |         | ✓        |
| Experiment Management    | ✓       | ✓         | ✓            | ✓       | ✓        |
| Model Versioning         | ✓       | ✓         | ✓            | ✓       | ✓        |
| Auto Feature Generation  |         |           |              |         |          |
| Auto Hyperparameter Opt. | ✓       |           | ✓            | ✓       |          |
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
| Batch Scoring            | ✓       |           |              |         |          |

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
