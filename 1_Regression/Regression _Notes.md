# Simple Linear Regression 
Business Problem Description 
Salary = f(YearsExperience)
Ordinary Least Squared Method

# Multiple Linear Regression 
Business Problem Description 
Profit = FunctionOf(R&D Spend, Administration Spend, Marketing Spend, State)

- What are the the best start ups in which we should invest ? 
- In which State a startup perform the best ?
 
# Polynomial Regression

# Support Vector Regression (SVR)


# Support Vector Machine (SVM)
- SVM (Support Vector Machine) can be used to do binary classification.
- SVM finds a hyper-plane (line in 2d, plane in 3d, etc) that separates its training data in such a way that the distance between the hyper plane and the closest points from each class is maximized.
- Once SVM finds this hyper-plane, you can classify new data points by seeing which side of this hyper-plane they land on.
- SVM can only be used on data that is linearly separable (i.e. a hyper-plane can be drawn between the two groups) 
- Fear not though, as a common way to make data linearly separable is to map it to a higher dimension (but beware, as this is computationally expensive). 
- You can map it however you want, but there are established ways to do it, they are called Kernels.
- By using a combination of these Kernels, and tweaking their parameters, you'll most likely achieve better results than making up your own way.
- The really cool thing about SVMs are that you can use them when you have very little data compared to the number of features each of your data points has. In other words, when the number of data to the number of features per data ratio is low. Normally when this ratio is low, you experience overfitting, but since SVMs only use a few of your data points to create the hyper-plane in the first place, it doesn't really care that you give it such little data. Note however that accuracy of predictions is reduced when you use very little data. 
- SVMs simply tell you what class a new data point falls in, not the probability that it's in that class. This is of course a disadvantage. 
