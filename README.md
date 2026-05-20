# Direction-Oriented Smooth Sensitivity

We propose ${\it Direction}$- ${\it Oriented \ Smooth \ Sensitivity}$ (DOSS), a novel concept that takes the direction of noise into account. By varying the amount of noise with direction, we can add perturbations more in line with reality than the original ${\it smooth \ sensitivity}$ and improve the output accuracy.

This page contains the Python codes for our experiments on accuracy and run time. We also investivated key properties regarding the TDT and $\chi^2$-statistics, which are particularly important statistics in genomic statistical analysis. This makes it easier to use our theorems for efficiently computing the value of ${\it sensitivity}$.

In "beta_evaluation" folder, the evaluation for the characteristics of the two genome statistics are provided.

In "distribution_evaluation" folder, the most advisable $(\alpha, \beta)$-admissible distribution for noise generation was investigated.

"vs SS" folder provides the comparison results between our DOSS and the original ${\it smooth \ sensitivity}$ in terms of output accuracy.

The run time of our algorithm (Algorithm 1 in our paper) was measured for reference, in "RunTime" folder.

The omitted proofs in the main paper are provided in Proofs.pdf.

## Important Note
### Relation between $S^{ i \pm}(x)$ and $S^{ i \mp}(y)$
We should state that Lemma 2 is satisfied (i.e., the algorithm using the proposed DOSS is $\epsilon$-differentially private) when the following relation holds:  
$\forall x,y \in D^n, d(x,y)= 1 \ \mathrm{and} \ \forall i: \ \ S^{ i  -}(x) \leq e^{\beta} \cdot S^{ i  +}(y) \land S^{ i  +}(x) \leq e^{\beta} \cdot S^{ i  -}(y).$   
(The Proofs.pdf was revised accordingly.) Please note that the experiments in this study assumed that the above condition held for the obtained $S^{ i \pm}(x)$.

In our paper at IEEE CCWC 2026 on [Enhanced DOSS](https://github.com/ay0408/EnhancedDOSS), we addressed the above issue and proposed more reliable and useful concepts and algorithms. A more concise proof was also provided.

### General Form of Admissible Distributions
In Theorem 1, we provided "the most concise" general form of $(\alpha, \beta)$-admissible distributions. Based on this, it is possible to construct a variety of admissible distributions, e.g, those with density $h(z) \propto \frac{1}{(|z|^a + b)^c}$ (with appropriate $a$, $b$, and $c$) and Student's t-distributions. Finding "the best" distribution among them might be an important future challenge. 

If you find any other important issues or errors, please feel free to contact me!

## Future Directions

・Conducting rigorous theoretical analysis of the influence of $(k,l)$ on the noise distributions and the exploration of the "optimal" distribution with reference to it.

・Investigating $(\alpha, \beta)$-admissible distributions on $m$-dimensional space, especially when $m$ is large.

・Are there any cases where $\alpha$ and $\beta$ in the ${\it admissible}$ property should not be represented as linear functions of $\epsilon$? / Given functions $\alpha$ and $\beta$, is it possible to find an $(\alpha, \beta)$-admissible distribution?

・Developing more efficient methods for computing direction-oriented local sensitivity and smooth sensitivity.  
← It might be beneficial to considering the dependency of dimensions.

## Note

For details of our methods and discussion, please see our paper entitled "Direction-Oriented Smooth Sensitivity and Its Application to Genomic Statistical Analysis" (https://doi.org/10.1007/978-981-96-9101-2_4) presented at ACISP 2025. 

Errata:  
・The part following Definition 6, $\frac{\epsilon}{2(\gamma - 1)}$ → $\min\left( \frac{\epsilon}{2(\gamma - 1)}, \ \frac{\epsilon}{2} \right)$  
・Theorem 1, $\frac{\epsilon}{2(k - 1)}$ → $\min\left( \frac{\epsilon}{2(k - 1)}, \ \frac{\epsilon}{2} \right)$  
・Lemma 2, "is $\epsilon$-differentially private" → "can be $\epsilon$-differentially private"  
In particular, when $\forall x,y \in D^n, d(x,y)= 1 \ \mathrm{and} \ \forall i: \ \ S^{ i  -}(x) \leq e^{\beta} \cdot S^{ i  +}(y) \land S^{ i  +}(x) \leq e^{\beta} \cdot S^{ i  -}(y)$ holds, the alogorithm is $\epsilon$-differentially private. In Proofs.pdf, we provide the proof for the case. (See also Important Note above.)  
・The variables $z^+$ and $z^-$ are derived for each $i \in \[m\]$ independently. (In Proofs.pdf, this point has been clarified.)  

### Contact
Akito Yamamoto

Division of Medical Data Informatics, Human Genome Center,

the Institute of Medical Science, the University of Tokyo

a-ymmt@ims.u-tokyo.ac.jp

