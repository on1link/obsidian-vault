  * # Probability distribution
    * Specifies the probabilities for each of the values that a random variable may take, i.e. describes the possible outcomes of a random variable with their probabilities. "A list of probabilities associated with each of the values".
    * If randomness due to chance is relevant in a variable, this variable is called **random variable**. ^ZFiFjmOYf
      * Variables whose possible values are numerical outcomes of a random phenomenon.
      * Can take on a set of possible values, each with an associated probability $X$, (italic capital letter) is used to denote a random variable $x_1, x_2$ represent the value that it takes.
      * There are two types: **discrete** and **continuous**
	      * Discrete take countable number of distinct values.
	      * Continuous take infinite number of possible values.
	      * Usually for measurements e.g. height, age, temp, time
      * Every random variable has by definition a probability distribution
    * Can be take the form of a table, graph or equation.
    * For a discrete random variable values it's called a **probability mass function**
      * Gives probabilities on the y-axis.
      * The distribution can be described by a probability histogram, exactly the same as with the frequency table and a frequency histogram
    * For a continuous random variable it's called a **probability density function**  ^7H3TOM36v
      *  This does not give probability on the y-axis, but rather a unit called probability density, the probability per unit value of the x value.
        * The consequence is that when units of the random variable change, e.g m to cm, the values along y-axis change accordingly. The surface area for the same interval should not change
      * To get a probability you need to consider a certain interval under the curve rather than the height of the curve at a certain location, so is given by the surface area
  * # Cumulative probability distribution
    * A cumulative probability of a random variable is the probability of obtaining a value lower than or equal to a threshold value.
    * In the other direction, a cumulative probability specifies a quantile of a random variable
      * At the cumulative probability of 0.5 the median of the random variable is found.
    * Can exist in the form of table, graph or equation
    * Can be obtained from a probability distribution by summing the probabilities in the latter from the smallest up to the largest value of the random variable. And it is continuously increasing with increasing values of the random value, from zero to one.
    * There is not difference between discrete and continuous variables for cumulative probability distribution
  * # Mean and variance of a random variable
    * With a probability distribution is defined it is possible to calculate summary statistics, even without actual observations for that variable.
    * ### Mean of a random variable
      * $$\mu_x$$ provides the expected average outcome of many observations or the expected value of $$x$$, $$E(x) = \mu_x $$
      * The mean of a discrete random variable
        * Probability-weighted average of all possible values that the random variable can take
          * $$mu_x = E(x) = x_1 P(x_1) + x_2 P(x_2)+...+x_kP(x_k) = \sum [x_i P(x_i)]$$
      * The mean of a continuous random variable
        * Average of all possible values that the random variable can take
        * $$\mu_x = E(x) = \int_{-\infty}^{\infty} x f(x) dx$$
      * Properties of the mean of a random variable $$\mu_x$$
        * ### Adding or multiplying a constant to a random variable.
          * If we add and multiply the random variable x with a and b the mean is affected as follows:
            * $$a + bx $$ -> $$\mu_{a+bx}$$
        * ### Addition or subtraction of two random variables
          * $$\mu_{x+y} = \mu_x + \mu_y$$
          * $$\mu_{x-y} = \mu_x - \mu_y$$
    * ### Variance of a random variable
      * Is define as the expected value of the squared deviation of $$X$$ from its mean mu
        * $$E[(X - \mu)^2]$$
        * For discrete random variable X:
          * $$\sum (x_i - \mu)^2 P_i (x_i)$$
        * For continious random variable X
          * $$\int (x - \mu)^2 f(x) dx$$
      * Properties of the variance of the random variable
        * ### Adding or multiplying a constant to a random variable
          * Adding a constant to a random variable doesn't change its variance
          * $$var(a+X)$$ or $$var(a-X)$$
            * $E[a+bX)- (a+b\mu^2] = E[(bX - b\mu)^2]$
            * $$E[b^2(X-\mu)^2] = b^2 E[(X - \mu)^2]$$
          * Multiplication with a constant leads to multiplication of its variance with the squared constant.
          * $$var(bX)$$
            * $$b^2 var(X)$$
            * And the Standard deviation
              * $$\sigma(bX) = \sqrt{b^2 var(X)} = \sqrt{b(var(X))} = b\sigma(X)$$
        * ### Addition or subtraction of two random variables
          * $$var(X + Y)  = var(X) + var(Y) + 2cov(X,Y)$$
          * $$var(X-Y) = var(X) + var(Y) - 2cov(X,Y)$$
          * Equation for any two random variables: $$var(aX + bY)  = a^2 var(X) + b^2var(Y) + 2abcov(X,Y)$$$$var(aX-bY) = a^2var(X) + b^2var(Y) - 2abcov(X,Y)$$
            * Covariance information is often not available, in some case are the restricted case, where the variables are not correlated, i.e $$cov(X,Y) = 0$$
              * $$var(aX+bY) = a^2var(X) + b^2var(Y) = var(aX-bY)$$
              * Generalize equation to any sum of random variables
                * $$var (X+Y+Z+...)  = var(X)+var(Y)+var(Z)+...$$ <-> $$var(\sum_{i=1}^n X_i) = \sum_{i=1}^n var(X_i)$$
          * The standard deviation of the resulting sum of random variables is always smaller tha the sum of the standard deviations for the separate random variables.
            * Some variability will cancel out when random variables are combined.
            * $$\sigma(X+Y) = \sqrt{var(X+Y)} = \sqrt{(var(X) + var(Y))}$$ -> $$\sigma(X+Y) < \sigma(X) + \sigma(Y) $$