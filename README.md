# Sentiment Based Product Recommendation

### Problem Statement

The e-commerce business is quite popular today. Here, you do not need to take orders by going to each customer. A company launches its website to sell the items to the end consumer, and customers can order the products that they require from the same website. Famous examples of such e-commerce companies are Amazon, Flipkart, Myntra, Paytm and Snapdeal.

 Suppose you are working as a Machine Learning Engineer in an e-commerce company named 'Ebuss'. Ebuss has captured a huge market share in many fields, and it sells the products in various categories such as household essentials, books, personal care products, medicines, cosmetic items, beauty products, electrical appliances, kitchen and dining products and health care products.

 With the advancement in technology, it is imperative for Ebuss to grow quickly in the e-commerce market to become a major leader in the market because it has to compete with the likes of Amazon, Flipkart, etc., which are already market leaders.

### Solution

* github link: https://github.com/Dharmender5535/SentimentBasedProductRecommendationDK-/

* Heroku (Application is Live): https://c34-dk.herokuapp.com/

### Built with

*Flask==1.1.2
*nltk==3.6.1
*numpy==1.20.1
*pandas==1.2.4
*gunicorn==20.1.0
*scikit-learn==0.24.1
*xgboost==1.6.1
*Jinja2==3.0.3
*MarkupSafe==2.1.1

### Solution Approach

* Both files dataset along with attribute description are available under dataset\ folder
* Applied Data Cleaning, Visualization and Text Preprocessing (NLP) on the available data set provided in the capstone project. 
  - TF-IDF Vectorizer is used to vectorize the textual data(review_title+review_text). 
  - It measures the relative importance of the word w.r.to other documents
* Dataset was not balanced therefore we used SMOTE Oversampling technique before applying the model
* We tried creating 4 Machine Learning Classification Models (Logistic Regression, Naive Baiyes, Random Forrest, xgboost) are applied on the vectorized data and the target column (user_sentiment). 
 --Objective of this ML model is to classify the sentiment to positive(1) or negative(0). 
 --Best Model is selected based on the various ML classification metrics (Accuracy, Precision, Recall, F1 Score, AUC).
 --xgboost is selected to be a better model based on the evaluation metrics.
*  Colloborative Filtering Recommender system is created based on User-user and item-item approaches.RMSE evaluation metric is used for the evaluation.
*  \SentimentBasedProductRecommendation.ipynb Jupiter notebook contains the code for Sentiment Classification and Recommender Systems
*  Top 20 products are filtered using the better recommender system, and for each of the products predicted the user_sentiment for all the reviews and filtered out the Top 5 products that have higher Postive User Sentiment (model.py)
*  Machine Learning models are saved in the pickle files(under the pickle\); Flask API (app.py) is used to interface and test the Machine Learning models. Bootstrap and Flask jinja templates (templates\index.html) are used for setting up the User interface. No additional Custom Styles used.
*  Final deployment on application is deployed in Heroku 



