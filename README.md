
# Airline Customer Satisfaction Optimization

## Project Overview 

This project uses a Decision Tree to predict customer satisfaction based on various customer attributes. The target variable is binary, Satisfied or Dissatisfied. The goal is to understand which features most strongly influence customer satisfaction and to build a model that can predict satisfaction for new customers.

## Data

The data for this project is simualated airline customer survey responses from 129,880 customers provided by Google as part of the Google Advanced Data Analytics Certificate. It includes data points such as class, flight distance, and in-flight entertainment, among others.

## Code and Resources

- Visual Studio Code
- Python version 3.12.12

## Packages
- EDA - numpy, pandas
- Visualization - matplotlib, seaborn
- Modeling - scikit-learn, train_test_split, 
- Machine Learning - DecisionTreeClassifier, ConfusionMatrixDisplay, classification_report, plot_tree

## Skills
- Data Exploration and Cleaning
- Feature Transformation
- Data Modeling
- Building a Decision Tree Model

## Model Evaluation
**Confusion Matrix**

<img width="525" height="435" alt="Screenshot 2025-12-10 at 8 53 11 PM" src="https://github.com/user-attachments/assets/84b55cb7-a157-4d6e-a203-1a73e08e6ad4" />

**Classification Report**

<img width="332" height="158" alt="Screenshot 2025-12-10 at 8 57 45 PM" src="https://github.com/user-attachments/assets/ae33201c-80a1-40e4-8e97-2dfe3aca0cb8" />

**Accuracy** 
- The model achieves an accuracy of 93%, meaning that 93% of all predictions, both satisfied and dissatisfied customers, were correctly classified. 

**Precision**
- With a precision of 94%, the model correctly identifies satisfied customers 94% of the time, with the remaining 6% representing false positives.

**Recall**
- A recall of 94% indicates that the model successfully captures 94% of all actual satisfied customers (true positives), with the remaining 6% representing false negatives.

**F1** 
- How good is the model at being both accurate when it predicts positive (precision) and thorough in finding positives (recall)? Balances precision and recall
- F1 of 94% shows the model is highly reliable (accurate and consistent) at both correctly predicting satisfied customers and successfully identifying true satisfied customers

## Results and Conclusions

<img width="578" height="650" alt="Screenshot 2025-12-09 at 8 44 51 PM" src="https://github.com/user-attachments/assets/45b8e710-781d-40ec-8131-a461061f53b2" />

**Among all predictors, Inflight Entertainment contributes the most to the model’s predictive performance, as indicated by its highest feature importance score.**

### Decision Tree

<img width="846" height="739" alt="Screenshot 2025-12-10 at 9 12 37 PM" src="https://github.com/user-attachments/assets/19d1a4ea-0109-4abd-bd16-5e4a9e4eee51" />

**Root Node**
- The model selects Inflight Entertainment as the root feature. This confirms that inflight entertainment is the strongest single predictor/first split of customer satisfaction in the dataset.

**Right Branch** 
- Good inflight entertainment is a strong indicator of satisfaction, even when ease of online booking is low (≤ 3.5).
- Certain types of customers (loyal vs. disloyal) are highly correlated with satisfaction.
- High inflight entertainment ratings strongly predict satisfaction, and this effect is reinforced by positive customer experience in online booking and customer type characteristics.

**Left Branch**
- Among customers with inflight entertainment ratings of ≤ 3.5, and seat comfort rating of ≤ 3.5, the model predicts dissatisfaction.
- Low inflight entertainment, when combined with low seat comfort, is the strongest predictor of dissatisfaction. Improvements in seat comfort partially offset negative entertainment ratings.

## Next Steps

Create a partial dependency plot to answer if seat comfort ratings improve by one point would the predicted satisfaction increase?
