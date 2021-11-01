# Neural_Network_Charity_Analysis


## Overview of Analysis

Using machine learning, neural networks, and the features in the provided dataset, we are able to create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup.  The CSV provided from Alphabet Soup's busniess team contains more than 34,000 organizations that have received funding from Alphabet Soup over the years.  


## Results

### Data Preprocessing

- What variables are considered the target(s) for your model?

  IS-SUCCESSFUL
  
- What variables are considered to be the features for your model?

  Every column besides the target and the columns that were dropped.  Some examples: APPLICATION_TYPE, CLASSIFICATION, ORGANIZATION, STATUS
  
- What variables are neither targets nor features, and should be removed form the input data?

  EIN and NAME
  
  
### Compiling, Training, and Evaluating the Model

- How many neurons, layers, and activation functions did you select for your neural network model, and why?

Originally, I selected 80 hidden nodes in layer 1 and 30 in layer 2.  The first and second hidden layers used relu activation mode due to the positive nonlinear input data.

- Were you able to achieve the target model performance?

This first attempt was close, with a 72.7% accuracy, but not quite the 75% we were hoping for. 
![image](https://user-images.githubusercontent.com/64279232/139738903-7388938b-b9e5-42a3-b39e-2e2864361bc5.png)


- What steps did you take to try and increase model performance?

I did three attempts with optimization to try to improve the performance of the machine learning algorithm.  See below. 

Attempt #1: 
- added a third hidden layer, with 80 neurons in the first layer, 45 in the second, and 15 in the third
- changed the output layer to a sigmoid activation
![image](https://user-images.githubusercontent.com/64279232/139739491-b54daa2b-06d6-439a-ab87-22ce608daf35.png)

Attempt #2:
- kept the third hidden layer, but adjusted the neurons to 100, 55, and 25
- change the output layer to a tanh activation
- 80 epochs
![image](https://user-images.githubusercontent.com/64279232/139739812-b19598d9-a8dc-4501-97b2-a4277bd5d897.png)

Attempt #3: 
- returned back to two hidden layers with 100 and 50 neurons, respectively
- sigmoid activation for output layer
- 80 epochs
![image](https://user-images.githubusercontent.com/64279232/139740251-da0edc6c-4ab8-4dbe-a5db-cb74933519ae.png)



## Summary

Although we did not reach a 75% accuracy before or after optimization, we did come close given the large dataset and all of the variables.  I think this classification problem can possibly be solved by removing some additional variables or adding more data to possibly increase accuracy.  
