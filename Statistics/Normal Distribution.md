  * ## Functional form of the normal distribution
    * Also called Gaussian distribution
      * It is symmetric, bell-shaped and characterized by it's mean $$\mu$$ and standard deviation $$\sigma$$.
      * The highest point of the distribution is located at the mean
      * Its width is specified by the standard deviation.
      * $$\mu$$ and $$\sigma$$ are the parameters of the distribution.
        * They determine the location and shape of the normal curve.
        * The greater the $$\sigma$$ the lower the peak of the curve and wider the distribution
    * The cumulative normal [[Probability Distribution]] has a sigmoidal shape
      * $$\mu$$ is given at the probability value of 0.5
      * $$\sigma$$ determines the slope of the curve
    * The random variable $$X$$ has a normal distribution with parameters $$\mu$$ and $$\sigma$$ is:
      * $$X \sim N(\mu,\sigma^2)$$
      * [[Probability Distribution#^7H3TOM36v|For a continuous random variable it's called a **probability density function** ]]
        * $$f(x) = \frac{1}{\sigma \sqrt{2\pi}} e^{-0.5(\frac{(x-\mu)}{\sigma})^2}$$
        * f(x), probability density of a random variable X
        * It's an exponential function with a constant in front and a part in the exponent which contains small x, the value that the random variable may take.
        * The mean is subtracted from x and divided by the standard $$\sigma$$, i.e. the z-score
          * The values of the random variable are standardized before the rest of the equation
        * The exponential function without a constant has a surface under the curve that is changing with the value of sigma.
        * When multiplied with a constant it has a value of exactly one (area under the curve)
        * $$f(\mu) = \frac{1}{\sigma \sqrt{2\pi}}$$
        * The probability density approaches zero for very large positive or negative values of x, but will never actually be zero. The random variable can take from minus infinity to plus infinity.
        * The sum of all probabilities will be one
    * The Gaussian distribution is encountered frequently because it is the distribution that you get if the effects or outcomes of independent random processes are combined according to the central limit theorem
    * If you change the unit along the x-axis, the probability density values change for the same unit
    * ### Probability calculations
      * On the based of the probability density function (pdf) you can calculate the probability that the random variable falls within a given range by estimating the area under the curve for that range
      * For any normal distribution regardless the values for $$\mu$$ and $$\sigma$$ we have that:
        * $$P(\mu - \sigma < x < \mu + \sigma) = 0.68$$
        * $$P(\mu - 2\sigma < x < \mu + 2\sigma) = 0.95$$
        * $$P(\mu - 3\sigma < x < \mu + 3\sigma) = 0.997$$
        * These properties are often use in statistical calculations
  * ## The standard normal distribution
    * The probability values associated with any number of standard deviation away from the mean Z
      * z-distribution ^SNUG_pGDu
        * The probability distribution of these z values is a normal distribution with a 0 mean, and standard deviation of 1, also called the **standard normal distribution**, or z-distribution.
        * z-distribution $$ = N(0,1)$$
    * Cumulative z-distribution
      * The table gives the probability that the outcome of a normally distributed random variable will be lower than or equal to the point, $$x_i \leq \mu+z_i \sigma$$
      * Inversely, for a given probability, you can find a z value in the table an calculate a data value x that matches with that cumulative probability.
      * Z Table
        * List the cumulative probabilities with the corresponding z values.
        * This give a tabulated set distribution, the probabilities to encounter a value below, above, or between specific values of the random variable. 
    * How to get a z-value?
      * ### z-transformation
        * $$X \sim N(\mu,\sigma^2)$$
        * $$X = \mu + z\sigma$$ -> $$z = (x - \mu) / \sigma$$
        * $$ z_i = (x_i - \hat{x} / s)$$ can be applied to any numerical data, results in a data with mean 0 and standard deviation 1. Involves no assumptions about the underlying distribution of the data.
        * When the data is know to follow a normal distribution, probability statement can be made on the basis of the resulting z scores by using the table