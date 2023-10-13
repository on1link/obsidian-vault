  * The most important [[Probability Distribution]] for discrete random variables.
  * It gives probabilities for accounts with binary data, and gives the probability of $$x$$ successes in $$n$$ outcomes of the random variable, with probability of success on a single trial denoted by $$p$$
    * Assumption: $$p$$ is fixed for all trials.
  * Elementary [[Probability Distribution#^ZFiFjmOYf|If randomness due to chance is relevant in a variable, this variable is called **random variable**.]]: A variable with only **two mutually exclusive outcomes** and a **fixed probability p** to obtain one of the two outcomes 
  * Conditions to met to be certain that a random variable follows binomial distribution.
    * The probability of success in each separate trial is the same throughout the experiment, i.e. probability of success does not change
    * Trials are statistically independent. This means that the result of one trial does not depends on the results of others.
  * Ingredients of Binomial Distribution
    * ### 1)Bernoulli trial
      * Trial with 2 possible outcomes & constant probability $$p$$
    * 2) Observe $$n$$ trials
    * 3) Count number of success $$x$$
    * $$P(x) = \frac{n!}{x!(n-x)!} p^x(1-p)^{n-x}$$ where $$x = 0,1,2,...,n$$
      * The first part is the binomial coefficient. gives the number of ways you can select x elements, disregarding their order, from a set of n elements.
        * $$(x n)$$
      * $$X \sim  B(N, P)$$
        * x is a binomial random variable with n trials and success probability p.
    * ### Cumulative probability distribution
      * $$F(x) = P(X \leq x) = \sum_{k=0}^x \frac{n!}{k!(n - k)!}p^k (1-p)^{n-k}$$
    * Its mean and standard deviation depends of the probability of success $$p$$
      * $$\mu = g(p,n) = n p$$
      * $$\sigma = f(p, n) =\sqrt{(np(1-p))}$$
    * The shape of the binomial distribution varies from right-skewed when the 
value of  p is close to zero to symmetric when p is around 0.5 and  
left-skewed when p is close to one