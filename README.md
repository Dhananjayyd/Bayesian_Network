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
>  Ynew <-- arg maxyk πk Πi  θijk
>
> Probabilities must sum to 1, so we need to estimate only n-1 parameters.

**Estimating Parameters**: ***Y , Xi*** discrete valued
> Maximum likelihood estimates(MLE's):
> πk  = P(Y = yk) = #D{Y = yk} / |D|
> θijk = P(Xi = xij|Y = yk) = #D{Xi = xij ^ Y = yk}/ #D{Y = yk}
> where #D{Y = yk} = Number of items in set D for which Y = yk





**EXAMPLES**






















