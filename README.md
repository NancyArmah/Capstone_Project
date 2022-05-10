# Capstone_Project
<div align="center">
  
<img src="https://github.com/NancyArmah/Capstone_Project/blob/main/ccfraud.png">
  
</div>
From the moment the e-commerce payment systems came to existence, there have always been people who will find new ways to access someone’s finances illegally. This has become a major problem in the modern era, as all transactions can easily be completed online by only entering your credit card information.

Payment card fraud is a major challenge for businesses, payment card issuers and tranactional service companies. The losses from payment card fraud reached 28.6 billion worldwide in 2019 according to [Nilson Report Data](https://nilsonreport.com/content_promo.php?id_promo=16). United States alone is responsible for more than a third of the total global loss, making it the most card fraud prone country in the world. 

The corona virus pandemic has also fueled an explosive growth in card fraud activity because many consumers and retailers decided it was not worth the risk and pivoted to using their bank cards and phones to make everyday purchases. In the UK, card payments were 75.3% higher in early April 2020 compared with a year earlier, while contactless payment limits also rose to $100, making the switch to contactless even more appealing.

Unfortunately, this rapid change was overshadowed by increased levels of fraud. It impacts consumers, merchants and issuers alike. Its economic cost goes far beyond the cost of illegally purchased merchandise because businesses often spend millions to protect themselves from fraud. Big businesses can absorb some amount of losses but if a small one-shop business or a restaurant all of a sudden has a $10,000 loss, that could be the difference between making payroll and not making payroll for that company.

It should also be noted that fraud detection is a cat and mouse game, where fraudulent patterns change over time. As technology evolves, both in terms of fraud prevention and ease of use of payment systems, so do fraudster techniques. They adapt by moving from the old (and by now fixed) targets to the vulnerability of the new technologies.

Credit card fraud detection (CCFD) is like looking for needles in a haystack. It requires finding, out of millions of daily transactions, which ones are fraudulent. Due to the ever-increasing amount of data, it is now almost impossible for a human specialist to detect meaningful patterns from transaction data. For this reason, the use of machine learning techniques is now widespread in the field of fraud detection, where information extraction from large datasets is required.

Credit Card Fraud Detection with Machine Learning is a process of data investigation and the development of a model that will provide the best results in revealing and preventing fraudulent transactions. This is achieved through bringing together all meaningful features of card users’ transactions. The information is then run through a subtly trained model that finds patterns and rules so that it can classify whether a transaction is fraudulent or is legitimate. 

# Objective

*   Train a Machine Learning Model with historic data to learn patterns behind fraudulent behavior to enable the model filter out fraudulent transactions and stop them from occurring in real-time.

#  Data

Simulated credit card transaction dataset from [Kaggle](https://www.kaggle.com/datasets/kartik2112/fraud-detection) containing legitimate and fraud transactions from the duration 1st Jan 2019 - 31st Dec 2020. It covers credit cards of 1000 customers doing transactions with a pool of 800 merchants.

This was generated using [Sparkov Data Generation | Github](https://github.com/namebrandon/Sparkov_Data_Generation) tool created by Brandon Harris. This simulation was run for the duration - 1 Jan 2019 to 31 Dec 2020. The files were then combined and converted into a standard format.

#Pipiline
* Import Packages
* Import Data
* EDA
* Balance Dataset
* Modelling

# Modelling

SMOTE to handle the imbalance in the dataset
The challenge of working with imbalanced datasets is that most machine learning techniques will ignore, and in turn have poor performance on, the minority class, although typically it is performance on the minority class that is most important. One approach to addressing imbalanced datasets is to oversample the minority class. The simplest approach involves duplicating examples in the minority class, although these examples don’t add any new information to the model. Instead, new examples can be synthesized from the existing examples. This is a type of data augmentation for the minority class and is referred to as the Synthetic Minority Oversampling Technique, or SMOTE for short.

## Supervised Learning Models Used

* Logistic Regression
* Decision Tree 
* XGBoost

Both Decsion Tree and XGboost performed well in the detection of the fradulent transactions with both returning a recall score of 74% as that is what we were modelling for.

# Challenges

Some challenges faced during the project are;

* Lack of public datasets: For obvious confidentiality reasons, real-world credit card transactions cannot be publicly shared. There exists only one publicly shared dataset, which was made available on Kaggle

* Class imbalance: Transaction data contain much more legitimate than fraudulent transactions: The percentage of fraudulent transactions in a real-world dataset is typically well under 1%. Learning from imbalanced data is a difficult task since most learning algorithms do not handle well large differences between classes. 

* Categorical features: Transactional data typically contain numerous categorical features, such as the ID of a customer, a terminal, the card type, and so on. Categorical features are not well handled by machine learning algorithms and must be transformed into numerical features.

# Future Work

* Train a more models to get one that is able to balance between precision and recall score
* Try other sampling techniques
* Include deep learning models
