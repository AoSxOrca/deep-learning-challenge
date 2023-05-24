# Analysis report for Alphabet Soup Charity

##Overview of the Analysis:

This project attempts to develop a tool which helps to select the applicants for funding with the best chances of success in their ventures using machine learning and neural networks.
    
Bucketing of data, removal of non-essential columns, application of neural networks, training, transformation and fitting the data, determination of accuracy and loss was done.


### Initial Features:

   * **EIN and NAME** — Identification columns 
   * **APPLICATION_TYPE** — Alphabet Soup application type 
   * **AFFILIATION** — Affiliated sector of industry 
   * **CLASSIFICATION** — Government organisation classification 
   * **USE_CASE** — Use case for funding 
   * **ORGANIZATION** — Organisation type 
   * **STATUS** — Active status 
   * **INCOME_AMT** — Income classification 
   * **SPECIAL_CONSIDERATIONS** — Special considerations for application 
   * **ASK_AMT** — Funding amount requested 
   * **IS_SUCCESSFUL** — Was the money used effectively

## Data Preprocessing:

* What variable(s) are the target(s) for your model? 
  
    **IS_SUCCESSFUL** column was used as target for the model.
 

* What variable(s) are the features for your model? 

   **APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT** columns have been used for features.


* What variable(s) should be removed from the input data because they are neither targets nor features?
     
  **NAME and EIN** columns have been removed because they are not contributing to the result.


## Compiling, Training and Evaluating the Model:


* How many neurons, layers, and activation functions did you select for your neural network model, and why?

   In my model, the number of neurons varied between 1 and 120, number of hidden layers varied between 1 and 5 layers, three activation functions namely relu, leaky relu and tanh functions were assessed for hidden layers and sigmoid activation function was used for output.

  Based on the pre-processed data, it was understood that the number of input parameters are 43. Hence, the number of neurons in the hidden layers were varied upto 120. Iterations were carried to estimate the loss and accuracy calculations. 

    ### Accuracy calculation for the top three best Hyperparameters:
    ![](Images\capture.PNG)

* Were you able to achieve the target model performance? 
   
   The maximum attained accuracy was 73.3%


* What steps did you take in your attempts to increase model performance? 

  For attaining better accuracy, I varied the number of hidden layers between 1 and 5, I varied the number of neurons in the hidden layers between 1 and 120. I used tanh, relu and leakyrelu activation functions. I also test the model for 20 and 100 epochs. Overall, the best obtained accuracy was 0.73376.


## Summary
Based on the above accuracy, I think that the convergence of the solution has been attained indicating that changing the number of epochs may not play a crucial role. The smoothness of the curve (loss and accuracy) may be improved by changing the other parameters such as changing the number of neurons, changing the number of hidden layers and changing the activation functions. But the overall pattern indicates that the convergence of the solution has been attained and it may be very difficult to increase the accuracy further.

## Recommendation:
A supervised machine learning can be better way to classify the groups and result. Since the number of input parameters are higher, I think a random forest classifier may provide a reliable and accurate result. Performing deep learning algorithm using random forest classifier might provide a better accuracy.