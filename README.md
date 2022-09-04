# Neural_Network_Charity_Analysis

## Overview of the Analysis
The purpose of this project is to assist AlphabetSoup in determining if grant applicants will be successful if they receive funding for their projects. Alphabet Soup has provided a dataset that will be used to create a binary classifier that can predict the success or failure of funding applicants. 

## Results:
### Data Preprocessing
- The target variable for this model is the "IS_SUCCESSFUL" variable
- The features of the model are: "APPLICATION_TYPE",	"AFFILIATION",	"CLASSIFICATION",	"USE_CASE"	"ORGANIZATION",	"STATUS",	"INCOME_AMT",	"SPECIAL_CONSIDERATIONS",	"ASK_AMT"
- The variables that were removed were: "EIN", "NAME"

### Compiling, Training, and Evaluating the Model
- For the first model, I had two hidden layers, the first with 80 neurons and the second with 30 neurons. I used the relu activation function for the hidden layers and the sigmoid activation function for the outer layer:
![Model1_neurons](https://user-images.githubusercontent.com/103215123/188327755-fd2a7d5f-10d9-46a1-8ce4-a9b1010e7ff8.png)

- The target model performance was 75% accuracy, this was not achieved by this first model which achieved just short with 72.6% accuracy:
![Model1_accuracy](https://user-images.githubusercontent.com/103215123/188327879-b3e3e136-d69b-4bbb-827b-282585e7aa47.png)

- The first step I took to optimize the model was to drop an additional variable: "SPECIAL CONSIDERATIONS"
![Model_Opt1](https://user-images.githubusercontent.com/103215123/188328486-b00a3565-2985-47c9-afad-67340440e7a5.png)

- The accuracy achieved was 72.6%:
![Model_Opt1_accuracy](https://user-images.githubusercontent.com/103215123/188328514-2a332b02-7502-4605-b13e-b52dd814a7c5.png)

- The 2nd attempt to optimize the model was to increase the number of epochs to the training regimen from 50 to 100: 
![Model_Opt2](https://user-images.githubusercontent.com/103215123/188328724-24716fc2-421b-4ef7-8afe-036d40eb26e6.png)

- The accuracy increased for the 2nd Optimization model to 72.79%:
![Model_Opt2_accuracy](https://user-images.githubusercontent.com/103215123/188328787-6f20818e-6fed-4d21-98e9-d44236eaf8cc.png)

- The 3rd attempt to optimize the model was to add additional hidden layers:
![Model_Opt3](https://user-images.githubusercontent.com/103215123/188328846-a0826e51-162e-42aa-9e14-43f9c88e4505.png)

- The accuracy for the 3rd attempt to optimize the model was 72.47%: 
![Model_Opt3_accuracy](https://user-images.githubusercontent.com/103215123/188329003-80afb774-d41a-454a-9c87-682a131be65e.png)

## Summary 
This model did not achieve the target predictive accuracy of 75%. The optimization method that seemd to have the most success in increasing the accuracy of this model was increasing the number of epochs in the training regimen.  Another model such as the random forest model could be used to solve this classification problem, since the data is tabular. The predictive accuracy may be similar, but it may be a better option to start with as the random forest model uses less code and can be faster.   








