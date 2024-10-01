# Bank Marketing Campaign Optimization

This project focuses on optimizing a bank's telemarketing campaign by using machine learning, specifically XGBoost, to predict potential customers who are likely to subscribe to a term deposit. The goal is to improve marketing efficiency by identifying the most relevant customer traits and targeting them effectively, resulting in higher conversion rates, better customer acquisition accuracy, and reduced marketing costs.

## Table of Contents

- [Project Overview](#project-overview)
- [Problem Statement](#problem-statement)
- [Objectives](#objectives)
- [Dataset](#dataset)
- [Machine Learning Model](#machine-learning-model)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [How to Use](#how-to-use)
- [Future Improvements](#future-improvements)
- [Technologies](#technologies)
- [Contributors](#contributors)

## Project Overview

Telemarketing is an effective but costly method for customer outreach, especially when it leads to low conversion rates. This project aims to reduce operational costs and increase the effectiveness of a bank's marketing efforts by building a predictive model that identifies potential customers. The predictive model helps the bank focus its resources on individuals who are most likely to subscribe to a term deposit, thus increasing overall profitability.

## Problem Statement

The bank's current telemarketing strategy is expensive and has a low conversion rate. The challenge is to identify potential customers to target them more efficiently, improving the return on investment (ROI) of the marketing campaigns.

## Objectives

- Identify key demographic and financial characteristics of customers likely to subscribe to a term deposit.
- Develop a predictive machine learning model using XGBoost to improve targeting.
- Provide actionable insights for marketing teams to improve campaign efficiency.

## Dataset

The dataset used for this project contains information on customer demographics, financial status, and previous interactions with the bank's marketing campaigns. Key features include:

1. **Age**:  
   - Type: Numeric  
   - Description: Age of the customer.
   
2. **Job**:  
   - Type: Categorical  
   - Description: Type of job held by the customer.  
   - Categories:  
     - "admin."
     - "unknown"
     - "unemployed"
     - "management"
     - "housemaid"
     - "entrepreneur"
     - "student"
     - "blue-collar"
     - "self-employed"
     - "retired"
     - "technician"
     - "services"
   
3. **Marital**:  
   - Type: Categorical  
   - Description: Marital status of the customer.  
   - Categories:  
     - "married"
     - "divorced" (includes divorced or widowed)
     - "single"
   
4. **Education**:  
   - Type: Categorical  
   - Description: Education level of the customer.  
   - Categories:  
     - "unknown"
     - "secondary"
     - "primary"
     - "tertiary"
   
5. **Default**:  
   - Type: Binary  
   - Description: Whether the customer has credit in default.  
   - Values:  
     - "yes"
     - "no"
   
6. **Balance**:  
   - Type: Numeric  
   - Description: Average yearly balance of the customer in euros.
   
7. **Housing**:  
   - Type: Binary  
   - Description: Whether the customer has a housing loan.  
   - Values:  
     - "yes"
     - "no"
   
8. **Loan**:  
   - Type: Binary  
   - Description: Whether the customer has a personal loan.  
   - Values:  
     - "yes"
     - "no"

### Contact Information (Related to Last Contact of the Current Campaign)

9. **Contact**:  
   - Type: Categorical  
   - Description: Contact communication type used in the campaign.  
   - Categories:  
     - "unknown"
     - "telephone"
     - "cellular"
   
10. **Day**:  
    - Type: Numeric  
    - Description: Last contact day of the month.
    
11. **Month**:  
    - Type: Categorical  
    - Description: Last contact month of the year.  
    - Categories:  
      - "jan", "feb", "mar", "apr", "may", "jun", "jul", "aug", "sep", "oct", "nov", "dec"
    
12. **Duration**:  
    - Type: Numeric  
    - Description: Duration of the last contact in seconds.

### Other Campaign-Related Attributes

13. **Campaign**:  
    - Type: Numeric  
    - Description: Number of contacts performed during this campaign for this client (includes the last contact).

14. **Pdays**:  
    - Type: Numeric  
    - Description: Number of days that passed since the client was last contacted from a previous campaign.  
    - Special value: **-1** means the client was not previously contacted.

15. **Previous**:  
    - Type: Numeric  
    - Description: Number of contacts performed before this campaign for this client.

16. **Poutcome**:  
    - Type: Categorical  
    - Description: Outcome of the previous marketing campaign.  
    - Categories:  
      - "unknown"
      - "other"
      - "failure"
      - "success"

### Target Variable

17. **y (Target)**:  
    - Type: Binary  
    - Description: Whether the client subscribed to a term deposit in the current campaign.  
    - Values:  
      - "yes"
      - "no"

## Machine Learning Model

We utilize XGBoost for this project, a high-performance gradient boosting algorithm that is well-suited for structured data and classification tasks. The model is trained to predict the likelihood of a customer subscribing to a term deposit based on their demographic and financial features.

### Why XGBoost?

- **High Accuracy**: XGBoost is known for its excellent performance in classification tasks.
- **Efficiency**: The model is optimized for both speed and memory usage, making it ideal for large datasets.
- **Flexibility**: XGBoost allows for fine-tuning and handling complex interactions between features.

## Evaluation Metrics

To evaluate the model's performance, the following metrics are used:

- **Accuracy**: The percentage of correctly classified instances.
- **Precision**: The ratio of true positive predictions to all positive predictions.
- **Recall**: The ratio of true positive predictions to all actual positives.
- **F1-Score**: The harmonic mean of precision and recall, providing a balanced measure of the model's performance.
- **AUC-ROC**: A measure of the model's ability to distinguish between classes.

## Results

The XGBoost model demonstrated the following improvements:

- **Higher conversion rate**: By focusing on customers with a high probability of subscribing.
- **Improved accuracy**: Increased accuracy in identifying potential customers for term deposits.
- **Reduced costs**: By targeting only high-potential customers, the overall cost of marketing campaigns was reduced.

## How to Use

### Prerequisites

To run this project, you'll need the following:

- Python 3.x
- Jupyter Notebook or any Python IDE
- Required Python libraries (listed below)

### Installation

Clone the repository:

```bash
git clone https://github.com/your-username/bank-marketing-optimization.git
cd bank-marketing-optimization
