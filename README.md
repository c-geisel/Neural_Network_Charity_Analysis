# Neural Network Charity Analysis

[Original Model](https://github.com/c-geisel/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity.ipynb)

[Model Optimization Trial](https://github.com/c-geisel/Neural_Network_Charity_Analysis/blob/main/AlphabetSoupCharity_Optimization.ipynb)

## Overview of the analysis: 
Alphabet Soup is a philanthropic organization that has donated 10 billion dollars to different organizations in the past 20 years. The goal of this organization is to improve the world and they do this through their donations. Some of the donations made have not always led to success of a company. This analysis is thus completed to analyze past data on donations made and make a model that will predict if a donation will be successful based on a variety of factors. 

## Results: 
### Data Preprocessing
The target variable of this model is the "IS_SUCCESSFUL" column with a 1 referring to the donation being successful and a 0 referring to that organization’s donation not being successful. With this being said, almost all other columns beside this one are the features of our model. However, there are two columns that are not feature columns or target variables, and those are the "EIN" and "NAME" columns. These both are identifiers for an organization and have no impact on the successfulness of the outcome and thus are dropped from the data frame. 

### Compiling, Training, and Evaluating the Model
Two models are made to decide on the successfulness of a donation. In the first iteration of the model, two hidden layers are used, the first with 80 neurons, and the second with 30 neurons. This number of neurons are used because there are 43 input features. This provides plenty of opportunities for the model to identify the correct weights to use. Along with these layers, the ReLU function is used in the hidden layers. ReLU is used as the data is positive, but also nonlinear. The output layer uses a sigmoid function since a binary classification result is desired. 

![model.png](Resources/Images/model.png)

The first model with these specifications has a 72.6% accuracy which does not achieve the target performance of 75%. 

![accuracy.png](Resources/Images/accuracy.png)

### Increasing Model Accuracy
To try and increase the model performance, 3 changes were made in a second iteration of the model. First, the "STATUS" column is dropped. When a value counts method is performed on this column it shows 34,294 counts are an active status, and only 5 have a non-active status. Because much of the column has a similar value is does not have much effect on the effectiveness of a result and thus it is removed. Another change that is made is changing the "sigmoid" function in the output layer to be a "tanh" function. This is used as it expands the possible output range. Finally, a third output layer is used as it assists the model in identifying nonlinear characteristics of input data without requiring more input data.

![model_optimized.png](Resources/Images/model_optimized.png)

With these changes made, the model had an accuracy of 72.68% which raises the accuracy only by 8 ten-thousandths but still does not raise the accuracy to 75%. However, this new optimized model does display less signs of overfitting. 

![accuracy_optimized.png](Resources/Images/accuracy_optimized.png)

## Summary: 
Overall, the deep learning neural network models fell short of reaching the accuracy goals. More changes could be implemented to improve the models such as dropping or bucketing more columns, using less neurons/hidden layers, or trying various activation functions. However, the neural network may not be the best choice for this dataset and another type of model could be tested. A recommendation for another model to use would be a random forest model. This model combines weak decision trees to make a robust final decision. They are easy to interpret and can handle outliers and nonlinear data. Also, Random Forest models run with the same or higher accuracy at a much faster rate than a deep learning model.
