## Practical Exercise: Scientific Text Classification with the Naive-Bayes Algorithm

### Context: 
You are working as a data analyst for the biomedicine and biotechnology company "BioSyn", where the most cutting-edge research in these fields is conducted. Your team has gathered data on the most important publications in the cancer research area from the past two years to find patterns in the documents for quick identification and documentation within the company’s databases.

### The Challenge:
Use this dataset to design a classification method that allows classifying the large volume of scientific articles into the different cancer types studied and improve the organization and distribution of knowledge within the company.

### Objective:
Based on the provided dataset (Source: https://www.kaggle.com/datasets/falgunipatel19/biomedical-text-publication-classification), your task is to classify each record according to the three considered cancer types: thyroid cancer, colon cancer, and lung cancer. The categorization must be based on an exploratory data analysis and feature extraction from raw text.

---

### Instructions:

#### 1. Exploratory Data Analysis:
##### Exercise 1:
Conduct an Exploratory Data Analysis (EDA) to gather insights about the data and detail the problem to be modeled:
- Declare the dataset size and display a few records on the screen. Rename the variables of the dataset as "Tipo_Cancer" (Cancer_Type) and "Texto_Cientifico" (Scientific_Text).
- What is our target variable? Analyze its distribution (using graphical methods) and reason whether the dataset is well-balanced and how this will affect classification. Argue whether it’s necessary to select prior distributions to balance our data in the problem to be modeled.

#### 2. Feature Extraction:
##### Exercise 2:
We will perform transformations on our raw data to obtain the variables to correctly model the problem:
- Apply a transformation on the target variable to convert it from text to numeric encoding using the **LabelEncoder** method from the **SKLearn** library ([documentation here](https://scikit-learn.org/stable/modules/generated/sklearn.preprocessing.LabelEncoder.html)).
- **Dataset Split**: Segment the data using the **scikit-learn** library, utilizing 75% for the training set and 25% for the testing set. Indicate the size of both sets.
- **Feature Extraction**: Use the **CountVectorizer** method to extract the features for our model and explain how this method works.

#### 3. Model Training:
##### Exercise 3:
Once the features are extracted, we need to build and train the desired model:
- Argue reasonably, based on the distribution of features, which Naive-Bayes model should be applied in this case.
- **Training**: Train the selected model with the training set using the chosen Naive-Bayes algorithm. Use the Laplace smoothing coefficient with an alpha value of 2. Explain in detail the function of this coefficient and its value contribution to the model.
- Build the model in two different ways: First, by applying the **CountVectorizer** transformation to our training data and later using the **Pipeline** method from **sklearn**.

#### 4. Model Evaluation:
##### Exercise 4:
Evaluating the model’s performance is key to understanding its effectiveness. This includes:
- **Comparison of Metrics**: Observe and analyze performance metrics such as accuracy, precision, recall, and F1-score. What conclusions can be drawn from each of these metrics? Justify your answers with reasoned explanations.
- **Confusion Matrix**: Calculate the model’s confusion matrix and analyze the results. What do each of the values represent? In the problem we are modeling, how many records have been correctly and incorrectly predicted for each class? Is it preferable to have a model with higher precision or higher recall? Justify your answer with reasoned arguments.
- **Test Texts for the Model**: Manually generate 3 short texts (one sentence long, in English) to test the model and classify them.
- **Conclusions**: Based on all the observed metrics, how could the model be improved in future iterations? What qualities of the model are most relevant to the text classification problem? From a Bayesian perspective, would it be interesting to include prior and/or subjective information by selecting a specific prior distribution?


