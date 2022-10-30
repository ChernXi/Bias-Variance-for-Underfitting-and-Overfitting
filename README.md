# Bias-Variance-for-Underfitting-and-Overfitting

If a model is underfit, it has high bias and low variance.<br>
This is because its prediction is consistently wrong. (consistent = low variance, wrong = high bias) <br>
Also, it is important to understand that the noise is the cause of variance.<br>
if a model failed to capture enough information, at the same time, it must also failed to capture enough noise, therefore, it must also of low variance.<br>  
The argument above may not seems intuitive to all people. You can think that a " $Data_i$ " is the result of " $GroundTruthData_i$ " + some noise, eg.
$$Data_i = GroundTruthData_i + \sum_k^M noise_k $$
If a model failed to capture $Data_i$, as we expected, it failed to capture the $GroundTruthData_i$, also, we must not forget that it also failed to capture the noises, this is to say, the model is insensitive to the noises and its performance of prediction will not varies much from a prediction to another prediction.<br>
The variance of accuracy of a model in N predictions can be calculated as:
$$Variance = \frac{ \sum_j^N (accuracy_j - accuracy_{average})^2 }{N}$$
By using this formula, you are expected to get a lower variance in an underfit model than in an overfit model, which is credited to the existence of extreme value of accuracy in the overfit model that is highly significant to levelling up the overall variance.

