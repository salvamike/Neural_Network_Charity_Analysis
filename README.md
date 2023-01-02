# Neural_Network_Charity_Analysis

## Analysis Overview
- Beks, a data analyst, has been tasked with a final project to prove her data abilities. Primarily focusing on neural networks and machine learning. This project focuses on a foundation, called Alphabet Soup, that analysis businesses applying for funding and predicts which businesses to invest in.
## Results
### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
    First, I checked to see if the target is marked as successful in the DataFrame, which suggests that it has been successfully funded by AlphabetSoup.
- What variable(s) are considered to be the features for your model?
     The IS_SUCCESSFUL column is the feature chosen for this dataset.
- What variable(s) are neither targets nor features, and should be removed from the input data?
      The EIN and NAME columns will not increase the accuracy of the model and can be removed to improve code efficiency.
### Compiling, Training, and Evaluating the Model
- How many neurons, layers, and activation functions did you select for your neural network model, and why?
![Screenshot](https://github.com/salvamike/Neural_Network_Charity_Analysis/blob/main/1.png)
In the optimized model, layer 1 started with 120 neurons with a relu activation. For layer 2, it dropped to 80 neurons and continued with the relu activation. From there, the sigmoid activation seemed to be the better fit for layers 3 (40 neurons) and layer 4 (20 neurons).
- Were you able to achieve the target model performance?
  The target for the model was 75%, but the best the model could produce was 72.7%.
- What steps did you take to try and increase model performance?
  Columns were reviewed and the STATUS and SPECIAL_CONSIDERATIONS columns were dropped as well as increasing the number of neurons and layers. Other activations were tried such as tanh, but the range that model produced went from 40% to 68% accuracy. The linear activation produced the worst accuracy, around 28%. The relu activation at the early layers and sigmoid activation at the latter layers gave the best results.
  ![Screenshot](https://github.com/salvamike/Neural_Network_Charity_Analysis/blob/main/2.png)
## Summary
  The relu and sigmoid activations yielded a 72.7% accuracy, which is the best the model could produce using various number of neurons and layers. The next step should be to try the random forest classifier as it is not as likely to be influenced by outliers.