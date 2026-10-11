<h1><center>Kindle Book Recommendation Engine</center></h1>
<br> 

## 📄Problem Statement
The project aim is to create an intelligent Book Recommendation System that helps users discover relevant books based on their reading preferences, and historical rating behavior. Using book metadata, user information, and rating data, the system aims to analyze patterns in reader behavior and generate personalized recommendations.
<br>

## 🎯Objective
The objective of user specific book recommendation includes personalised recommendations, improved user experience, increased user engagement, and new book discovery.
<br>

## 🔢Dataset
Three datasets, namely Books, Users, and Ratings, were used as the primary inputs for the recommendation system.
- **Books**: `ISBN`, `Book-Title`, `Book-Author`, `Year-Of-Publication`, `Publisher`, `Image-URL-S`, `Image-URL-M`, `Image-URL-L`
- **Users**: `User-ID`, `Location`, `Age`
- **Ratings**: `User-ID`, `ISBN`, `Book-Rating`
<br>

### Dataset Description
`ISBN` - International Standard Book Number (ISBN) that uniquely identifies the book <br>
`Book-Title`- Title of the book <br>
`Book-Author` - Author of the book <br>
`Year-Of-Publication` - Year of publication of the book <br>
`Publisher` - Name of the book publishing company <br>
`Image-URL-S` - URL to small-sized book cover image <br>
`Image-URL-M` - URL to medium-sized book cover image <br>
`Image-URL-L` - URL to large-sized book cover image <br>
`User-ID` - Unique identifier of the book reader <br>
`Book-Rating` - Reader's rating of the book on a scale from 0 to 10 <br>
`Location` - Geographic location of the book reader <br>
`Age` - Age of the book reader in years <br>
<br>

## 🧹Data Cleaning & Transformation
- Converting Columns to Appropriate Data Types 
    - `Year-Of-Publication` - Datatype converted from text to number
- Missing value imputation
    - `Age` - Mean-based imputation of missing values
- Created new columns
    - `Country` - Extracted country details from the `Location` column
    - `age_group` - Categorization of age groups by binning
- Clean categorical values
    - `Country` - Correction of spelling inconsistencies and redundancies in country
<br> 

## 📁 Repository Structure
```
├──input/
│  ├──Books.csv
│  ├──Ratings.csv
│  ├──Users.csv
│  ├──transformed/
|  |  ├──book_pivot.pkl
|  |  ├──books_content.pkl
|  |  ├──books_with_rating_fil.pkl
|  |  ├──countries.xlsx
├──output/
│  ├──plots/
|  |  ├──Authors with highest number of books written.png
|  |  ├──Books with highest number of ratings.png
|  |  ├──Countries with highest number of readers.png
|  |  ├──Distribution plot of book ratings.png
|  |  ├──Distribution plot of reader age.png
|  |  ├──Publishers with highest number of books published.png
|  |  ├──Year-wise Distribution of Published Books.png
│  ├──popularity based recommendations/
|  |  ├──popular_book_recommendations.xlsx
│  ├──country based recommendations/
|  |  ├──United States_popular_book_recommendations.xlsx
|  |  ├──United Kingdom_popular_book_recommendations.xlsx
|  |  ├──Canada_popular_book_recommendations.xlsx
│  ├──author based recommendations/
|  |  ├──Stephen King_popular_book_recommendations.xlsx
|  |  ├──Nora Roberts_popular_book_recommendations.xlsx
|  |  ├──Danielle Steel_popular_book_recommendations.xlsx
│  ├──publisher based recommendations/
|  |  ├──Warner Books_popular_book_recommendations.xlsx
|  |  ├──Berkley Publishing Group_popular_book_recommendations.xlsx
|  |  ├──Ballantine Books_popular_book_recommendations.xlsx
│  ├──year based recommendations/
|  |  ├──1987_popular_book_recommendations.xlsx
|  |  ├──1991_popular_book_recommendations.xlsx
|  |  ├──2003_popular_book_recommendations.xlsx
│  ├──age_group based recommendations/
|  |  ├──Youth_popular_book_recommendations.xlsx
|  |  ├──Middle aged adults_popular_book_recommendations.xlsx
|  |  ├──Elderly_popular_book_recommendations.xlsx
│  ├──title based recommendations/
|  |  ├──cosine ratings/
|  |  |  ├──A Beautiful Mind The Life of Mathematical Genius and Nobel Laureate John Nash book_recommendations.xlsx
|  |  |  ├──similarity_scores.pkl
|  |  ├──cosine contents/
|  |  |  ├──A Beautiful Mind The Life of Mathematical Genius and Nobel Laureate John Nash book_recommendations.xlsx
|  |  |  ├──similarity_scores.pkl
|  |  ├──nn ratings/
|  |  |  ├──A Beautiful Mind The Life of Mathematical Genius and Nobel Laureate John Nash book_recommendations.xlsx
|  |  |  ├──model.pkl
|  |  ├──hybrid/
|  |  |  ├──A Beautiful Mind The Life of Mathematical Genius and Nobel Laureate John Nash book_recommendations.xlsx
│  ├──reader based recommendations/
|  |  ├──cosine ratings/
|  |  |  ├──11676 book_recommendations.xlsx
|  |  |  ├──similarity_scores.pkl
|  |  ├──cosine contents/
|  |  |  ├──11676 book_recommendations.xlsx
|  |  |  ├──similarity_scores.pkl
|  |  ├──nn ratings/
|  |  |  ├──11676 book_recommendations.xlsx
|  |  |  ├──model.pkl
|  |  ├──hybrid/
|  |  |  ├──11676 book_recommendations.xlsx
├──kindle book recommendation system.ipynb
├── 📄 README.md
```