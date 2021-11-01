# Neural_Network_Charity_Analysis

## Overview of Analysis

### Purpose

The purpose of this analysis was to help Alphabet Soup’s foundation predict where to make investments. 
used machine learning and neural networks to help Beks create a binary classifier that is capable of predicting whether applicants will be successful if funded by Alphabet Soup. For this analysis, I was provided a CSV containing over 34,000 organizations that have received funding from Alphabet Soup over the years. Included within that dataset were a number of columns that captured metadata about each organization.


## Results
Below, please find the results of the analysis:

### Data Preprocessing
- What variable(s) are considered the target(s) for your model?
 
  The "IS_SUCCESSFUL" column. 

- What variable(s) are considered to be the features for your model?
  
  Each of the the columns within the dataset are considered features, except for the "IS_SUCCESSFUL," "EIN," and "NAME" columns.

- What variable(s) are neither targets nor features, and should be removed from the input data?
  
  The "EIN" and "NAME" columns.

### Compiling, Training, and Evaluating the Mode 
- How many neurons, layers, and activation functions did you select for your neural network model, and why?

There were two hidden layers. The first layer had 80 neurons and the second had 30. The first and second hidden layers had the Relu activation function and the activation function for the output layer is Sigmoid.

<img width="1142" alt="Hidden_Layers" src="https://user-images.githubusercontent.com/85654649/139744745-3ef5de48-efcd-4678-b9bc-f99cd34f54c5.png">

- Were you able to achieve the target model performance?

  No, the model was unable to achieve the target model performance of 75% accuracy. The model achieved 63% accuracy.

  <img width="767" alt="accurracymodel" src="https://user-images.githubusercontent.com/85654649/139745247-4d7a4790-5197-4a17-b96e-4c5e5af4887b.png">

- What steps did you take to try and increase model performance?

  First, I tried to remove an additional feature, the "USE_CASE" column. This did not improve the performance, but reduced it to 62%.

  <img width="830" alt="attempt1_62percentaccuracy" src="https://user-images.githubusercontent.com/85654649/139746126-a0208dd8-5ee3-447d-b45a-302027bc4c44.png">


  <img width="798" alt="dropusecasecolumn" src="https://user-images.githubusercontent.com/85654649/139745752-2bfef14b-3e01-46f8-9a71-11739f3663ed.png">

  Next, I tried to add neurons and additional hidden layers. This improved the model slightly by increasing the accuracy to 64%.
  
  <img width="1039" alt="attempt2hiddenlayersneurons" src="https://user-images.githubusercontent.com/85654649/139747293-456ff964-a815-489d-adca-89976b9890cb.png">

  <img width="788" alt="attempt2accuracy64" src="https://user-images.githubusercontent.com/85654649/139747309-746b0aff-1625-4964-b7cc-b9f007dd82cd.png">

 Lastly, I tried changing the activation function of the output layer from Sigmoid to Tanh. The accuracy of the model went down to its lowest at 47%.
 
 <img width="1041" alt="attempt3tahn" src="https://user-images.githubusercontent.com/85654649/139748307-c6df2363-8457-45ba-80a6-0125e6dcfe5a.png">

 <img width="756" alt="attempt3accuracy47percent" src="https://user-images.githubusercontent.com/85654649/139748356-ed2e6d05-6023-433c-8e0b-b862d12c66a1.png">

 
## Summary
Based on the analysis, 
Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.
