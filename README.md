# Module-13-Homework

## Venture Funding with Deep Learning
The task was to read, analyse and compile a model from the csv data provided using neural network. Then this model has to be optimised by employing two additional methods so that the best outcome out of the three models are chosen to arrive at the best target results

## Preparing the data for use on a Neural Network model
After reading the data from the csv file and converting it into a dataframe, the data is cleaned up by dropping some unwanted columns like "EIN' and 'NAME'. Then the non numerical categorical varaibles are listed and encoded using the OneHotEncoder function.
The original numerical data from the dataframe is concacted with the above encoded categorical variable dataframe. 
Then, the datasets are divided into target(y) and features (X) datasets
Using the train_test_split function, the X and y datasets are split into training and testing datasets
Lastlty, the X-train and X-teast datasets are scaled using the Standard Scaler

## Compile and Evaluate a Binary Classification Model Using a Neural Network
I created a deep neural network(named = nn) and using the Dense function imported from tensorflow.keras, added the first and second hidden hidden layers after defining the number of neurons and hidden nodes in the input layers and the output layer.The activation of the input layers was done through 'relu' and the output layer using 'sigmoid' functions
The nn model is compiled using the 'binary_crossentropy' loss function, the 'adam' optimiser and the 'accuracy' evaluation metric
The model is then fitted with the X_train and y_train scaled datasets and 50 epochs. The 50 epoch runs show an increasing accuracy and decreasing loss scores.
The model (with original dataset) is then saved and exported to an HDF5 file

## Optimize the neural network model
The above model with the original dataset is then optimised by creating two different neural network models, naming them nn_A1 and nn_A2
The two new optimised models are created using different feature columns, adding more neurons to the hidden layers, adding more hidden layers, reducing the number of epochs (to 20 in the case of nn_A2) and using a different activation method ()"LeakyReLU' in the case of nn_A2) 
As done in the previous model, the loss and accuracy scores are measured for the two optimised models and the results were exported and saved to HDF5 file