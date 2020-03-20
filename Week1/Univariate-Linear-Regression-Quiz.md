# Machine Learning Week 1 Quiz 2 (Linear Regression with One Variable) Stanford Coursera

Question 1
----------
Consider the problem of predicting how well a student does in her second year of college/university, given how well she did in her first year.

Specifically, let x be equal to the number of "A" grades (including A-. A and A+ grades) that a student receives in their first year of college (freshmen year). We would like to predict the value of y, which we define as the number of "A" grades they get in their second year (sophomore year).

Here each row is one training example. Recall that in linear regression, our hypothesis is h<sub>θ</sub>(x)=θ<sub>0</sub>+θ<sub>1</sub>x, and we use m to denote the number of training examples.

x | y
--- | ---
3 | 4
2 | 1
4 | 3
0 | 1

For the training set given above (note that this training set may also be referenced in other questions in this quiz), what is the value of m? In the box below, please enter your answer (which should be a number between 0 and 10).

Answer: </br>
4

Question 2
----------
Consider the following training set of m=4 training examples:

x | y 
--- | --- 
1 | 0.5
2 | 1
4 | 2
0 | 0

Consider the linear regression model h<sub>θ</sub>(x)=θ<sub>0</sub>+θ<sub>1</sub>x. What are the values of θ<sub>0</sub> and θ<sub>1</sub> that you would expect to obtain upon running gradient descent on this model? (Linear regression will be able to fit this data perfectly.)

* θ<sub>0</sub>=0.5,θ<sub>1</sub>=0

* θ<sub>0</sub>=1,θ<sub>1</sub>=0.5

* θ<sub>0</sub>=0,θ<sub>1</sub>=0.5

* θ<sub>0</sub>=1,θ<sub>1</sub>=1

* θ<sub>0</sub>=0.5,θ<sub>1</sub>=0.5

Answer: </br>
θ<sub>0</sub>=0,θ<sub>1</sub>=0.5 </br>

Question 3
----------
Suppose we set θ<sub>0</sub>=−2,θ<sub>1</sub>=0.5. What is h<sub>θ</sub>(6)?

Answer: </br>

h<sub>θ</sub>(6) = -2 + (0.5)(6) = 1

Question 4
----------
Let f be some function so that

f(θ<sub>0</sub>,θ<sub>1</sub>) outputs a number. For this problem,

f is some arbitrary/unknown smooth function (not necessarily the

cost function of linear regression, so f may have local optima).

Suppose we use gradient descent to try to minimize f(θ<sub>0</sub>,θ<sub>1</sub>)
as a function of θ<sub>0</sub> and θ<sub>1</sub>. Which of the

following statements are true? (Check all that apply.)

* If θ<sub>0</sub> and θ<sub>1</sub> are initialized so that θ<sub>0</sub>=θ<sub>1</sub>, then by symmetry (because we do simultaneous updates to the two parameters), after one iteration of gradient descent, we will still have θ<sub>0</sub>=θ<sub>1</sub>.

* If θ<sub>0</sub> and θ<sub>1</sub> are initialized at a local minimum, then one iteration will not change their values.

* Even if the learning rate α is very large, every iteration of gradient descent will decrease the value of f(θ<sub>0</sub>,θ<sub>1</sub>).

* If the learning rate is too small, then gradient descent may take a very long time to converge.

Answers: </br>

The true statements are <b>#1</b> and <b>#4</b>. <b>#1</b> is true because the gradient at a local minimum will be 0. <b>#4</b> is true because the steps taken by gradient descent will be small, and thus converging on a local minimum can take longer.

Question 5
----------
Suppose that for some linear regression problem (say, predicting housing prices as in the lecture), we have some training set, and for our training set we managed to find some θ<sub>0</sub>, θ<sub>1</sub> such that J(θ<sub>0</sub>,θ<sub>1</sub>)=0.

Which of the statements below must then be true? (Check all that apply.)

* For this to be true, we must have θ<sub>0</sub>=0 and θ<sub>1</sub>=0 so that h<sub>θ</sub>(x)=0.

* For this to be true, we must have y<sup>(i)</sup>=0 for every value of i=1,2,…,m.

* Our training set can be fit perfectly by a straight line, i.e., all of our training examples lie perfectly on some straight line.

* Gradient descent is likely to get stuck at a local minimum and fail to find the global minimum.

Answers: </br>

The only true statement is <b>#43</b>.