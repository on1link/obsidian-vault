  * There are two types of statistical inference methods
    * Estimate population parameters
    * Test hypotheses about these parameters
  * This page is focused in the first type of [[Inferential statistics]]: estimation by means of a confidence interval
  * A confidence interval is a range of numbers, which, most likely, contains the actual population value. 
  * The probability that the interval actually contains the population value is what we call the **confidence level**.
  * ## How to construct confidence intervals for means and proportions
  * ## How interpret confidence intervals.
  * ## How decide how large your sample size should be.
  * # Inference and confidence interval for mean
    * We can estimate the value of a population parameter in two ways:
      * By means of a so-called **point estimate** (a single number that is our best guess for the population parameter)
      * Or by means of an **interval estimate** (a range of values within which we expect the parameter to fall)
        * The probability that the interval contains the population value is what we call the **confidence level**
    * How to compute a confidence interval if the population standard deviation is known.
      * In this case we need the **z-distribution** (unlikely scenario)
      * The standard deviation in the population is unknown. In this case we need the **t-distribution**
    * To compute a confidence interval for a population mean, two assumptions need to be satisfied
      * The data should be a **random sample**
      * The population should be **approximately normally distributed**
        * Using the t-distribution to construct a confidence interval for a mean is robust against violations of this assumption
      * * Be wary of extreme outliers when constructing a confidence interval based on the t-distribution
        * When the data have extreme outliers the method doesn't work well, always check the data before.
    * ### Confidence Interval for mean with known population standard deviation
      * Using the Sampling distribution of the mean
        * The formula is
          * $$\overline{x} \pm 1.96 \sigma_{\overline{x}}$$
          * It is the point estimate or the sample mean plus and minus the margin of error, which equals 1.96 standard deviations.
          * The standard deviation equals to $$\sigma_{\overline{x}} = \frac{\sigma}{\sqrt{n}}$$
          * With an infinite number of samples
            * Compute the confidence interval, in 95% of the samples the population value will fall within the confidence interval
    * ### Confidence Interval for mean with unknown population standard deviation
      * To compute the confidence interval, you need to known the standard deviation of the population.
        * Usually we don't know this parameter
        * We estimate the population standard deviation and therefore apply another distribution than the standard normal distribution
          * The T-distribution
        *  We can rewrite the formula for confidence interval as follows:
          * $$\overline{x} \pm Z_{95\%}\sigma_{\overline{x}}$$ 
            * Solution to the unknown standard deviation for the sample, we estimate the population standard deviation with the sample standard deviation
          * $$\overline{x} \pm Z_{95\%}(SE)$$ where
            * $$SE = \frac{s}{\sqrt{n}}$$ 
            * SE is the Standard Error, adding extra error in the computation.
              * For that reason we use another distribution than the standard normal distribution or z-distribution
              * We now use the t-distribution
          * $$\overline{x} \pm t_{95\%}(SE)$$ where
            * $$SE = \frac{s}{\sqrt{n}}$$
          * The T-distribution
            * Strongly resembles the standard normal distribution
            * Bell-shaped, symmetric, mean of zero
            * Slightly different, we're now estimating the standard deviation of the sampling distribution, we introduce extra error. That error can be substantial when we have a small sample
            * The t-distribution takes into account the extra error for small samples
            * The t-distribution therefore has slightly thicker tails than a normal distribution and have a large standard deviation.
            * The large the sample, the more the t-distribution look like the normal distribution, the shape is dependent on a single parameter, the degrees of freedom $$df$$.
              * The degrees of freedom parameter in the t-distribution equals the sample size $$n$$ minus 1
              * $$df = n - 1$$
              * This means we have many t-distributions, one separate distribution for each $$df$$, with 30 or more degrees of freedom is almost identical to the standard normal distribution
              * The standard normal distribution is the t-distribution with infinite degrees of freedom $$df = \infty$$ 

  * # Confidence interval for proportion and confidence levels
    * ## Confidence intervals for population proportions.
      * To construct the confidence interval for a proportion we use the **sampling distribution of the sample proportion**
      * The formula with which we can compute a 95% CI looks like this
        * $$p \pm 1.96 \sigma_p$$ where
        * $$\sigma_p=\sqrt{\frac{\pi (1-\pi)}{n}}$$ or
        * $$p \pm Z_{95\%} \sigma_p$$ where
        * $$\sigma_p=\sqrt{\frac{\pi (1-\pi)}{n}}$$
      * We don't known the population proportion $$\pi$$, so it is impossible to compute a standard deviation of the sampling distribution of the sample proportion. We therefore substitute the population parameter $$\pi$$ with an estimate, this estimate is the sample statistic $$p$$
      * $$p \pm Z_{95\%} (se)$$ where
      * $$se = \sqrt{\frac{p (1-p)}{n}}$$, the standard error
      * In contrast with the confidence interval for a mean for the proportion we don't use the t-distribution.
      * Assumptions for use the **standard normal distribution**
        * You should have at least 15 successes and 15 failures.
        * $$np \geq 15$$ and $$ n(1-p)\geq 15$$
    * ## Confidence levels and margin of error trade-off between confidence and precision
      * 95% confidence interval means that we can be 95% confident that our point estimate, which could be a mean or a proportion, falls within in our confidence interval
      * Tell us that if we would draw a infinite number of samples, similar to our extra sample and for every sample, we would compute a 95% confidence interval with a similar margin of error. In 95% of the cases the population value would fall within this confidence interval.
      * This also means that in 5% of the cases, this method will produce an interval that does not contains the actual population parameter.
      * ### How to change the confidence levels and the consequences
        * A higher confidence level leads to a wider confidence interval. The more confident we are that we draw a correct inference, the large of margin of error.
        * We have to compromise between confidence and precision
      * ### Constructing a confidence interval
        * 1. Which confidence level?
        * 2. Proportion or mean?
          * Proportion -> z-distribution
          * Mean -> t-distribution
            * Also compute the $$df$$
        * 3. Compute endpoints of interval
        * 4. Interpret results substantively
  * # Sample size and example
    * ## Choosing the sample size of a study
      * Because is impossible to question all the population, we draw a simple random sample to obtain a sample.
      * How large the sample should be?
        * Situations in means
          * Dependens on three main factors
            * 1. Magnitude of desired margin of error, smaller margin of error -> large sample size
            * 2. Confidence level, larger confidence level -> large sample size.
            * 3. Variability of the data, the larger the standard deviation, the larger the sample size
          * $$n = \frac{\sigma^2 z^2}{m^2}$$
            * For population mean $$\mu$$ and margin of error $$m$$
            * $$\sigma$$ is the standard deviation in the population (**not known**). You need to estimate this value by means of an educated guess.
            * $$z$$ is z-score corresponding to the chosen confidence level
            * $$m$$ is the margin of error
            * We assume that the population distribution is normally distributed 
        * Situations in proportions
          * $$99%$$ confidence level
          * $$0.10$$ of margin of error
          * $$n = \frac{p(1-p) z^2}{m^2}$$
          * We don't know the variable p:
            * You can use previous studies.
            * Estimate with educated guest.
            * Safe approach
              * The sample size depends of $$p(1-p)$$, the largest possible multiplication can take is $$0.25$$ if $$p=0.5$$ 
    * ## Example
      * ![[Roam/Turing/Attachments/imgs/app/Turing/PrhcpoVp3s.png]]