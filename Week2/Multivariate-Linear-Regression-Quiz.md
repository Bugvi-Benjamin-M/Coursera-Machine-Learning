# Multivariate Linear Regression Quiz

Question 1
----------
Suppose m=4 students have taken some class, and the class had a midterm exam and a final exam. You have collected a dataset of their scores on the two exams, which is as follows:

Midterm Exam | (midterm exam)<sup>2</sup> | Final Exam 
--- | --- | ---
89 | 7921 | 96
72 | 5184 | 74
94 | 8836 | 87
69 | 4761 | 78

You'd like to use polynomial regression to predict a student's final exam score from their midterm exam score. 
Concretely, suppose you want to fit a model of the form hθ(x)=θ<sub>0</sub>+θ<sub>1</sub>x<sub>1</sub>+θ<sub>2</sub>x<sub>2</sub>, 
where x<sub>1</sub> is the midterm score and x<sub>2</sub> is (midterm score)<sup>2</sup>. 
Further, you plan to use both feature scaling (dividing by the "max-min", or range, of a feature) and mean normalization.

What is the normalized feature x<sub>2</sub><sup>(4)</sup>? (Hint: midterm = 69, final = 78 is training example 4.) 
Please round off your answer to two decimal places and enter in the text box below.

Answer: </br>

The mean of x<sub>2</sub> is 6675.5.
The range is 8836 - 4761 is 4075. </br>

x<sub>2</sub><sup>(4)</sup> = (4761 - 6675.5) / 4075 = <b>-0.47</b>

Question 2
----------
You run gradient descent for 15 iterations
with α=0.3 and compute
J(θ) after each iteration. You find that the
value of J(θ) <b>decreases</b> quickly then levels
off. Based on this, which of the following conclusions seems
most plausible?

* Rather than use the current value of α, it'd be more promising to try a larger value of α (say α=1.0).

* Rather than use the current value of α, it'd be more promising to try a smaller value of α (say α=0.1).

* α=0.3 is an effective choice of learning rate.

Answer: </br>

The correct answer is that we should set α=1.0 in order to speed up convergence.

Question 3
----------
Suppose you have m=14 training examples with n=3 features (excluding the additional all-ones feature for the intercept term, which you should add). 
The normal equation is θ=(X<sup>T</sup>X)<sup>−1</sup>X<sup>T</sup>y. 
For the given values of m and n, what are the dimensions of θ, X, and y in this equation?

* X is 14×3, y is 14×1, θ is 3×1

* X is 14×4, y is 14×4, θ is 4×4

* X is 14×4, y is 14×1, θ is 4×1

* X is 14×3, y is 14×1, θ is 3×3

Answer: </br>

We have X is 14×4, y is 14×1, θ is 4×1. Note we have n+1 columns in X due to the extra dimension of x<sub>0</sub>.

Question 4
----------
Suppose you have a dataset with m=10000000 examples and n=200000 features for each example. You want to use multivariate linear regression to fit the parameters θ to our data. Should you prefer gradient descent or the normal equation?

* Gradient descent, since (X<sup>T</sup>X)<sup>−1</sup> will be very slow to compute in the normal equation.

* The normal equation, since it provides an efficient way to directly find the solution.

* Gradient descent, since it will always converge to the optimal θ.

* The normal equation, since gradient descent might be unable to find the optimal θ.

Answer: </br>

We would want to go with gradient descent, as computing the birnak equation would mean that we would have to compute the inverse of an n+1 x n+1 matrix, which would be very computationally expensive - O(n^3).

Question 5
----------
Which of the following are reasons for using feature scaling?

* It speeds up solving for θ using the normal equation.

* It prevents the matrix X<sup>T</sup>X (used in the normal equation) from being non-invertable (singular/degenerate).

* It speeds up gradient descent by making it require fewer iterations to get to a good solution.

* It is necessary to prevent gradient descent from getting stuck in local optima.

Answer: </br>

The statements are false, false, true, false.