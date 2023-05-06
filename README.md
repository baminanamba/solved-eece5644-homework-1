Download Link: https://assignmentchef.com/product/solved-eece5644-homework-1
<br>
<span style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Make sure you read the problem statements and answer the questions. Submit the code online. This homework could be a bit challenging, so I suggest you start early.</span>

<strong>1.1 </strong>(14 pts) Suppose two equally probable one-dimensional densities are of the form <em>p</em>(<em>x</em>|<em>ω<sub>i</sub></em>) ∝ <em>e</em>−|<em>x</em>−<em>a</em><em>i</em>|<em>/b</em><em>i </em>for <em>i </em>= 1<em>,</em>2 and <em>b </em>≥ 0.

<ul>

 <li>Write an analytic expression for each density, that is, normalize each function for arbitrary <em>a<sub>i</sub></em>, and positive <em>b<sub>i</sub></em>.</li>

 <li>Calculate the likelihood ratio <em>p</em>(<em>x</em>|<em>ω</em><sub>1</sub>)<em>/p</em>(<em>x</em>|<em>ω</em><sub>2</sub>) as a function of your four variables.</li>

 <li>Plot a graph (using MATLAB or Python) of the likelihood ratio for the case <em>a</em><sub>1 </sub>= 1, <em>b</em><sub>1 </sub>= 1, <em>a</em><sub>2 </sub>= 2 and <em>b</em><sub>2 </sub>= 2. Make sure the plots are correctly labeled (axis, titles, legend, etc.) and that the fonts are legible when printed.</li>

</ul>

<strong>1.2 </strong>(18 pts) Consider a two-class, one-dimensional problem where <em>P</em>(<em>ω</em><sub>1</sub>) = <em>P</em>(<em>ω</em><sub>2</sub>) and <em>p</em>(<em>x</em>|<em>ω<sub>i</sub></em>) ∼

<em>N</em>(<em>µ<sub>i</sub>,σ<sub>i</sub></em><sup>2</sup>). Let .

<ul>

 <li>Derive a general expression for the location of the Bayes optimal decision boundary as a function of <em>µ </em>and <em>σ</em>.</li>

 <li>With <em>µ </em>= 2 and <em>σ</em><sup>2 </sup>= 2, make two plots using MATLAB: one for the class conditional pdfs <em>p</em>(<em>x</em>|<em>ω<sub>i</sub></em>) and one for the posterior probabilities <em>p</em>(<em>ω<sub>i</sub></em>|<em>x</em>) with the location of the optimal decision regions. Make sure the plots are correctly labeled (axis, titles, legend, etc.) and that the fonts are legible when printed.</li>

 <li>Estimate the Bayes error rate <em>p<sub>e</sub></em>.</li>

 <li>Comment on the case where <em>µ </em>= 0 and <em>σ</em><sup>2 </sup>is much greater than 1. Describe a practical example of a pattern classification problem where such a situation might arise.</li>

</ul>

<strong>1.3 </strong>(34 pts) Write a function that generates independent and identically distributed samples given class-specific parameters. The class conditional densities are normal distributions accepting class dependent means <em>µ</em><strong><sub>i </sub></strong>and covariances Σ<em><sub>i</sub></em>. The function should also accept arbitrary class priors <em>P</em>(<em>ω<sub>i</sub></em>). Be sure to test your function with some simple cases to validate that it is working correctly. Here are the specifications for the function:

One way to write this function would be to first sample the class and then sample the data point from the respective class conditional density. Generate samples according to the parameters given below and produce two-dimensional scatter plots with the simulated datasets (six plots in total):

<ul>

 <li>nSamples = 400, ,mu1 = [0,0], sigma1 = I, (with I being the identity matrix), and mu2 = [-3,-3], sigma2 = I. Use equal priors.</li>

 <li>Same as (a), but now sigma1 = sigma2 = [3, 1; 1, 0.8]. Use equal priors.</li>

 <li>nSamples = 400, mu1 = [0,0], sigma1 = [2 0.5; 0.5 1], mu2 = [2,2], sigma2 = [2 -1.9; -1.9 5]. Use equal priors.</li>

 <li>Same as (a), but make the <em>P</em>(<em>ω</em><sub>1</sub>) = 0<em>.</em>05</li>

 <li>Same as (b), but make the <em>P</em>(<em>ω</em><sub>1</sub>) = 0<em>.</em>05</li>

 <li>Same as (c), but make the <em>P</em>(<em>ω</em><sub>1</sub>) = 0<em>.</em>05</li>

</ul>

The plots must have a legend to indicate what class the samples belong to. Make sure the plots are correctly labeled (axis, titles, legend, etc.) and that the fonts are legible when printed.

<strong>1.4 </strong>(34 pts) Write a function for each of the three normal distribution discriminant functions discussed in class ([case I] class dependent mean with identity covariance, [case II] class dependent mean with shared covariance, and [case III] class dependent mean and covariances). The inputs to the functions should be similar to those of problem 3. The output of the discriminant functions should be a numberOfSamples-by-k array with the score for each class along the columns and the scores for each data point along the rows. Classify the simulated samples from question 1.3 (the 6 cases (a)-(f)) using the discriminant functions you coded. Make a scatter plot with the classification results. Compute the accuracy (number of correctly classified points divided by the total number of points) and display it on the title of the plot. Make sure the plot has a legend to indicate the classification results. In the same plot, show the decision boundary. Use the following instructions for each of the respective simulated datasets:

<ul>

 <li>For data from 1.3(a): Since only the means change, use only the class dependent mean discriminant (case I). You should have 1 plot.</li>

 <li>For data from 1.3(b): Since the covariances are the same, use the class dependent mean discriminant (case I) and the shared covariance discriminant (case II). You should have 2 plots. Do you see a difference in performance between the two classifiers? Why?</li>

 <li>For data from 1.3(c): For this dataset, use the three discriminant functions (case I, II, and III). Notice that each discriminant function will make some assumptions about the data. For the shared covariance case (case II), just average the individual class covariances (can you explain if this is a reasonable thing to do?). You should have 3 plots. Do you see a difference in performance between the three classifiers? Which one works best? Why?</li>

 <li>For data from 1.3(d): Repeat the same analysis as for the dataset used in (a). Additionally, compute the accuracy of classifying all data points as the class with the highest prior. How does it perform? Is this a good classifier? Why or why not? What can you say about accuracy as classification metric?</li>

 <li>For data from 1.3(e): Repeat the same analysis as for the dataset used in (b). Additionally, compute the accuracy of classifying all data points as the class with the highest prior. How does it perform? Is this a good classifier? Why or why not? What can you say about accuracy as classification metric?</li>

 <li>For data from 1.3(f): Repeat the same analysis as for the dataset used in (c). Additionally, compute the accuracy of classifying all data points as the class with the highest prior. How does it perform? Is this a good classifier? Why or why not? What can you say about accuracy as classification metric?</li>

</ul>

In total, you should have 12 plots.35