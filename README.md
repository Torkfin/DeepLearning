# DeepLearning

**Results**: Using bulleted lists and images to support your answers, address the following questions.

* Data Preprocessing
* What variable(s) are considered the target(s) for your model?

The “Is_Successful” column contains the variables that are considered the targets for the model.  
	
* What variable(s) are considered to be the features for your model?

All the other columns ( EIN, NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS,  INCOME_AMT,	SPECIAL_CONSIDERATIONS and ASK_AMT)
are potential features of the model.	

* What variable(s) are neither targets nor features, and should be removed from the input data?

The EIN and NAME fields are neither target nor features and were removed from the input data.

* Compiling, Training, and Evaluating the Model
* How many neurons, layers, and activation functions did you select for your neural network model, and why?

I tried 2 through 7 layers and varied the units per layer between 10-25.  Tried different number of epochs,  I used relu, tahn, softplus, swish, softmax and elu as different activation functions. My understanding is that it is better to go deep with layers than wide with units so I kept the number of units in the 20-25 range and increased the layers to try to optimize the model.

Were you able to achieve the target model performance?

I was not able to achieve the 75% performance.  The closest I came was 73.05% performance with .54 loss.  

What steps did you take to try and increase model performance?

Along with trying different # of layers, units, activation functions, I tried different optimizers; adam, adagrad, adadelta, and rmsprop.  I also tried a bit of a radical idea and binned the “ASK_AMT” thinking that binning might make that feature a bit more discrete and allow the model to improve.  Binning the ASK_AMT didn’t hurt the model, but it also did not help.

. **Summary**: Summarize the overall results of the deep learning model. Include a recommendation for how a different model could solve this classification problem, and explain your recommendation.

The overall results were a bit disappointing, in that, despite dozens for options for levels, units, acitvators and optimizers, I could not find a model that would generate and accuracy over 73.05%.  Given this is a Supervised data set, you could run general Supervised models on the data like Logistical, RandomForest and AdaBoost Classifier.  They may provide a better result. 
