# Naive Bayes

>Naive Bayes is a probabilistic algorithm used for classification tasks in machine learning. It is based on Bayes' theorem, which provides a way to calculate the >probability of a hypothesis based on the evidence available.
>
>>The basic idea behind Naive Bayes is to calculate the probability of each possible label for a given input, based on the conditional probabilities of each feature >>given each label. The label with the highest probability is then chosen as the predicted label for the input.
>
>>Naive Bayes can be trained on labeled data, where the input is a set of features and the label is the desired output. During training, the algorithm calculates the >>conditional probabilities for each feature given each label. Then, during prediction, it uses Bayes' theorem to calculate the probability of each label given the input >>features, and chooses the label with the highest probability.

**ALGORITHM**

The steps for implementing the Naive Bayes algorithm are as follows:

> 1. Data Preparation: Preprocess the data and split it into training and testing sets.
>
> 2. Feature Extraction: Identify and extract the relevant features for the classification task.
>
> 3. Training: Compute the prior probabilities for each class and the conditional probabilities for each feature given the class.
>
> 4. Prediction: For a given instance to be classified, calculate the probability of it belonging to each class using Bayes' theorem, and select the class with the highest probability as the predicted class.

Mathematical expression is given by:

Discrete Xi:

Train Naive Bayes

for each* value yk

estimate  πk = P(Y =yk)

for each* value of xij of each attribute of Xi

estimate  θijk = P(Xi = xij|Y = yk)

Classify (Xnew) 

> Ynew <-- arg maxyk P(Y = yk)  Πi = P(Xinew | Y = yk)
> 
>  Ynew <-- arg maxyk πk Πi  θijk
>
> Probabilities must sum to 1, so we need to estimate only n-1 parameters.

**Estimating Parameters**: ***Y , Xi*** discrete valued

> Maximum likelihood estimates(MLE's):
> 
> πk  = P(Y = yk) = #D{Y = yk} / |D|
> 
> θijk = P(Xi = xij|Y = yk) = #D{Xi = xij ^ Y = yk}/ #D{Y = yk}
> 
> where #D{Y = yk} = Number of items in set D for which Y = yk

**EXAMPLES**

Here is an example to decide whether to play tennis or not..

![Screenshot (13)](https://user-images.githubusercontent.com/107355282/236604406-08e3d06a-4f3c-40d9-bb0b-71fc4df95511.png)

![Screenshot (14)](https://user-images.githubusercontent.com/107355282/236605779-75d31da1-a438-415f-a84c-c9b2f970480e.png)

In the above eg. we found that the probability for playing tennis is:

P(play = yes) = 9/14

and the probability for not playing tennis is:

P(play = no) = 5/14

**Advantages**

> 1. Naive Bayes is easy to implement and computationally efficient, making it suitable for large datasets and real-time applications.
> 
> 2. It can handle high-dimensional data with a relatively small amount of training data, making it useful in many practical situations where the number of features is >    large.
> 
> 3. It can perform well even when the independence assumption between features is not strictly true, as long as the features are not strongly correlated.
> 
> 4. It is robust to irrelevant features, which means it can handle noisy data and irrelevant variables.

**Disadvantages**:

> 1. Naive Bayes assumes that all features are independent, which may not be true in some cases. This can lead to poor classification accuracy,
>  if the dependencies  between features are strong.
> 2. It is a linear classifier and cannot model complex relationships between features.
> 
> 3. It relies heavily on the quality of the data and the selection of features. Garbage in, garbage out applies to Naive Bayes as well.
> 
> 4. It can suffer from the "zero-frequency problem," where a category or feature that is not represented in the training data
>  will result in a zero probability estimate, making the model unable to make predictions.

> This may tends to overfit.











