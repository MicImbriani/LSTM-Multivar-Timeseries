# _[COMPLETED]_
# Multi-Variate Time Series Regression with LSTM for Seoul Bike-Renting Dataset
<p>
In this project I work on an LSTM implementation for making a regression prediction on the number of bikes to be made available for rental. 
The problem is a multi-variate time-series regression supervised problem.
Keras with Tensorflow backend used.<br>
  For a more thorough discussion of the dataset, architecture choice, methods, design and implementation, see "Discussion.pdf" file 
  <br>
  There are two .csv files for the dataset: "SeoulBikeData.csv" is the original file provided in the download (see link below), while "SeoulBikeData2.csv" is a modified version with oneextra column at the end with the month of the datapoint. 
</p>

<h1>Layers</h1>
<p>
Several architectures were tested with 2, 3, 4 and 5 layers each.
The architecture with 3 layers produced the best results, with:<br>
val RMSE = 290.6013<br>
test RMSE = 303.2519 <br>
val RAE = 209.757<br>
test RAE = 222.0884</p>
<br><br>

<h1>Hyperparameters</h1>
<p>
Keras Tuner and Hyperband module were employed to find the optimal parameters. <br>
  It generated an optimal result of 192 neurons for the first layer, 352 neurons for the second layer and 448 neurons for the third layer. All layers have a bias neuron which is initialised at zero.
</p>
Dataset Donwload: http://archive.ics.uci.edu/ml/datasets/Seoul+Bike+Sharing+Demand
Eploratory Analysis Notebook based on: https://www.kaggle.com/srvmig/seoulbike
