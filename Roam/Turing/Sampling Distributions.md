  * Methods for summarizing sample data are called descriptive statistics. However, in most studies we're not interested in samples, but in underlying **populations**. If we employ data obtained from a sample to draw conclusions about a wider population, we are using methods of **inferential statistics**. It is therefore of essential importance that you know how you should draw samples.
    * Sampling methods
    * Poor practices
    * Sampling distribution
  * # Sample and sampling
    * We use the computed  **sample statistics** to draw **inferences** about the corresponding **population parameters**.
    * **Simple random sample**
      * **random multi-stage cluster sampling**
      * **stratified random sampling**
    * Forms of **bias**
  * # Sample and population
    * ## Sample
      * A focused subset of a population
      * You can do univariate analysis or bivariated and compute statistics 
      * All numerical summaries resulting from this computations are fully based on you sample and they're called **statistics** (by roman letters)
      * For summarizing sample data are called **descriptive statistics**
      * In practice the **goal** is to make statements about the **entire** underlying population
        * Employing the data obtained from a sample to draw inference about a population, we are using methods of **inferential statistics**.
        * We use the computed  **sample statistics** to draw **inferences** about the corresponding **population parameters** (Greek letters).
      * ### How to draw a sample
        * A bigger sample is better if the sampling is random, after certain point an increase in your sample only results in a very small increase in the precision of you estimation of the population parameter. But can **never** make up for a bad sampling procedure.
        * For methods of inferential statistics not every sample  is appropiated
        * You want a representative sample.
          * Simple random sample (almost imposible to do)
            * Each subject of population have the same chance of being selected
          * Random multi-stage cluster sample
            * Identify a large number of clusters within your population
            * Every cluster is represented by a bucket
            * Randomly pick a number of bucakets
            * Select all the samples from these buckets (sample)
            * Good choice if you don't have a good sampling frame or if drawing a SRS would be very expensive.
          * Stratified random sample
            * Divide the population in several groups (in strata). e.g every university is represented by a box
            * Select a simple random sample of each box (sample)
            * Advantage
              * You can make sure that you have enough subjets from every stratum in you sample.
            * Disadvantage
              * you need a sampling frame, and that you need to know to which stratum each respondent belongs.
        * Sampling frame
        * Different forms of bias
          * Estimation will be biased due to systematic under or over-representation of certain groups.
          * Undercoverage
            * Not everyone in the population is included in the sampling frame
          * Sampling bias
            * Not every person in the sampling frame is equally likely to be included in the sample
            * Fail to draw a random sample
            * e.g. convenience sample (randomly approach people on the street)
          * Nonresponse bias
            * Some selected subjects might refuse to participate, or they might be unreachable.
            * The problem is that the ones who don't responde may be different that the one who did.
          * Response bias
            * The actual given responses are biased. 
            * This could be due interviewer asking leading questions or because respondents think that some answers are socially unacceptable.
  * # Sampling distribution of sample mean and central limit theorem
    * ## The sampling distribution
      * The **sampling distribution of the sample mean** is the distribution that you get if you draw an infinite number of samples from your population and compute the mean of all the collected sample means.
      * Is the link that helps to draw conclusions about a population on the basis of only one sample.
    * ## The central limit theorem
      * Provided that the sample size is sufficiently large, the sampling distribution of the sample mean has an approximately normal distribution even is the variable of interest is not normally distributed in the population. The mean of the sampling distribution equals the population mean, and the standard deviation in the population divided by the square root of the sample size
      * No matter how a variable is distributed in the population, the sampling distribution of the sample mean is approximately normal as long as the sample size is at least thirty
      * In practice is impossible to draw an infinite number of samples
        * But as it's normal, you can describe its shape with just two parameters
          * Mean and Standard deviation
            * Mean of sampling distribution = population mean $$\mu_{\overline{x}} = \mu$$
            * Standard deviation of sampling distribution 
              * $$\sigma_{\overline{x}} = \frac{\sigma}{\sqrt{n}}$$
              * $$n$$ sample size
      * N of samples is approximatly over 30
      * The larger the size of your sample, the closer the sample means will lie to the population mean, and the smaller the standard deviation of your sampling distribution
    * ## Three dsitributions
      * Population distribution
        * Approximately Bell-shaped
          * Mean $$\mu$$, Standard deviation $$\sigma$$
      * Data/sample distribution
        * Approximateley Bell-shaped
          * Mean \overline{X}, standard d $$S$$
      * Sampling distribution
        * It's a theoretical distribution, we don't actually collect an infinite number of samples.
        * Normal distribution -> original scores into z-scores and calculate the probabilties through the z-table
        * Bell-shaped, normaled distritbuted
        * Mean = indefinity sample means $$\mu_{\overline{x}}$$
        * Standard deviation $$\sigma_{\overline{X}} = \sigma_{population} / \sqrt{n}$$
      * Summary
        * Selecting individual subjects -> population distribution
        * Selecting samples -> sampling distribution
  * # Sampling distribution of sample proportion and example 
    * For binary categorical variables it doesn't make sense to compute the population mean or standard deviation instead we compute proportions. And we only have the population proportion $$\pi$$
    * What the **sampling distribution of a population proportion** looks like
      * We DO have a mean and standard deviation
    * The sampling distribution of a population proportion is bell-shaped if you have at least 15 positive cases and 15 negative cases, and the mean of the distribution is equal to the population proportion.
      * if $$n \pi \geq 15$$ and $$ n(1-\pi)\geq 15$$
    * For a sample we have the sample proportion $$p$$
    * The mean of the sampling distribution of the sample proportion will be equals the population proportion $$\mu_p$$
    * Standard deviation of sampling distribution of sample proportion $$\sigma_{p}$$
      * $$\sigma_p = \sqrt{\frac{\pi(1-\pi)}{n}}$$
