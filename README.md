Download Link: https://assignmentchef.com/product/solved-biostat276-problemset1-bayesian-adaptive-lasso
<br>



Please describe all your work in clear terms, before implementing R code. Each question should include a description of your approach with clear indication of where I can find the associated source code. Your code should be attached to your assignment or uploaded online to a repository I can freely access.

Consider the implementation of a posterior simulation algorithm for Bayesian adaptive LASSO. More precisely consider the following model:

<em>Y </em>| <em>β,σ</em><sup>2 </sup>∼ <em>N</em>(<em>X</em><em>β,σ</em><sup>2</sup><em>I<sub>n</sub></em>) Let <em>β </em>= (<em>β</em><a href="#_ftn1" name="_ftnref1"><sup>[1]</sup></a><em>,…,β<sub>p</sub></em>)<sup>0</sup>, the model is completed with priors:

<em>β<sub>j </sub></em>| <em>τ<sub>j</sub></em><sup>2 </sup>∼ <em>N</em>(0<em>,τ<sub>j</sub></em><sup>2</sup>); <em>j </em>= 1<em>,…,p</em>

<em>h </em>= 1<em>/σ</em><sup>2 </sup>∼ <em>Gamma</em>(0<em>.</em>1<em>,rate </em>= 10)

<ol>

 <li></li>

</ol>

<table>

 <tbody>

  <tr>

   <td width="95"></td>

  </tr>

  <tr>

   <td></td>

   <td></td>

  </tr>

 </tbody>

</table>

<ul>

 <li>Consider <em>p </em>= 1. Simulate 5,000 Monte Carlo samples from the conditional prior <em>β </em>| <em>τ</em><sup>2 </sup>= 1 and obtain a plot of the density using the R function density.</li>

</ul>

<ol>

 <li>Consider <em>p </em>= 1. Simulate 5,000 Monte Carlo samples from the marginal prior <em>β</em>, considering <em>λ</em><sup>2 </sup>= 2, so that <em>E</em>(<em>τ</em><sup>2 </sup>| <em>λ</em>) = 1. Obtain a plot of the density as in</li>

 <li>Consider <em>p </em>= 1. Add a hyper prior on <em>γ </em>= 1<em>/λ </em>∼ <em>Gamma</em>(<em>a,rate </em>= <em>b</em>). Assess how the marginal prior of <em>β </em>changes for <em>a </em>= 1 and values of <em>b </em>≥ 1.</li>

 <li>Considering the hyper prior in <strong>c</strong><em>.</em>, describe a Markov Chain Monte Carlo algorithm to sample from the posterior distribution of <em>β </em>and <em>σ</em><sup>2</sup>.</li>

 <li>Implement such algorithm in R and compare your results with estimates obtained using glmnet(). In particular, you should test your results on the diabetes data available from lars, (use the matrix of predictors x).</li>

 <li>For the diabetes data, fix <em>λ </em>and produce a regularization path for adaptive Bayesian Lasso obtained on a grid of values for the tuning parameter <em>λ</em>. Describe your approach and compare your result with the path obtained using glmnet().</li>

 <li>Free <em>λ </em>and carry out a sensitivity analysis assessing the behavior of the posterior distribution of <em>β </em>and <em>σ</em><sup>2</sup>, as hyper parameters <em>a </em>and <em>b </em>are changed. Explain clearly the rationale you use to assess sensitivity and provide recommendations for the analysis of the diabetes data.</li>

 <li>[Extra credit] Using rcpp attempt and quantify acceleration of your code in (e.).</li>

</ol>