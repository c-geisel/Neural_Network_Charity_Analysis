# Neural Network Charity Analysis

[Original Model](https://github.com/c-geisel/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb)

[Model Optimization Trial](https://github.com/c-geisel/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimization.ipynb)

## Overview of the analysis: 
Alphabet Soup is a philanthropic organization that has donated 10 billion dollars to different organizations in the past 20 years. The goal of this organization is work to improve the world and they do this through their donations. Some of the donations made have not always led to success of a company. This analysis is thus completed in order to analyze past data on donations made and make a model that will predict if a donation will be successful based on a variety of factors. 

## Results: 
### Data Preprocessing
The target variable of this model is the "IS_SUCCESSFUL" column with a 1 referring to the donation being successful and a 0 referring to that organizations donation not being successful. With this being said, almost other columns beside this one are the features of our model. However, there are two columns that are not feature columns or target variables, and those are the "EIN" and "NAME" columns. These both are just identifiers for an organizationa dn have no impact on the successfulness of the outcome and are dropped from the dataframe. 

### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
- Were you able to achieve the target model performance?
- What steps did you take to try and increase model performance?



![3d_plot.png](Resources/3d_plot.png)

## Summary: 
Summarize the overall results of the deep learning model. 
Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
