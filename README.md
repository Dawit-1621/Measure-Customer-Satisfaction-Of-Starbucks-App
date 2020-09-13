# Starbucks-Capstone-Challenge

## Installation
**Importing Libraries**</br>
* numpy
* pandas
* matplotlib
* sklearn
## Project Motivation
Interest in the concept of measuring customer satisfaction is growing. More and more companies want to know how satisfied their customers are. Customer satisfaction drives business success and data scientist provides insight into what customers think. This capstone project is using data provided by Udacity as part of the Data Scientist Nanodegree course. It contains simulated data that mimics customer behavior on the Starbucks rewards mobile app. Periodically, Starbucks sends offers to users that may be an advertisement, discount, or buy one get one free (BOGO). An important characteristic regarding this dataset is that not all users receive the same offer.
The data sets contains three files. The first file describes the characteristics of each offer, including its duration and the amount a customer needs to spend to complete it (difficulty). The second file contains customer demographic data including their age, gender, income, and when they created an account on the Starbucks rewards mobile application. The third file describes customer purchases and when they received, viewed, and completed an offer. An offer is only successful when a customer both views an offer and meets or exceeds its difficulty within the offer's duration.</br> There's also a Medium link with the project summary. https://medium.com/@dawit.hassen/what-is-an-effective-offer-on-the-starbucks-app-3d840bd19b79?sk=d7c5ef3b2e6849018a847d12b2da3d1b
## File Descriptions 
The data is contained in three files:

* portfolio.json - containing offer ids and meta data about each offer (duration, type, etc.)
* profile.json - demographic data for each customer
* transcript.json - records for transactions, offers received, offers viewed, and offers completed

Here is the schema and explanation of each variable in the files:

**portfolio.json**
* id (string) - offer id
* offer_type (string) - type of offer ie BOGO, discount, informational
* difficulty (int) - minimum required spend to complete an offer
* reward (int) - reward given for completing an offer
* duration (int) - time for offer to be open, in days
* channels (list of strings)

**profile.json**
* age (int) - age of the customer 
* became_member_on (int) - date when customer created an app account
* gender (str) - gender of the customer (note some entries contain 'O' for other rather than M or F)
* id (str) - customer id
* income (float) - customer's income

**transcript.json**
* event (str) - record description (ie transaction, offer received, offer viewed, etc.)
* person (str) - customer id
* time (int) - time in hours since start of test. The data begins at time t=0
* value - (dict of strings) - either an offer id or transaction amount depending on the record

**Data Visualization**</br>
* Matplotlib and Seaborn visualization </br>
## Modeling 
There are 2 different models to be built. Since we are predicting whether an offer would be effective or not, this is effectively a binary classification supervised learning model. </br>
* Decision tree classifier model
* Random forest classifier model

## Evaluation 
For evaluation and validation for the model; accuracy and f1 score as the model evaluation metric.</br> F1 score provides a better sense of model performance compared to purely accuracy as takes both false positives and false negatives in the calculation. With an uneven class distribution, F1 may usually be more useful than accuracy.
## Licensing, Authors, Acknowledgements
  I Acknowledge the https://www.starbucks.com/ and https://www.udacity.com. For making the dataset available free for data scientist to exercise on real dataset
