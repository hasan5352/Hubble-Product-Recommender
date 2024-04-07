# Hubble-ProductRecommender
- This project is built on scikit-learn, pandas and nltk libraries of python
### The Data:
- The model operates on both numerical, and categorical data. The data contains 9 features, over 500k instances/products with more than 30% having missing values in atleast one feature. The instances are divided into 109 sub categories and 20 main categories of products. 
- The data used is a product sales dataset retrieved from - **[Kaggle](https://www.kaggle.com/datasets/lokeshparab/amazon-products-dataset)**   
- After downloading and extracting the dataset, delete the Amazon-products.csv in it and paste the dataset in the same folder as the model file. 

### The Process
### The Process:
  1. Collected datasets from a specified directory and transformed them into pandas DataFrames.
  2. Combined dataframes and important features, cleaned the data and stemmed the combined important features.
  3. Used the Bag of Words technique for vectorization of instances (movies) into 5000-dimensions
  4. Generated a similarity matrix with distances of each movie to every other movie. Each array in vector represents a movie.
  - The distance metric used to calculate distance between the movies is cosine similarity
  5. Implemented a recommendation algorithm to suggest the most similar movies based on a given movie name

    
1. Transform the datasets into pandas dataframes and clean the data.
1. Employ Univariate Imputation using mean on a subcategory basis to account for potential variations in feature means across different subcategories
  * I will update this to Multivariate Imputation
1. Apply CCA for values missing completely at random (MCAR)
1. Normalize numerical data due to skewness and presence of outliers
1.  


1.  Generated a similarity matrix with distances of each movie to every other movie. Each array in vector represents a movie.
  - The distance metric used to calculate distance between the movies is cosine similarity
