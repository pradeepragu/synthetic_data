# synthetic_data
The goal is to generate a synthetic tabular dataset using a generative model. This can be an interesting generative AI project and health policy department has great interest in this area.

Here's the dataset of our interest: https://www.cdc.gov/nchs/nhis/2022nhis.htm. You can download the csv file in the link.  Here's the preprocessing step you need to perform.
* Let D be the tabular dataset contained in the csv file.
* There are many observations in D with missing values.
* For each attribute c in D, compute the percentage of missing observation, denoted by MVc, MVc = (# of missing values in c / #total rows) * 100
* If MVc is greater than 20%, we will remove the entire column c from D.
* If the percentage of missing values is smaller than or equal to 20%, we impute the missing values using k-nearest neighbors with k=5.
* Create a jupyter notebook showing the above preprocessing.
* Use Pandas' dataframe and scikit-learn
Given the imputed dataset, you can train a generative model and sample from the trained model to generate a synthetic dataset. A specific model of our interest is a GAN-baesd model called CTGAN. Here's the github repository by the authors of the paper : https://github.com/sdv-dev/CTGAN, and the paper is available at https://arxiv.org/abs/1907.00503
