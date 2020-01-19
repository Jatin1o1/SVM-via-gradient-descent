# SVM-via-gradient-descent
This is the implementation of Support Vector Machines via batch, mini batch and stochastic gradient descent

Here we implement the soft margin SVM using different gradient descent methods.

#1 Batch gradient descent: 

Iterate through the entire dataset and update the parameters as follows: k = 0

while convergence criteria not reached do for
j = 1,...,d do
Update w(j) ← w(j) − η∇w(j)f(w,b) end for
Update b ← b − η∇bf(w,b)
Update k ← k + 1 end
while


#2 Stochastic gradient descent: 

Go through the dataset and update the parameters, one training sample at a time, as follows:

Randomly shuffle the training data
i = 1,k = 0
while convergence criteria not reached do for
j = 1,...,d do
Update w(j) ← w(j) − η∇w(j)fi(w,b) end for
Update b ← b − η∇bfi(w,b) Update i
← (i mod n) + 1
Update k ← k + 1
end while

#3 Mini batch gradient descent: 

Go through the dataset in batches of predetermined size and update the parameters as follows:

Randomly shuffle the training data
l = 0,k = 0
while convergence criteria not reached do for
j = 1,...,d do
Update w(j) ← w(j) − η∇w(j)fl(w,b) end for
Update b ← b − η∇bfl(w,b)
Update l ← (l + 1) mod ((n + batch size − 1)/batch size)
Update k ← k + 1 end
while

The dataset contains the following files :
1) features.txt : Each line contains features (comma-separated values) for a single datapoint. It has 6414 datapoints (rows) and 122 features (columns).
2) target.txt : Each line contains the target variable (y = -1 or 1) for the corresponding row in features.txt.
