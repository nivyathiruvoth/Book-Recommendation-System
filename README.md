# Book-Recommendation-System
Capstone Project Unsupervised Machine Learning: Recommendation System

# Introduction
Recommendation systems are widely used today to recommend relevant products to users based on their interests. Every consumer Internet company like Netflix, YouTube, etc., requires a recommendation system for efficient functioning. Recommendation systems are crucial in some industries where they can generate a large amount of income when they are efficient. It also helps companies to stand out from their competitors. 

A Book Recommendation System is a type of recommendation system where we have to recommend similar books to the reader based on their interest. This project aims to build different types of book recommendation systems.

# Problem Statement

Given the Book-Crossing dataset that comprises of three files-Users, Books and Ratings. The aim of this project is to build different types of book recommendation
systems. 

# Data Summary

### Books Dataset

* ISBN              
* Book-Title           
* Book-Author          
* Year-Of-Publication  
* Publisher            
* Image-URL-S, Image-URL-M, Image-URL-L 

Books dataset contains information regarding the books. ISBN stands for International Standard Book Number. The Image-URL columns contains links to the coverpage of books. Rest of the features are self-explanatory.

### Users Dataset

* User-ID	
* Location	
* Age

Users dataset contains information regarding the users.

### Ratings Dataset

* User-ID	
* ISBN	
* Book-Rating

Ratings dataset contains information regarding the users.

# Pre-processing

We have three different datasets which contains details of books, users and book ratings. Image-URL colums from books dataset contain no information that helps in the analysis process, hence we consider only the first 5 columns for further process. Users, books, and ratings datasets were merged after imputing missing values, removing duplicates, and correcting and cleaning invalid entries. The final dataset contained both implicit and explicit ratings. But unlike explicit ratings, implicit ratings cannot tell whether a user liked or disliked a book directly. So for this project, we are only considering explicit ratings.

# EDA

Identified most popular book, top authors, top publishers etc.
Carried out city, state and country based analysis to identify the demographic region with heighest number of online readers for amazon.
Performed age based analysis to understand which age group is more in to online reading.

# Recommendation Systems Biult

1. Popularity-Based Recommendation System
2. Simple Recommendation System
3. Author-Based Recommendation System
4. Collaborative Recommendation - k-Nearest Neighbours
5. Collaborative Recommendation- Singular Value Decomposition 

## Conclusion

• The most rated books are The Lovely Bones: A Novel and Wild Animus.

• Top book author with respect to the number of ratings is Stephan King and with respect to the number of books written is William Shakespeare.

• Top publishers on the basis of the number of ratings received for their books are Ballantine Books and Pocket.

• Majority of the readers are of the age bracket 30–40 and most of them are from the countries USA, Texas and Georgia.

• Wild animus is one of the most rated books irrespective of the age.

• Built 5 types of recommendation systems and did evaluation for one of them.

• After evaluation for Collaborative Filtering-Singular Value Decomposition, we obtained recall@5 of 30% and recall@10 of 41%.
