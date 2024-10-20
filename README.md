# Direction-Oriented Smooth Sensitivity

We propose ${\it direction-oriented smooth sensitivity}$ (DOSS), a novel concept that takes the direction of noise into account. By varying the amount of noise with direction, we can add perturbations more in line with reality than the original ${\it smooth sensitivity}$ and improve the output accuracy.

This page contains Python codes of our experiments on accuracy and run time. We also investivated properties regarding the TDT and $\chi^2$-statistics, which are particularly important statistics in genomic statistical analysis. This makes it easier to use our theorems for efficiently computing the value of {\it sensitivity}.

In "beta_evaluation" folder, the evaluation for the characteristics of the two genome statistics are provided.

In "distribution_evaluation" folder, the most advisable $(\alpha, \beta)$-admissible distribution for noise generation was investigated.

"vs SS" folder provides the comparison results between our DOSS and the original ${\it smooth sensitivity)$ in terms of output accuracy.

The run time of our algorithm (Algorithm 1 in our paper) used for computing the ${\it direction-oriented smooth sensitivity}$ was measured for reference, in "RunTime" folder.


## Future Directions

・Investigating $(\alpha, \beta)$-admissible distributions on $m$-dimensional space, especially when $m$ is large.

・Developing more efficient methods for computing direction-oriented local sensitivity and smooth sensitivity.

## Note

For details of our methods and discussion, please see our paper entitled "Direction-Oriented Smooth Sensitivity and Its Application to Genomic Statistical Analysis".

### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp

