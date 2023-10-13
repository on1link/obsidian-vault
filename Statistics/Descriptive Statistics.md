  * # Exploring Data
    * ## Data and visualisation
      * Cases
        * Something or someone
      * Variables
        * Characteristics of something or someone
        * Meets one essential criterion and it needs to have variation
          * e.g All football teams are in the same country (no variation) 
        * Levels of measurement
          * Categorical Variables:
            * Nominal: Made up of various categories that differ from each other
              * Difference (+); Order (-); Similar intervals (-); Meaningful zero point (-)
            * Ordinal:
              * Difference (+); Order (+); Similar intervals (-); Meaningful zero point (-)
              * Position in the table of teams
            * Quantitative Variables (Discrete: set of separte numbers, Continuous: infinite region fo values)
              * Interval
                * Difference (+); Order (+); Similar intervals (+); Meaningful zero point (-)
                * Age of football player
              * Ratio
                * Difference (+); Order (+); Similar intervals (+); Meaningful zero point (+)
                * Body height
      * Constant
        * Something that have no variation on the cases
      * **Data matrix**
        * Necessary for all statistical analyses
        * Cases (row) | Variables ( colums )
        * One cell in the matrix is called **observation**
        *  In practice there are too huge, so we need summarize them
      * ## Summary of data
        * ### Categorical (nominal or ordinal) 
          * Frequency tables
            * Show how the values are distributed over the cases
            * In terms of frecuency, percentage (relative frecuencies), cumulative percentage.
            * It's does not make sense for quantitative varaibles
              * Ordinal categories (lose information, but gain better overviw)
                * Less than X
                * X-Y
                * More than Y
              * This recoded the variables and this is one way, you can't recoded to inverse
          * Pie charts
            * The categories of the variable are displayed by means of slices of a pie
            * The surface of the pie are the percertange of observation of each category
            * Immediatley see **percentage**
          * Bar graphs
            * Shows how the data are distributed over the various categories of the variable
            * Easily retrieve exact number
            * It's better when the number of categories of a variable increases
        * ### Quantitative (interval / ratio ) 
          * Dot plots
            * Draw a horizontal line and label the possible values on it in regular intervals 
            * For each observation put a dot above its value on the horizontal line
            * Useful for small sample
          * Histograms
            * Similar to bar grapsh, portray the frecuencies of the possible values of a variable
            * The diff is the bars in histograms touch it others, its represetns that the values of an interval ratio variable represent an underlying continuous scale
            * We need to constructs intervals of equal weights
          * Distributions
            * The shape of the histogram can vary and could affect your statistical method:
              * Bell shaped and symetric
              * Skewed to the right or left
              * Two peaks (The variable means its bimodal instead of unimodal)

    * ## Measures of central tendency and dispersion
      * Measures of central tendency (Center of the distribution)
        * ### For categorical variables
          * Mode
            * The value that occurs most frequently
            * The most common outcome
            * Often use on nominal or ordinal level
            * Can be more than one mode in the distribution (bi-modal distribution)
        * ### For quantitative variables
          * Median 
            * Can't do it with nominal variables
            *  The middle value of your observations when arranged from the smallest to the largest
            * The median divides the distribution into two equals parts (50%/50%)
            * Use median whe the distribution is highly skewed or outliers
          * Mean ^qSAfbOB72
            * The sum of all values divided by the number of observations
            * $$ \overline{x} = \frac{\sum{x}}{n} $$
              * The mean of variable x equals the sum of all the values of x divided of sample size
            * Is like the *balance point* of the data
            * Too sensible to outliers
          * **NOTE**: On quantitative variables, bill gates bar example, in this case take more sense to use the median instead of the mean to calculate the central tendency of the distribution
      * Measures of dispersion
        * Give information about the variability of the data
        * Range
          * Its the diference between the highest and lowest value (range = high - low)
          * Higher means more variability
          * Simple to computed, but doesn't give a good impression of the variability of the data (only extreme values takes part)
        * Interqueartile Range
          * Leaves out the extreme values
          * Dsitribution in four equal parts, the values that divides the distribution are called quartiles: Q1, Q2, Q3
          * Q1 = Middle value of the values on the left side of the median.
          * Q2 = median
          * Q3 = Middle value of the values on the rigth side of the median.
          * Interquartile range is the distance between the third and first quartiles $$ IQR = Q3 - Q1 $$
            * It's not affected by outliers
            * Outliers equals to:
              * Values lower than $$Q1 - 1.5 (IQR)$$
              * Values higher than $$Q3 + 1.5(IQR)$$
        * Box Plot
          * Graph to describe center, variabliity and outliers
          * Shows Q1, Q2 and Q3, minimum value that's not an outlier, maximun value that's not an outlier, and outliers
          * ![[Roam/Turing/Attachments/imgs/app/Turing/wO_QYA6ddN.png]]
          * The box stands for the central 50% of the distribution (From Q1 to Q3)
          * Outliers are displayed by means of dots.
        * ### Variance and Standard deviation
          * The main advantage is that they take into account **all** the values of a variable
        * Variance
          * $$ S^2 =  \frac{\sum{(x - \overline{x})^2}}{n - 1}$$
            * For every observation x you have to substract de mean value x bar
              * The positive values counter the negative values, the sum of these values equals to zero, for that reason its use the square of deviations
            * The upper part is call the **sum of squares**
            * Finally divide for the size of sample - 1
          * The larger the variance -> the large the variability -> the more the values are spread out around the [[Descriptive Statistics#^qSAfbOB72|Mean]] 
          * ** Disadvantages**
            * The metris fo the variance is the metric of the variable under analysis but SQUARED
            * The solution is apply square root and get the standard deviation
        * Standard deviation
          * $$ S =  \sqrt{\frac{\sum{(x - \overline{x})^2}}{n - 1}}$$
          * Can be seen as the average distance of an observation from the [[Descriptive Statistics#^qSAfbOB72|Mean]]
          
    * ## Z-score
      * **Z-score**: Used to know if a specific observation is common or excepcional. Give information about how extreme an observation is. Useful to compare different distributions.
      * Is a score in terms of the number of standard deviations it is removed from the mean. This number is called z-score.
      * If we recode original scores into z-scores, we say that we **standardize** a variable $$ Z = \frac{x - \overline{x}}{S}$$
        * Negative z-scores represent values below the mean
        * Positive z-scores represent values above the mean
        * The negative and positive z-scores cancel each others, their sum is equal to zero
      * How to know if a z-score is low or high 
        * Depends on the distribution and on context
        * If the distribution is bell-shaped
          * 68% of the observations fall between z-scores of -1 and 1.
          * 95% of the observations fall between z-scores of -2 and 2.
          * 99% of the observations fall between z-scores of -3 and 3.
          * More of +-3 is considered expectional
        * If the distribution is skewed to the right
          * Large positive z-scores are more common, because more extreme values on the right side of the distribution
        * If the distribution is skewed to the left
          * Large negative z-scores are more common, because more extreme values on the left side of the distribution
        * A rule that apply to any distribution regardless shape
          * 75% of the data must lie within a z-score of -2 and 2
          * 89% of the data must lie within a z-score of -3 and 3
      * ### Standardization
        * Recode original scores into z-scores. We standardize a variable
        * **Replace the original scores by standard deviations from the mean**
        * The advantage: easy to see whether a specific score is relative common or exceptional
  * # Correlation and Regression
    * ## Correlation
      * **Correlation**
        * Relationship between two variables
      * Display relationship of two variables by means of tables and graphs
      * **Contigency tables**
        * Enables to display the relationship between two **ordinal** or **nominal** variables, it's similar to a frecuency table (the difference is that frecuency table concenrs one variable)
        * Columns by numbers not indicate too much, it is better transform into column percentages in the form of proportions, called **conditional proportions**
          * Their formation is conditional on another variable
        * Using the count in the margin of the table, these are called **marginal proportions** 
      * **Scatterplot**
        * Useful for **quantative** variables 
        * We display two axes (x independent and y dependent variable; if no dependency the choose of each axis is a mather of choice)
        * Next display every observation in the figure.
        * Helps to broadly assess whether a correlation is strong or weak
        * But it doesn't tell us exactly how strong the relationship is (Pearson's r do)
      * **Pearson's r**
        * Expresses the exact direction and strength of the linear correlation between two variables with one single number.
          * A positive Pearson's indicates that a correlation is positive.
          * A negative correlation indicates that it is negative
          * Example
            * Strong, positive and linear relationship
            * Perfect, negative and linear relationship (all cases are exactly in the line)
            * Curvilinear relationship
        * The size of R expresses how tightly the observations are clustered around the imaginary best fitting straight line through the cloud of the data points
          * Between - 1 and 1
          * -1 = perfect negative correlation
          * +1 = perfect positive correlation
          * zero means no correlation at all.
        * One of the most frequently used measures of correlation
        * Appropiate if the variables under analysis are measured on **quantitative level** and if they are **linearly related** to each other
        * $$ r = \frac{\sum Z_x Z_y}{n-1}$$
        * **important note**
          * You can always compute a Pearson's r, even if the relationship is not linear
          * Check scaterplot before you calculate Pearson's r to see if the variables are linearly related. If not, do not compute a Pearson's r, because it doesn't tell much about relationship between your variables.
    * ## Regression
      * ### Regression Analysis 
      * ### Regression Line 
        * The line that best represents the linear correlation between two quantitative variables in a scatterplot
        * The best fitting line is called a regression line, and the name of the method of analysis is called **ordinary least squares regression** (which refers to the way the line is found)
        * From a given line on the scatterplot we measure the vertical distance between a observation and the line
          * Every distance is called a residual
          * Exists positive residuals (cases from above the line )and negative residuals (cases from below the line)
          * Do it for every posible line in the scatterplot. In practice is impossible, and the trick is to minimize the square of the least residuals
        * ### Sum of the squared residuals
          * Residual: Vertical distance of the cases in your scatterplot to the line
          * Used to choose a regression line where the sum of the squared residuals is the smallest (squared because positive and negative residuals cancel each other)
        * ### How to describe a regression line?
          * Important for:
            * Communication
            * Prediction
            * Indentification of unusual cases
          * $$ \hat{y} = bx + a $$
            * $$ \hat{y} $$  is the predicted value of $$ y $$
            * $$ a $$ **regression intercept** or constant
              * It is the predicted value of $$ \hat{y}$$ when the regression line crosses the $$y$$ axis and $$x$$ does equal 0
            * $$ b $$ is the **regression coefficient** or slope
              * It is the change of $$y$$ when $$x$$ increases with one unit
          * Very useful because it can help to make **predictions** about the dependent variable by means of the **regression equation** or formula with much more precission 
          * ** Note ** When you know the means and the standard deviations of the variables and also the corresponding Pearson's r, it can be use two formulas
            * $$ b = r \frac{S_y}{S_x} $$ computes the regression coefficient (unstandardized Pearson's r)  
            * $$ a = \overline{y} - b(\overline{x}) $$ computes the regression intercept
      * ### How well does the regression line fit the data?
        * The reason is to know how accuracy of predictions analysis are.
        * ### r-squared 
          * It is expressed by means of the $$r^2$$
            * Is closely related to the Pearson's r $$ r^2 = $$ pearson's  squared
            * With perfect linear fit 
              * $$ r = 1 $$ and $$ r^2 = 1 $$
              * $$ r = 0 $$ and $$ r^2 = 0 $$
          * How much better a regression line predicts your dependent variable than the mean of the dependent variable.
          * It use the residuals too
          * Example
            * $$ r^2 = 0.69 $$ The prediction error is 69% smaller than when you use the mean of the dependent variable
          * Another definition:
            * The amount of the variance in the dependent variable ($$y$$) that is explained by the independent variable ($$x$$)
            * Explained variance is the percentage of hte variance in the dependent variable that can be explained using the formula of the regression line.
            * Example
              * $$ r^2 = 0.69 $$ 69% of the variance in the grades can be predicted by the previous grades
    * ## Caveats and examples
      * ==Correlation is not Causation==
        * On a basis of a regression analysis you never prove that there are a causal relationship between two variables
        * Causality can run in both directions, or the opposite direction.
        * We can have a third variable that explains both the independent and the dependent variable. This is called a confounding variables if it is included in the study. If it is not but could have the potential for confounding, we would call it a lurking variable.
      * ### Outliers can impact on the results of a study 
        * Always check for influential outliers, especially when you are working with a small sample
        * They can have a strong efffects on the results of an analysis.
        * They can be the result of wrong measurement, and might want to delete the case.