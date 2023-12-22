# deep-learning-challenge
Overview: 
  The dataset used was based on the Alphabet Soup nonprofit foundation. They fund different organizations and want to      know which organizations will use the money that was funded effectively.
Data Preprocessing:
  For this model, I will be predicting the IS_SUCCESSFUL column, so this will be the target variable. This measures if     the money was used effectively.
  The features will be the all other columns except those that were removed.
  The EIN	and NAME columns will be removed.
Compiling, Training, and Evaluating the Model:
  The first model used two hidden layers with 5 neurons each. This is a basic model that will give a decent accuracy of    about 72%. This will be a good baseline for trying to optimize later. 
  To optimize the model, I first scaled only the ASK_AMT column. Then I used pd.get_dummies on the non numeric columns.    After splitting the data into features and target arrays, I took the target arrays and used a PCA model to eleminate     unuseful columns. This new dataframe along with the target array was used in the train_test_split, which was then fed    into the new neural network model.
  I was also able to optimize the model by adding a third hidden layer and using 7 neurons instead of 5. 
  This was successful in optimizing the model and brought the accuracy up to almost 95%.

NOTE:
  In order to use the model to make predictions, you will need to modify the data the same way I did here. So remove the   necessary columns and use a PCA model with 3 components.  
