# Superstore Sales Analysis
##### *PREPARED BY ABRAHAM MAURICE* 

![Sales Analysis again](https://github.com/user-attachments/assets/dc17f806-3985-4f6e-8a51-9c2e6a3602bd)

## Table of Contents

- [PROJECT OVERVIEW](#project-overview)
- [DATA CLEANING PROCESS](#data-cleaning-process)
- [DATA EXPLORATION](#data-exploration)
- [ASSUMPTIONS](#assumptions)
- [RESEARCH QUESTIONS](#research-questions)
- [HYPOTHESIS TESTING](hypothesis-testing)
- [SUMMARY](#summary)
- [RECOMMENDATIONS](#recommendations)

---

### PROJECT OVERVIEW 
The superstore dataset provides sales and profit data for a variety of products across different categories and regions. 
The goal of this project is to analyse the data and identify insights that can help the company improve its business performance. 
Specifically, I aim to answer questions such as: which regions have the highest sales and profit? Which product categories are the most profitable? What are the most profitable products? 
By answering these questions, I hope to provide recommendations for the company on how to optimize its products offerings and improve its revenue and profitability. 

### DATA CLEANING PROCESS
- Once I have defined the problem, I need to gather the data I’ll need to analyse and also clean the data to ensure it is accurate, complete, and consistent. 
- Here is the primary dataset used for this analysis : [Superstore Dataset](https://www.kaggle.com/datasets/vivek468/superstore-dataset-final)

 #### TOOLS 
- I will use the Jupyter notebook in Python environment for the data cleaning process. 😃 💻
- The libraries I will be using includes:
  1. Pandas for *data cleaning and analysis.*
  2. Matplotlib.pyplot for *visualisation.*

One of the most used method for getting a quick overview of the DataFrame, is the head() method. The head() method returns the headers and a specified number of rows (default number of rows = 5), starting from the top.

Let's view the first five rows of our dataset.

![Data Sample](https://github.com/user-attachments/assets/c1149692-f7f6-43d3-98ce-c9b761ebd74d)

### DATA EXPLORATION
I will explore the dataset to get a sense of what it contains.
This would involve calculating basic statistics, creating exploratory analysis techniques and creating visualisations.

The data.info() method allows me to get some informations about our data including the number of rows and columns, missing values and data types.

![Data Info](https://github.com/user-attachments/assets/f0c17e17-043c-46c3-873c-864a2e055491)

##### Missing Values and Duplicates
I will check the data for missing values and duplicates using the isnull().sum() and duplicated.any() methods respectively:
![Null values](https://github.com/user-attachments/assets/f0dcb32d-d343-4179-806b-00fab0db0e02)


![Duplicates](https://github.com/user-attachments/assets/1b63dd87-980b-4551-b578-fca9b3916768)

The ouputs show that there are no missing values or duplicates in the dataset. 

I would love to get an overall statistics about the data. The describe() method returns description of the data in the DataFrame.

If the DataFrame contains numerical data, the description contains these information for each column:

- count - The number of not-empty values.
- mean - The average (mean) value.
- std - The standard deviation.
- min - the minimum value.
- 25% - The 25% percentile.
- 50% - The 50% percentile.
- 75% - The 75% percentile.
- max - the maximum value.

![Overall statistics](https://github.com/user-attachments/assets/d59b276d-c53e-44b3-981f-7bce39033958)


##### Drop Unnecessary Columns
![drop unnecessary columns](https://github.com/user-attachments/assets/6f934855-ea6b-4f08-8f94-068f5aeb142c)

_**Row ID, Order ID, Customer ID, Postal Codes**_; These columns have been dropped since I won't be needing them for my analysis.

The columns have been reduced from 21 to 17.

![Columns update](https://github.com/user-attachments/assets/22efe098-72fa-477b-85d8-1f0aca5101c8)


### ASSUMPTIONS

- The superstore dataset contains a representative sample of all transactions conducted by the store during the time period covered by the dataset. 

- The data in the superstore dataset is accurate and has been cleaned and preprocessed prior to analysis. 

- The superstore dataset covers a sufficient time period to allow for the identification of patterns or trends in sales and profitability. 

- The superstore dataset is not impacted by any significant outliers or anomalies that could skew the results of any analysis conducted on the dataset. 

 
### RESEARCH QUESTIONS 
I am interested in understanding which factors contribute to high sales in the Super Store. 

- **Which product categories have the highest profit margins in the Super Store?**
- **Are there any significant differences in sales between the East region and other region?**
- **How do sales vary by product category during different months of the year?**
- **How do sales and profit vary by product category on weekdays compared to weekends?** 

Building on these research questions, a set of hypotheses have been formulated and will be tested for validation: 

#### HYPOTHESES 

- _Hypothesis 1: Technology products have the highest profit margin compared to other product categories._

- _Hypothesis 2: East region has the highest sales compared to other regions._ 

- _Hypothesis 3: Sales are higher during certain months of the year._

- _Hypothesis 4: The company’s profit is more on weekdays than on weekends._

### HYPOTHESIS TESTING
![Hypothesis 1 code](https://github.com/user-attachments/assets/4377cef1-0eab-4225-b214-87d417f855f9)
![Hypothesis 1 chart](https://github.com/user-attachments/assets/a9785463-31d7-4fcd-b7fe-219f2b425072)

**RESULT 1**: The hypothesis is supported as technology products have the highest profit margin of the three categories. 

---

![Hypothesis 2 code](https://github.com/user-attachments/assets/8805b830-bdda-4f49-98b8-eacb629a155e)
![Hypothesis 2 chart](https://github.com/user-attachments/assets/051cb950-00ee-472a-8fe5-e14e12c0c997)

**RESULT 2**: The hypothesis is **not** supported as the East region does not have the highest sales compared to other regions. 
The bar chart shows that the West region has the highest sales. 

---

![Hypothesis 3 code](https://github.com/user-attachments/assets/63e5b204-43ad-43d3-9aee-83f8a74ae5c4)
![Hypothesis 3 chart](https://github.com/user-attachments/assets/ec1c532b-fa1d-42c6-a160-d192d6e3567c)

**RESULT 3**: The hypothesis is supported as sales are higher during certain months of the year.

---

![Hypothesis 4 code](https://github.com/user-attachments/assets/4e2a1cec-3c46-413c-ae3f-cdf3ed77b148)
![Hypothesis 4 chart](https://github.com/user-attachments/assets/972856bd-e4ce-4b71-9baa-59cc2b7f7068)

**RESULT 4**: The hypothesis is **not** supported as the company does not make more profit on weekdays than on weekends. On the contrast, we can clearly see that the highest profit made is on Sunday while the lowest is on Wednesday.

---


### SUMMARY 
Based on the analysis, it can be concluded that: 

- Technology products have the highest profit margin compared to other product categories. 

- The East region does not have the highest sales compared to other regions. The data shows that the West region has the highest sales. 

- Sales are higher during certain months of the year. However, the hypothesis that the company’s profit is more on weekdays than on weekends is not supported by the data. 

These conclusions provide valuable insights into the company’s performance and can guide future decision-making processes. 

It is important to note that further investigation may be required to fully understand the underlying factors influencing these observations. 

 
### RECOMMENDATIONS 

- The company should focus on developing and promoting technology products to increase its profits. They could also consider reducing the production and promotion of products with lower profit margins. 

- West region has the highest sales compared to other regions. Therefore, the company could consider increasing its focus on this region. For the other regions, the marketing and sales strategies should be re-evaluated. 

- The company should focus on maximizing sales during the months of November and December. This could involve increasing the inventory of popular products during this time, running target marketing campaigns, and offering discounts to customers. 

- The company should also consider strategies to maintain sales during other months, such as introducing new products or offering promotions and discounts during slower months. 

 
![Thank you](https://github.com/user-attachments/assets/bd1f7839-a002-4e31-a0eb-15de1350f284)
