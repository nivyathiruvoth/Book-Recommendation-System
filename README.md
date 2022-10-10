<p align="center"> 

<img src="Images/logo.png" height="100px">

</p>

<h1 align="center"> Book-Recommendation-System

 </h1>

<h3 align="center"> AlmaBetter Verified Project - <a href="https://www.almabetter.com/"> AlmaBetter School </a> </h5>

<h4 align="center"> Capstone Project Unsupervised Machine Learning: Recommendation System</h4>

<p align="center"> 

<img src="Images/books.png" height="400px">

</p>

<p> </p>

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :floppy_disk: Table of Content</h2>

 
  * [Introduction](#Introduction)
  * [Problem Statement](#Problem-Statement)
  * [Data Summary](#Data-Summary)
  * [Steps involved](#Steps-involved)
  * [Pre-processing](#Pre-processing)
  * [Exploratory Data Analysis](#Exploratory-Data-Analysis)
  * [Algorithms used](#Algorithms-used)
  * [Model Evaluation](#Model-Evaluation)
  * [Conclusion](#Conclusion)


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


<h2> 📄 Introduction</h2>

Recommendation systems are widely used today to recommend relevant products to users based on their interests. Every consumer Internet company like Netflix, YouTube, etc., requires a recommendation system for efficient functioning. Recommendation systems are crucial in some industries where they can generate a large amount of income when they are efficient. It also helps companies to stand out from their competitors.

A Book Recommendation System is a type of recommendation system where we have to recommend similar books to the reader based on their interest. This project aims to build different types of book recommendation systems.


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> ❓ Problem Statement</h2>

Given the Book-Crossing dataset that comprises of three files-Users, Books and Ratings. The aim of this project is to build different types of book recommendation systems.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :book: Data Summary </h2>

There were three datasets containing information regarding more than 50,000 books from amazon.com.

![image](https://user-images.githubusercontent.com/92729412/194911631-25af44b3-fdae-49f9-9980-59db994c6731.png)

Books dataset contains information regarding the books. ISBN stands for International Standard Book Number. The Image-URL columns contains links to the coverpage of books. Rest of the features are self-explanatory.

Users dataset contains information regarding the users.

Ratings dataset contains information regarding the users.


![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :gear: Steps Involved </h2>

![image](https://user-images.githubusercontent.com/92729412/194911208-ae5ab75e-5fc4-4720-8a67-f9e831a95d2d.png)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2>🛠️ Pre-processing </h2>

We have three different datasets which contains details of books, users and book ratings. Image-URL colums from books dataset contain no information that helps in the analysis process, hence we consider only the first 5 columns for further process. Users, books, and ratings datasets were merged after imputing missing values, removing duplicates, and correcting and cleaning invalid entries. The final dataset contained both implicit and explicit ratings. But unlike explicit ratings, implicit ratings cannot tell whether a user liked or disliked a book directly. So for this project, we are only considering explicit ratings.

Final Dataset

![image](https://user-images.githubusercontent.com/92729412/193462037-fafd63a5-787a-41db-afc1-ed5f6a5509b7.png)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :bar_chart: EDA </h2>
 
### 1. MOST RATED BOOKS

![image](https://user-images.githubusercontent.com/92729412/193462256-2637b479-67dc-4c58-8546-e5caf4b4faa8.png)

* 'The Lovely Bones:A Novel' is the book with the highest number of ratings.

* It is followed by 'Wild Animus' and 'The Da Vinci Code'

### 2. Top Book-Authors

![image](https://user-images.githubusercontent.com/92729412/193462301-74e7c76a-1ab3-487a-b393-2665488ac84a.png)

Analyzing the given data, one can conclude that Stephan King's books received the most number of ratings.

### 3. Top 15 Book-Publishers

![image](https://user-images.githubusercontent.com/92729412/193462341-58ddd9d3-588d-4f00-8623-030c54147d82.png)

Top publishers on the basis of the number of ratings received for their books are 'Ballantine Books' and 'Pocket'.

### 4. Number of ratings from each Country

![image](https://user-images.githubusercontent.com/92729412/193462363-8682e8a9-13d6-4f6e-95a9-d6ccab2ee8bc.png)

It can be observed that 77.16% of the ratings is from the Country USA. Now let's check the ratings from each state in USA.

### 5. Age distribution

![image](https://user-images.githubusercontent.com/92729412/193462422-f2b570f0-0b32-447a-939c-e47d44c9d5b5.png)

It can be observed that most of the ratings are given by people of age between 30-40 years. Now let us find out the most rated books by people of different age groups- Teenage, Youth, Middle-age and elderly.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2>💻 Algorithms used</h2>

### 1. Popularity-Based Recommendation System

It is a type of recommendation system which works on the principle of popularity and or anything which is in trend.

![image](https://user-images.githubusercontent.com/92729412/193462783-64203b7e-84a4-4125-9c62-dacb393f66a6.png)

These are the popular books based on the number of ratings received.

### 2. Simple Recommendation System

This method is based on the concept of weighted rating.
![image](https://user-images.githubusercontent.com/92729412/193463267-d24def35-9870-4dfd-94ed-f5efca0a6a59.png)

### 3. Author-Based Recommendation System
This model recommends the top books by the same author.

### 4. Collaborative Recommendation - k-Nearest Neighbours

Collaborative filtering is a technique that helps filter out items for a user in a collaborative way, that is, based on the preferences of similar users. 

KNN is a perfect memory based model for item based. It relies on item similarity.
First we will convert our dataset to a 2D user-item matrix containing ratings as values and fill the missing values with zeros (since we will calculate distances between rating vectors). We then transform the values(ratings) of the matrix data frame into a scipy sparse matrix for more efficient calculations. Then we will fit the model. KNN will calculate the “distance” between the target book and every other book in its database, then it ranks its distances and returns the top K nearest neighbor books as the most similar book recommendations. The algorithm we use to compute the nearest neighbors is “brute”.  We have tried both minkowski and cosine similarity as distance metric.

#### * Cosine Similarity: 

This measures the similarity using the cosine of the angle between two vectors in a multidimensional space. It is given by:

![image](https://user-images.githubusercontent.com/92729412/193464135-14554da7-7919-4d4b-be7c-7f5197409221.png)

If θ = 0°, the ‘x’ and ‘y’ vectors overlap, thus proving they are similar(similarity=1)

If θ = 90°, the ‘x’ and ‘y’ vectors are dissimilar.(similarity=0)

#### * Minkowski Distance: 

Minkowski distance is a distance/ similarity measurement between two points in the normed vector space (N dimensional real space) and is a generalization of the Euclidean distance and the Manhattan distance.

![image](https://user-images.githubusercontent.com/92729412/193464204-a56335dc-f886-46e3-bcbd-13e6cdcae27d.png)

p = 1, Manhattan Distance
p = 2, Euclidean Distance

### 5. Collaborative Recommendation- Singular Value Decomposition 

Singular Value Decomposition (SVD)  is one of the Matrix Factorization models for identifying latent factors.

Matrix Factorization is simply a mathematical tool for playing around with matrices. The Matrix Factorization techniques are usually more effective, because they allow users to discover the latent (hidden)features underlying the interactions between users and items (books).

SVD is a model based approach. It uses a user-item matrix where each row represents a user, and each column represents an item. The elements of this matrix are the ratings that are given to items by users. Unlike other methods, this method is used for personalized recommendation where we will also consider removing those items the user has already interacted with in the recommendation.

Like KNN, we convert our dataset into a 2D matrix (user-item matrix) and fill the missing values with zeros. Then we fit it into the model for dimensionality reduction.

After the factorization, we try to reconstruct the original matrix by multiplying its factors. The resulting matrix is not sparse any more. It generated predictions for items the user has not yet interacted with, which we will exploit for recommendations.

We then transpose this utility matrix, so that the ISBN becomes rows and UserIDs become columns. Then for each user we will sort the books according to the predicted values and recommend top books as most similar books.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :mag: Evaluation </h2>

In Recommender Systems, there are a set of metrics commonly used for evaluation. We choose to work with Top-N accuracy metrics, which evaluates the accuracy of the top recommendations provided to a user, comparing to the items the user has actually interacted in test set.

That is for each user and each item he has interacted in the test set, we take 100 non-interacted items by him. Then we generate recommendations using these 101 items. And will count how many of these interacted items are present within the topN positions. Then we compute recall@N by dividing hit@N-count by the total number of interacted items by the user in the test dataset.

Finally we will aggregate the results of all the users to obtain the global recall@N.

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<h2> :bulb: Conclusion</h2>

• The most rated books are The Lovely Bones: A Novel and Wild Animus.

• Top book author with respect to the number of ratings is Stephan King and with respect to the number of books written is William Shakespeare.

• Top publishers on the basis of the number of ratings received for their books are Ballantine Books and Pocket.

• Majority of the readers are of the age bracket 30–40 and most of them are from the countries USA, Texas and Georgia.

• Wild animus is one of the most rated books irrespective of the age.

• Built 5 types of recommendation systems and did evaluation for one of them.

• After evaluation for Collaborative Filtering-Singular Value Decomposition, we obtained recall@5 of 30% and recall@10 of 41%.

This project will help the company stand out from its competitors and retain customers by enriching the user experience.
 
![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)

<!-- CREDITS -->
<h2 id="credits"> :scroll: Credits</h2>

Nivya T | Avid Learner | Data Scientist | Machine Learning Engineer | Deep Learning Enthusiast

<p> <i> Contact me for Data Science Project Collaborations</i></p>


[![LinkedIn Badge](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/nivyathiruvoth/)
[![GitHub Badge](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/nivyathiruvoth)
[![Medium Badge](https://img.shields.io/badge/Medium-1DA1F2?style=for-the-badge&logo=medium&logoColor=white)](https://medium.com/@nivyathiruvoth)
[![Resume Badge](https://img.shields.io/badge/resume-0077B5?style=for-the-badge&logo=resume&logoColor=white)](https://drive.google.com/file/d/1o5VojatmPA-amnQkOJ-xb6yIq_Jof8D2/view?usp=sharing)

