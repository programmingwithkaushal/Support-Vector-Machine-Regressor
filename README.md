Support Vector Machine Regressor (SVR)
Support Vector Machine (SVM) is a powerful and versatile supervised learning algorithm used for both classification and regression tasks. When adapted for regression, it is known as Support Vector Regressor (SVR). SVR is especially effective for high-dimensional data and cases where the relationship between variables is not strictly linear.

🔍 What is SVR?
Support Vector Regressor aims to find a function that deviates from the actual target values by a value no greater than a specified margin (𝜀), while also being as flat as possible. Unlike traditional regression models that try to minimize the error between predicted and actual values, SVR tries to fit the best line within a threshold margin.

<p align="center"> <img src="https://miro.medium.com/v2/resize:fit:1200/1*on-rzD9YoBlbEQ2TCuz0_w.png" alt="SVR Margin" width="500"/> </p>
⚙️ How SVR Works
Margin of Tolerance (ε): Instead of minimizing the distance from the data points, SVR tries to fit the best line within an epsilon (ε) margin.

Support Vectors: Only the data points that lie outside the ε-tube (or on its boundary) influence the position of the regression line. These points are called support vectors.

Kernel Trick: SVR can efficiently handle non-linear relationships using kernel functions like:

Linear

Polynomial

Radial Basis Function (RBF)

Sigmoid

🧠 Mathematical Objective
SVR tries to solve the following optimization problem:

Minimize:

1
2
∥
𝑤
∥
2
+
𝐶
∑
𝑖
=
1
𝑛
(
𝜉
𝑖
+
𝜉
𝑖
∗
)
2
1
​
 ∥w∥ 
2
 +C 
i=1
∑
n
​
 (ξ 
i
​
 +ξ 
i
∗
​
 )
Subject to:

𝑦
𝑖
−
(
𝑤
⋅
𝑥
𝑖
+
𝑏
)
≤
𝜖
+
𝜉
𝑖
(
𝑤
⋅
𝑥
𝑖
+
𝑏
)
−
𝑦
𝑖
≤
𝜖
+
𝜉
𝑖
∗
𝜉
𝑖
,
𝜉
𝑖
∗
≥
0
y 
i
​
 −(w⋅x 
i
​
 +b)≤ϵ+ξ 
i
​
 
(w⋅x 
i
​
 +b)−y 
i
​
 ≤ϵ+ξ 
i
∗
​
 
ξ 
i
​
 ,ξ 
i
∗
​
 ≥0
Where:

∥
𝑤
∥
∥w∥ controls the flatness of the function

𝐶
C is the penalty parameter controlling the trade-off between flatness and tolerance

𝜉
𝑖
,
𝜉
𝑖
∗
ξ 
i
​
 ,ξ 
i
∗
​
  are slack variables

✅ Key Features
Robust to Outliers: SVR uses a margin of tolerance to ignore minor errors, making it robust.

Regularization Control: The C parameter helps control overfitting.

Flexible with Kernels: Handles linear and non-linear regression equally well.

Works Well with High Dimensional Data: Especially useful when the number of features is large.
