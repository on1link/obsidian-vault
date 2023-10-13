  * # Hypotheses and significance tests
  * ## Hypotheses
    * Statistical hypotheses, is an expectation about a population. Usually it is formulated as a claim **that a population parameter takes a particular value or falls within a specific range of values.**
      * Such a claim is based on previous studies and theory
    * There are the main ingredients of the method of [[Roam/Turing/Significance Tests#^PbdcKVIio|Significance tests]]
      * On basis of information from a sample, we asses if an hypothesis makes sense or not. This is what we call a significance test
      * Is a method using sample data to test hypotheses that area formulated in advance
    * ### Types of Hypotheses
      * Alternative Hypotheses
      * Nested Hypotheses
      * Secuential Hypotheses
      * Simple Hypotheses about $$\theta$$
      * Compound Hypotheses 
  * ## Significance tests
    * Like the [[Confidence Intervals]] is a method of [[Inferential statistics]], we **use sample data to draw inferences about population parameters**
    * ## Null-hypothesis testing
    * Each significance test is based on two hypotheses: [[Roam/Turing/Teoría de Hipótesis#^WLB7FCy9Y|1. Hipótesis Nula $(H_0)$]] y la [[Roam/Turing/Teoría de Hipótesis#^lbrWeg-GG|Hipótesis Alternativa $(H_1)$]] or $H_a$. 
    * Null-hypothesis ($$H_0$$)
      * Claims that the parameter you're interested in takes a **specific value**
      * It usually represent the situation where there is no relation between variables,  or differences between groups
      * Will be rejected if the data in your sample suggest that it is a highly unlikely expectation.
      * This hypothesis never will be considered probed
    * Alternative-hypothesis ($$H_a$$)
      * Claims that the parameter you're interested in falls within an alternative range of values.
    * The null hypothesis and the alternative hypothesis **are always mutually exclusive** (They can't be true simultaneously)
    * If you do a significance test, you assume that the null hypothesis is true unless your data provide strong evidence against it.
    * You always **assume** that the null hypothesis is true. Failing to reject the null hypothesis **doesn't** mean that the null hypothesis is true.
    * Example
      * Less than 3% of all Americans have scubadiving experience
        * $$H_a: \pi < 0.03 $$ alternative hypothesis, my expectation.
        * $$H_0: \pi = 0.03$$ null hypothesis, as to be expressed as a single value.
      * The mean maximum depth american divers have ever reached is not 25 meters
        * $$H_a: \mu \neq 25 $$ alternative hypothesis, my expectation.
        * $$H_0: \mu = 25$$ null hypothesis, as to be expressed as a single value.

  * ### Test about proportion
  * How should you conduct a significance test for proportion.
  * Conduct a significance test
    * We assume that the **population** value has a certain value, and asses if it's likely that the sample we have collected actually comes from a population with this assumed parameter value.
    * Because we look at a sample, we focus on the sampling distribution. The **sample** we collected comes from this population
    * **sampling distribution**
      * We can determine what the sampling distribution of the sample proportion looks like, e.g. given the assumed population parameter value of 0.03.
  * To condunct the test
    * We asses how many standard deviations (or standard errors for sampling distributions), the observed sample proportion is removed from the population proportion according to the null hypothesis.
    * This number of standard errors is what we refer to as the **test statistic**.
    * Example (H_0: pi = 0.03 - H_a: pi < 0.03)
      * n = 1000
      * p = 0.02
      * How likely is a sample proportion of 0.02 if the population proportion is indeed 0.03? (Assuming Null hypothesis true p = 0.03)
      * Test statistic
        * The number of standard errors from the mean is represented by a z-score.
        * $$ z = \frac{p - p_0}{\sqrt{\frac{p_0 (1 - p_0)}{n}}}$$
  * [[Roam/Turing/Research Methodology#^bIUTpgf_N|Tipos de errores; regiones criticas y valor p (__p-value__)]] test statistic, P-value, significance level and rejection region.
  * one-tailed test
  * two-tailed test.

  * ### Test about mean
    * Tests statistic = number of standard errors sample mean is removed from $$H_0$$ value.
      * To compute $$se$$ we need to know $$\sigma$$
      * We don't know $$\sigma$$
      * We estimate it using the sample standard deviation $$s$$
        * This implies that we introduce extra error
      * We use t-distribution instead of the [[Normal Distribution#^SNUG_pGDu|z-distribution]]
    * $$t =  \frac{x-\mu_0}{se}$$ where $$se= \frac{s}{\sqrt{n}}$$
    * In example we use significance level of $$\alpha = 0.05$$
  * # Step-by-step plan and [[Confidence Intervals]]
  * ## Step-by-step plan
    * ### Expectations
      * 1. More than half of all certified divers in America have more than 35 hours of diving experience.
      * 2. The mean number of hours of diving experience of all certified divers in American is more than 35 hours
    * The decision not to reject the null hypothesis is not equal to **accept** the null hypothesis
  * ## Confidence Interval
    * Significance test are closely related to confidence intervals
    * In general, the results of a two-tail significance test are in line with conclusions coming from a confidence interval
    * Based on the sample information, you want to draw inferences about population parameter $$\mu$$.
      * This is what we call [[Inferential statistics]]
    * There are two types of inferential statistics:
      * Inference about interval estimation by means of [[Confidence Intervals]]
      * Inference about point estimation using [[Significance Tests]]
    * Example
      * Sample $$n=500$$, $$\overline{X} = 36$$, $$S=9$$
      * $$H_0: \mu = 35$$, $$H_a: \mu \neq 35$$
      * Test statistic
        * $$t = \frac{\overline{x} - \mu_0}{se}$$ where $$se = \frac{S}{\sqrt{n}}$$
        * Falls in the rejection zone
      * Confidence Interval
        * 95% CI
          * $$\overline{X} \plusminus 
 t_{95\%}(se)$$ where $$se = \frac{S}{\sqrt{n}}$$
        *  Just like the significance test, this confidence interval suggest that the population mean differs from 35. In general, the results of a two-tail significance test are in line with conclusions coming from a confidence interval.
          * If the p-value in a two-tailed significance test p-value $$\leq 0.05$$, a 95% confidence interval does not contain the null hypothesis value.
          * Similarly if the p-value in a two-tailed test is p-value $$\geq 0.05 $$, then the 95% confidence interval will contain the null hypothesis value.
          * This makes sense, right? The null hypothesis value is a plausible value, so we shouldn't reject the null hypothesis.
  * # Errors
    * ## Type I Error
      * If the null hypothesis is **true** and you decide to **reject it**.

    * ## Type II Error
      * If the null hypothesis is **false** and you decide to **not reject it**
    * If you decrease the probability of making a Type I error, you increase the probability of making a Type II error and vice versa.
    * ## Power
      * The power of a test is the probability of rejecting the null hypothesis given that it is false.
  * ## Examples