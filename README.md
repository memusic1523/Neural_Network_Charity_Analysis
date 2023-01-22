# Neural_Network_Charity_Analysis
System: Google Colab

# Overview
Beck is in charge of data collecting and analysis for a nonprofit organization, AlphabetSoup. AlphabetSoup is a philanthropic foundation dedicated to helping organizations that improve the environment, help people's well-being, and unify the world. They have raised and donated $10 million in 20 years. They invest in lifesaving technologies and organize reforestation groups. However, Bec needs to know which group will be receiving the donation to enhance their organization. She knows what the impact of each donation can be but with the risk of some organizations disappearing after receiving the donation, she needs help creating mathematical data-driven solutions that predict which organization is high risk. We are to help her create a deep-learning neural network.

# Results

## Data Preprocessing
  - In our original analysis, we dropped the columns EIN and NAME because they were not the target variables for our model. Next, we binned columns APPLICATION_TYPE & CLASSIFICATION because they showed "rare" categorical variables, which was successful. As we optimize our data to get a model with 75% accuracy, we dropped EIN, NAME, SPECIAL_CONSIDERATIONS, and STATUS columns in the optimization file 1 & 2. However, with Optimization file 3, we kept the NAME column and replace it with the binning code instead of the CLASSIFICATION column. We preprocessed data into our feature and target array using the IS_SUCCESSFUL column.
  
![APPLICATION_TYPE graph](https://user-images.githubusercontent.com/108844775/213918387-7df27959-2aaa-4f78-a0dd-3421bdf47c19.png)

![CLASSIFICATION graph](https://user-images.githubusercontent.com/108844775/213918394-b6e1cf08-bc5b-4052-a76a-a8c9bb155543.png)


## Compiling, Training, and Evaluate the Model
![Evaluate](https://user-images.githubusercontent.com/108844775/213918422-34efea97-7905-44d0-af46-e17a761e9ce2.png)
  - Original code, we were only able to get an Accuracy of 72% with a loss of 55%. 
  
![Evaluate_Opt](https://user-images.githubusercontent.com/108844775/213918431-1b745161-e292-42df-8cc2-79d977602364.png)
  - Optimization we were only got an Accuracy of 72.7% and a loss of 55.1%.
  
![Layers](https://user-images.githubusercontent.com/108844775/213918531-39c4346e-972d-4567-8794-bd8b1dd14e0a.png)
  -We did 2 hidden layers using the activation function of rectified linear unit (relu) and sigmoid. We want our return a value from 0 to infinite so any negative inputs through the activation function are zero. As for our output, we want to transform the range from -1 to 1 by identifying by characteristic s curve. 

![Layer_Opt3](https://user-images.githubusercontent.com/108844775/213918539-e4b38683-ae5d-4b33-9d7c-29cf4a4a19e5.png)
  - We added 3 hidden layers and more neurons to the hidden layers.

![Train Evaluate_Opt1](https://user-images.githubusercontent.com/108844775/213918514-462a40fb-e151-4d32-9353-5b9c34602de6.png)
 - We removed the third layer to see if we can achieve 75% accuracy, which it did not. Accuracy was 72.4% and loss was 54.8%. 
 
![Train Evaluate_Opt3](https://user-images.githubusercontent.com/108844775/213918505-6d9f84ae-b6c9-4e9d-9b16-2049feba91af.png)
  - Add a third hidden layer, used the Relu function for all layers, and the output layer with use the sigmoid function. Achieve 75% accuracy by adding the NAME column as one of the target variables. We were able to get 79% accuracy and a 42.7% loss. We also changed the count to be greater than 5 when determining which values to replace. (Giving credit to Angelina Macedo, for helping with the idea of changing the dropping column and adding NAME column as the binning variable.)

# Summary
In conclusion, we were able to achieve the 75% accuracy that we wanted however we had to manipulate the deep learning model by using the NAME column which is an identification column. It allows the model to be set up nicely and faster than using the CLASSIFICATION column, which is what we originally wanted to use. We will need to continue to play around with this data set in order to get 75% accuracy using our original features and target values. 

