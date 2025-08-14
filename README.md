# Direction-Oriented Smooth Sensitivity

We propose ${\it Direction}$- ${\it Oriented \ Smooth \ Sensitivity}$ (DOSS), a novel concept that takes the direction of noise into account. By varying the amount of noise with direction, we can add perturbations more in line with reality than the original ${\it smooth \ sensitivity}$ and improve the output accuracy.

This page contains the Python codes for our experiments on accuracy and run time. We also investivated key properties regarding the TDT and $\chi^2$-statistics, which are particularly important statistics in genomic statistical analysis. This makes it easier to use our theorems for efficiently computing the value of ${\it sensitivity}$.

In "beta_evaluation" folder, the evaluation for the characteristics of the two genome statistics are provided.

In "distribution_evaluation" folder, the most advisable $(\alpha, \beta)$-admissible distribution for noise generation was investigated.

"vs SS" folder provides the comparison results between our DOSS and the original ${\it smooth \ sensitivity}$ in terms of output accuracy.

The run time of our algorithm (Algorithm 1 in our paper) was measured for reference, in "RunTime" folder.

The omitted proofs in the main paper are provided in Proofs.pdf.

## Important Note
We should state that Lemma 2 is satisfied (i.e., $\epsilon$-differential privacy is satisfied using the proposed DOSS) when the following relation holds:  
$\forall x,y \in D^n, d(x,y)= 1 \ \mathrm{and} \ \forall i: \ \ S^{ i  -}(x) \leq e^{\beta} \cdot S^{ i  +}(y) \land S^{ i  +}(x) \leq e^{\beta} \cdot S^{ i  -}(y).$   
(The Proofs.pdf was revised accordingly.) Please note that the experiments in this study were under the assumption that the above condition holds.

In our next paper (regarding this topic), we will modify and improve the current DOSS including the above point and propose more reliable and useful concepts and algorithms.

If you find any other important issues or errors, please feel free to contact me!

## Future Directions

・Conducting rigorous theoretical analysis of the influence of $(k,l)$ on the noise distributions and the exploration of the "optimal" distribution with reference to it.

・Investigating $(\alpha, \beta)$-admissible distributions on $m$-dimensional space, especially when $m$ is large.

・Are there any cases where $\alpha$ and $\beta$ in the ${\it admissible}$ property should not be represented as linear functions of $\epsilon$? / Given functions $\alpha$ and $\beta$, is it possible to find an $(\alpha, \beta)$- ${\it admissible}$ distribution?

・Developing more efficient methods for computing direction-oriented local sensitivity and smooth sensitivity.  
← It might be beneficial to considering the dependency of dimensions.

## Note

For details of our methods and discussion, please see our paper entitled "Direction-Oriented Smooth Sensitivity and Its Application to Genomic Statistical Analysis" (https://doi.org/10.1007/978-981-96-9101-2_4) presented at ACISP 2025. 

### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp

