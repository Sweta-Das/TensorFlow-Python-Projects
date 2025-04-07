# Logistic Regression Model

- Logistic regression is a supervised machine learning algorithm i.e., used primarily for binary classification tasks.
- It models the probability that a given input belongs to a certain class.

# Key Concepts

### 1. Binary Classification Overview

- In binary classification, the output variable `y` takes only 2 values: 0 or 1.
- Goal: to learn a function `f(x)` that maps input features `x` to a probability $P(y = 1|x)$.
- Commonly, a threshold of 0.5 is applied to decide the class:
    - If $P(y=1|x)>0.5$: predict class-1.
    - Else: predict class-0.

### 2. Sigmoid Function and Probability Interpretation

- Sigmoid function is used to squash real-valued input into the range (0, 1), making it interpretable as a probability.

    $\sigma(z)$ = $\frac{1} {(1+e^{-z})}$

    - Here, $z$ = $w^T x + b$ (linear combination of inputs and weights)
    - Output:
        - $\equiv$ 1 → strong confidence in class-1
        - $\equiv$ 0 → strong confidence in class-0

### Difference between Linear Vs. Logistic Regression

Aspect $\space$ $\space$ $\space$ $\space$ $\space$|	Linear Regression                     |	Logistic Regression
----------------------------------------------------------------------------
Output $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$|	Continuous values (e.g., 3.5, -1.2)	  |   Probabilities (0 to 1) </br>
Use Case $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$|	Regression problems $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$|   Classification problems </br>
Activation Function|  None $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$ $\space$|   Sigmoid </br>		
Loss Function $\space$ $\space$ $\space$ $\space$ $\space$|  Mean Squared Error (MSE) $\space$ $\space$ $\space$ $\space$ $\space$ $\space$|   Binary Cross-Entropy	


### Mathematical Foundation

1. Logistic (Sigmoid) Function
    
    $\sigma(z)$ = $\frac{1} {(1+e^{-z})}$, where $z$ = $w^T$ $x$ + $b$

    - Converts raw model output `z` into a probability
    - Output lies strictly between 0 and 1.

2. Cost Function: Binary Cross-Entropy (Log Loss)

    - Used to measure how well the predicted probabilities match the actual labels.

        $Loss$ = - $[y . log(ŷ) + (1-y) . log(1-ŷ)]$

        where,</br>
            - y: true label (0 or 1) </br>
            - ŷ = $\sigma (z)$: predicted probability

3. Gradient Descent in Logistic Regression
 
    - Gradient descent is used to optimize the **weights (w)** and **bias (b)**
    - Steps:
        - Compute prediction: $ŷ = \sigma (w^T x + b)$
        - Compute loss using binary cross-entropy
        - Compute gradients of loss w.r.t weights and bias
        - Update weights:</br>
            $w := w - \alpha . \frac{\delta Loss}{\delta w}$ </br>
            $b := b - \alpha . \frac{\delta Loss}{\delta b}$ </br>
            where, $\alpha$ is the learning rate.
