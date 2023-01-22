# Neural_Network_Charity_Analysis
System: Google Colab

# Overview
Beck is incharge of data collecting and analysis for a nonprofit organization, AlphabetSoup. AlphabetSoup is a philanthropic foundation deciated to helping organizations that improve the environment, help people's well-being, and unify the world. They have raised and donated $10 million in 20 year. They invest in lifesaving technologies and organize reforestation groups. However, Bec needs to know which group to give the donation to. She knows that the impact of each donation can be but with the risk of some organizations disappearing after receiving the donation she need help create a mathematical data driven soluation that predict which organization is high risk. We are to help her create a deep learning neural network.

# Results

## Data Preprocessing
  - In our original analysis we dropped the columns EIN and NAME because they were not our target variables for our model. Next, we binned columns APPLICATION_TYPE & CLASSIFICATION because they showed "rare" categorical variables, which was successful. As we optimatize our data to get a model with 75% accuracy, we dropped EIN, NAME, SPECIAL_CONSIDERATIONS, and STATUS columns in the optimization files 1 & 2. However with Optimization file 3, we kept the NAME column and replace in the binning code instead of CLASSIFICATION column.
  
![APPLICATION_TYPE graph](https://user-images.githubusercontent.com/108844775/213918387-7df27959-2aaa-4f78-a0dd-3421bdf47c19.png)

![CLASSIFICATION graph](https://user-images.githubusercontent.com/108844775/213918394-b6e1cf08-bc5b-4052-a76a-a8c9bb155543.png)


## Compiling, Training, and Evaluate the Model
![Evaluate](https://user-images.githubusercontent.com/108844775/213918422-34efea97-7905-44d0-af46-e17a761e9ce2.png)
  - Original code, we were only able to get an Accuracy of 72% with a loss of 55%. 
  
![Evaluate_Opt](https://user-images.githubusercontent.com/108844775/213918431-1b745161-e292-42df-8cc2-79d977602364.png)
  - Optimization we were only got an Accuracy of 72.7% and a loss of 55.1%.
  
![Layers](https://user-images.githubusercontent.com/108844775/213918531-39c4346e-972d-4567-8794-bd8b1dd14e0a.png)
  -

![Layer_Opt3](https://user-images.githubusercontent.com/108844775/213918539-e4b38683-ae5d-4b33-9d7c-29cf4a4a19e5.png)
  - We added 3 hidden layers and changed the 

![Train Evaluate_Opt1](https://user-images.githubusercontent.com/108844775/213918514-462a40fb-e151-4d32-9353-5b9c34602de6.png)


![Train Evaluate_Opt3](https://user-images.githubusercontent.com/108844775/213918505-6d9f84ae-b6c9-4e9d-9b16-2049feba91af.png)


# Summary




