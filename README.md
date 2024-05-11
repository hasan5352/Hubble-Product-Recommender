# Hubble-ProductRecommender
- This project is built on scikit-learn, pandas and nltk libraries of python
### Setup
-  Download data from **[Kaggle](https://www.kaggle.com/datasets/lokeshparab/amazon-products-dataset)**. paste it in the same directory as model file and rename as "data".
    - This is for **get_dfs_from_csvs function** to get the data as dataframes.
- Confirm that gitignore file is cloned with its first entry as "data/".
### The Data:
- The data used is a product sales dataset
- The model operates on both numerical, and categorical data. The data contains 9 features, over 500k instances/products with more than 30% having missing values in atleast one feature. The instances are divided into 109 sub categories and 20 main categories of products. 
   
- After downloading and extracting the dataset, delete the Amazon-products.csv in it and paste the dataset in the same folder as the model file. 


### The Process:
  1. Transform the datasets into pandas dataframes and clean the data.
  2. Employ Univariate Imputation using mean on a subcategory basis to account for potential variations in feature means across different sub categories
  3. Apply CCA for values missing completely at random (MCAR)
  4. Normalize numerical data due to skewness and presence of outliers
  5.  Expand the Main Category and the Subcategory features to 20 features and 109 features respectively using One-Hot Encoding due to the ordinal nature of the values in these features.
  6. Sample 20k instances from the dataset using stratified sampling for each Sub Category due to memory constraints.
  7. Use TF-IDF vectorization of instances into 5000-dimensions due to memory constraints
  8. Generate a similarity matrix with cosine of the angle of each product to every other product.
  - The distance metric used to calculate distance between the movies is cosine similarity
  8. Implement a recommendation algorithm to suggest the most similar products based on a given product name

### Further To Dos:
1. Update Univariate Imputation to Multivariate Imputation
2. Fetch the images of the recommended products
3. Deploy model on a website
4. Leverage Deep Learning and Neural Networks for recommendation model
5. Leverage Multi-label Classification to divide the dataset into groups (subcategory wise) so that when a seller lists a product, it directly gets assigned to a group and gets recommneded to users searching for similar products
6. Apply Reinforcement learning for learning
