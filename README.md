# USML_recipes


https://docs.google.com/document/d/15kin3AglOZvZFvPoMZIZEdrVKhnuLzx6E7bD0CBOSG0/edit


Project Participants
The participants are Charlie Taggart and Sravani Namburu; we both plan on splitting the project 50/50, with Charlie focusing on EDA, feature extraction, data cleaning, features tuning, and writeup, with Sravani focusing on modelling, its testing and evaluation. 

Problem Description
As someone who likes to cook and try new recipes, we sometimes find ourselves overwhelmed by the number of online sources available when looking up how to prepare something. So many recipe sites are over-inundated with content irrelevant to the recipe itself. They try to garner SEO points by adding stories about the first time they cooked it or why it is their favorite meal. We want a tool to search by a type of cuisine (Italian, Mexican, Chinese, Etc.) and have it auto-generate a unique recipe we can try.  

We aim to use online food recipes and see if we can classify each into a type of cuisine (Italian, Mexican, Chinese, Etc.) using only the ingredient list and instructions. Given that this is an unsupervised learning problem, we will avoid using explicit target labels. However, we will test our model's accuracy using internal evaluation measures (homogeneity completeness, v-measure, rand index, Etc.) 

Additionally, we would like a more qualitative analysis of our model by having it generate a recipe for each cuisine type and try to cook each result to give it a 'taste test' evaluation measure.
Algorithms
We plan on utilizing some classification algorithms discussed in class to see which yield the most accurate results. K-means is one approach, but also spectral clustering and GMM. For the PS2 assignment, we had to classify various article types into different subject matters; we also planned on leaning on the methods used for that problem. This will also require a fair bit of preprocessing, where the data will need to be cleaned, tokenized, and refined. 

The ingredient list also lends itself to interesting market basket findings - we can see the different common itemsets within each cuisine grouping.

Data Sets
There are a few online datasets that have readily available scraped data results. Kaggle has a food.com dataset with 500k+ recipes, broken into features by ingredients, steps, time, and more. We can also attempt to build a web scraping bot to extract these features from a specific website (perhaps Bon appetite and NYTimes cooking, it would be interesting to see if those sources yield different results). Both methods require data cleaning and tokenization to transform the text into model-ready data.

Libraries and Tools
Some of the libraries used will be:
Sklearn.feature_extraction.text CountVectorizer (preprocessing)
Sklearn.feature_extraction.text TfidfVectorizer (preprocessing)
Sklearn.cluser kmeans (algorithm) 
Sklearn.cluser SpectralClustering (algorithm) 
Mlxtend apriori (algorithm)
Sklearn metrics (results)

Results
Ideally, our classification algorithms will be able to group each recipe into a set of cuisine types (Italian, Mexican, Indian, Etc.). We will perform all of the aforementioned internal evaluation measures and query a few examples from each group to qualify results. Finding the appropriate number of clusters, i.e., the 'K' value, will be a key part of this as we do not know how many groups there may be or how robust they are. We will perform visualizations on the grouped datasets as well.

We will also leverage the clusters by extracting a series of top ingredients and steps from each group to generate a machine-built recipe to test (and eat) the result.

