# Bias-Variance-for-Underfitting-and-Overfitting

## Underfitted Model

If a model is underfitted, it has high bias and low variance.<br>
This is because its prediction is consistently wrong. (consistent = low variance, wrong = high bias) <br>
Also, it is important to understand that the noises and heterogeneity are the causes of variance.<br>
We may call them in a collective term: variability.<br>
if a model failed to capture enough information, at the same time, it must also failed to capture enough variabilities, therefore, it must also of low variance.<br>  
The argument above may not seem intuitive to all people. You can think that a " $Data_i$ " is the result of " $GroundTruthData_i$ " + some variabilities, eg.
$$Data_i = GroundTruthData_i + \sum_k^M variabilities_k $$
If a model failed to capture $Data_i$, as we expected, it failed to capture the $GroundTruthData_i$, also, we must not forget that it also failed to capture the variabilities, this is to say, the model is not built according to its variabilities and its performance of prediction will not varies much from a test data to another test data.<br>

## Overfitted Model

If a model is overfitted, it has low bias and high variance.<br>
This is because its prediction is built to be extremely fitted to predict the train data but its performance is inconsitent across different test data.
A picture of training process can be of help to our understanding. <br>
![image](https://user-images.githubusercontent.com/108325848/198884638-156f9585-996a-4fb6-bebc-494d17c244b7.png)<br>
In the beginning of training, the major cause of the error in the test data prediction is the bias. <br>
As the training proceeds, more and more information are captured such that the bias is decreased, at the same time more and more variabilities are captured, therefore the error of prediction on test data due to variance is increased. <br>
We see that at certain epoch the variance will start to become the major cause of the error, once this is happening, we can tell that the model has been overfitted. <br>

## Bias-Variance Trade-off
A good model should have low bias and low variance.<br>
However, in most scenario, we can't get the lowest bias and the lowest variance at the same time, so we have to make a trade-off.<br>
We have to choose a point where both the bias and the variance are aceptably low.<br>
This is a point where our model is neither underfitted or overfitted, and also have the lowest error.<br>
We see that this must be the "Optimal Balance" in the last picture, and this is also the point where we should stop our training.(We can get the optimize model by employing early-stopping)

