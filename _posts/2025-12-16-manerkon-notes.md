---
layout: post
title: "An Inquiry into Manerkonic Statistics"
author:
- Alexander Ahmann
date: 2025-12-16

journal: "Data Blogging and Working Technical Reports"
volume: 1
number: 1

draft: true

abstract: "This is something of an \"open notebook\" for inquiries into the Manerkon and related constructs developed by the controversial Harry H. Laughlin of the Eugenics Record Office. The Manerkon is a probability or correlation surface used for modelling the probability of an event given some prediction basis. Here, I will document the development of the Manerkon, decouple it from its original eugenic intentions, and repurpose the Manerkon surface into less problematic contexts."
---

<p style="font-size:22px;">Table of Contents</p>

* contents
{:toc}

# Background

## Social and Historical Context

The publication of Charles Darwin's groundbreaking monograph, _On the Origin of Species by Means of Natural Selection, or the Preservation of Favoured Races in the Struggle for Life_, has inspired new interpretations of social science from a biological perspective. A key figure in this Victorian-era social science was Sir Francis Galton, Darwin's half-cousin, who helped to formulate systematic and quantitative studies into the nature of biological inheritance. 

From Galton's interests, he coined the term "eugenics," a term deriving from Greek that roughly translates to "good birth." Eugenics is the application of selective breeding principles to humans, and eventually turned out to be a highly unethical approach to social engineering, culminating into the Holocaust and Aktion T4 in Nazi Germany. Laughlin developed the Manerkon surface as a tool to study heredity of complicated traits and to apply selective breeding principles, starting with thoroughbred horses to those abstract traits like intelligence or "work ethic" in humans. This should be kept in mind when reading this work.

## Caveat Lector

Of course, it should be noted that this author is fallible, and will definately make mistakes when writing this draft. Readers are encouraged to scrutinize every claim made, and keep in mind that this is an incomplete writing. Take caution when citing, and specifically regarding policymakers, _please do not cite this for legal proceedings_.

# Der Korrelationsfläche

Laughlin introduces the notion that a probability \\(K\\), as a function of a prediction-basis \\(M\\) and a "thing predicted" \\(R\\), or \\(K = f(M, R)\\). The \\(f(M, R)\\) is a surface, in which each cross-section of the surface is a conditional split-normal distribution. First, one must specify an index by which to use as a basis for prediction, or an \\(M\\) value. Next, one must specify a trait that can be expressed as a ratio or an interval scale--- be it height or, in the case of Laughlin, racing capacity in the thoroughbred horse.

## Manerkonic Cross-section Function

For the Manerkon surface, Laughlin presented a "real task," which was to find a function, \\(f(M, R)\\), that will "manipulate the \\(M\\) and \\(R\\) values decided upon, so as to give the correct \\(K\\) or probability." In various literature items, Laughlin vaguely discusses techniques for working out such a formula, which involve the Manerkonic cross-section formula, and a set of continuous, smoothing functions called the _specific formulae of heredity_, which estimate the parameters of a conditional split-normal distribution. 

With the Manerkonic cross-section formula, I present a slightly modified version of what Laughlin proposed, 

$${\LARGE K = K_{fc} \cdot \epsilon^\frac{-\|FC - R\|^2}{2 \left[ \sigma_1 + 2(\sigma_s - \sigma_1) \cdot \delta(R) \right]^2}}$$

where \\(FC\\) is the maximum-ordinate of the dataset, \\(K_{fc}\\) is the relative frequency, or probability, of the maximum-ordinate of the dataset, and the \\(\sigma_1\\) is the standard deviation of values to the right of the maximum ordinate,

$$\sigma_s = \frac{1}{K_{fc} \sqrt{2\pi}}$$

and

$$\delta(R) = \begin{cases}
0 & \text{ if } FC \geq R \\
1 & \text{ if } FC < R
\end{cases}$$

\\(FC\\), \\(K_{fc}\\) and \\(\sigma_1\\) are all free variables determined by continuous smoothing functions. Laughlin provided formulae for three parameters in the form of,

$$\displaystyle \theta_{FC \text{ or } K_{fc} \text{ or } \sigma_1} = (aM + bM^2)(C_{-M}) + (cM + dM^2)(C_{+M}) + e$$

The constants are to be "fitted to empirical data," though unfortunately I was not able to identify any formal techniques prescribed by Laughlin for estimating the \\(a, b, c, d, e\\) constants through a fitting procedure. Nonetheless, I do have an incomplete and informal algorithm for finding the parameters:

> 1. Define a bivariate dataset of ratios or intervals consisting of vectors \\(M\\) and \\(R\\). The \\(M\\)-axis is the absicca which represents the prediction-basis, and the \\(R\\)-axis is the ordinate which represents the "thing predicted."
> 2. On the \\(M\\)-axis, divide it up into \\(N\\) arbitrary "bins," where \\(M_0\\) is the first bin and \\(M_N\\) is the last bin.
> 3. Declare a new tabular dataset of \\(\theta_\text{p.d.} = [M, R, FC, K_{fc}, \sigma_1]\\)
> 4. For each bin \\(M_i\\) in the \\(M\\)-axis,
>     1. Estimate the \\(FC\\), \\(K_{fc}\\), and \\(\sigma_1\\) parameters for that particular bin.
>     2. Append the estimated parameters to \\(\theta_\text{p.d.}\\)
> 5. Define a continuous function for each of the Manerkon cross-section formula's parameters: \\(\theta_{FC}\\), \\(\theta_{K.fc}\\), \\(\theta_{\sigma_1}\\). 
> 6. Use regression analysis techniques to fit each of the functions to their respective \\(\theta_\text{p.d.}\\) vector.

__NOTE: that this algorithm is (most likely) really, really flawed, and needs to be better worded out.__

## The Probability Resultant

__[TODO]__

## The Coefficient of Prediction Accuracy

__[TODO]__

## The Metroporic Formula for Thoroughbred Racing Capacity

# End Matter

_This is an incomplete piece, much more work is needed._

## Supplementary Materials

The following is a GitHub repository of materials that I have came up with: [https://github.com/nekanatech/manerkon](https://github.com/nekanatech/manerkon)

## Acknowledgement

_Truman State University_ librarians for allowing me access to items in the Harry H. Laughlin collection, and an  anonymous Greek speaking person for confirmation of the Greek terms _Metron_ meaning "measure" and "porius" meaning "pathway." Furthermore, AI/LLMs were used as an "assistant" for analysing publically avaliable literature items and other resources (which is elaborated further in the supplementary GitHub repository.

# References

1. "1928-1929 Year Book," _Carnegie Institution of Washington_, no. 28, pp. 59--60  1929, [https://archive.org/details/yearbookcarne28192829carn/page/58/mode/2up](https://archive.org/details/yearbookcarne28192829carn/page/58/mode/2up)
2. H. H. Laughlin, "The General Formula of Heredity," _Proceedings of the National Academy of Sciences_, vol. 19, no. 8, pp. 787--801, Aug. 1933, [https://doi.org/10.1073/pnas.19.8.787](https://doi.org/10.1073/pnas.19.8.787)
3. H. H. Laughlin, “Racing Capacity in the Thoroughbred Horse. Part I. The Measure of Racing Capacity.,” _The Scientific Monthly_, vol. 38, no. 3, pp. 210–222, Mar. 1934, Available: [https://www.jstor.org/stable/15639](https://www.jstor.org/stable/15639)
4. H. H. Laughlin, "The Probability-Resultant," _Proceedings of the National Academy of Sciences_, vol. 21, no. 11, pp. 601--610, Nov. 1935, doi: [https://doi.org/10.1073/pnas.21.11.601]([https://doi.org/10.1073/pnas.21.11.601)
5. "Year Book (Jul. 1, 1936--Jun. 30, 1937)," pp. 62--69, _Carnegie Institution of Washington_, no. 36, 1927, [https://archive.org/details/yearbookcarne36193637carn/mode/2up](https://archive.org/details/yearbookcarne36193637carn/mode/2up)
6. H. H. Laughlin, "The Specific Formula of Heredity," _Proceedings of the National Academy of Sciences_, vol. 19, no. 12, pp. 1020–1022, Dec. 1933, [https://doi.org/10.1073/pnas.19.12.1020](https://doi.org/10.1073/pnas.19.12.1020)
7. R. A. FISHER, "Mathematics of Inheritance," _Nature_, vol. 132, no. 3348, pp. 1012--1012, Dec. 1933, [https://doi.org/10.1038/1321012a0](https://doi.org/10.1038/1321012a0)
8. C. Genest and J. V. Zidek, "Combining Probability Distributions: A Critique and an Annotated Bibliography," _Statistical Science_, vol. 1, no. 1, Feb. 1986, [https://doi.org/10.1214/ss/1177013825](https://doi.org/10.1214/ss/1177013825)
9. T. J. Cole and P. J. Green, "Smoothing reference centile curves: The lms method and penalized likelihood," _Statistics in Medicine_, vol. 11, no. 10, pp. 1305–1319, 1992, [https://doi.org/10.1002/sim.4780111005](https://doi.org/10.1002/sim.4780111005)
10. R. T. Clemen and R. L. Winkler, "Combining probability distributions from experts in risk analysis," _Risk Analysis_, vol. 19, no. 2, pp. 187–203, 1999, [https://doi.org/10.1023/a:1006917509560](https://doi.org/10.1023/a:1006917509560)
11. T. E. Clemons and E. L. Bradley, "A nonparametric measure of the overlapping coefficient," _Computational Statistics & Data Analysis_, vol. 34, no. 1, pp. 51–61, July 2000, [https://doi.org/10.1016/s0167-9473(99)00074-2](https://doi.org/10.1016/s0167-9473(99)00074-2)
12. D. M. Stasinopoulos and R. A. Rigby, "Generalized Additive Models for Location Scale and Shape (GAMLSS) inR," _Journal of Statistical Software_, vol. 23, no. 7, 2007, [https://doi.org/10.18637/jss.v023.i07](https://doi.org/10.18637/jss.v023.i07)
13. T. R. Fenton and R. S. Sauve, "Using the LMS method to calculate z-scores for the Fenton preterm infant growth chart," _European Journal of Clinical Nutrition_, vol. 61, no. 12, pp. 1380–1385, Feb. 2007, [https://doi.org/10.1038/sj.ejcn.1602667](https://doi.org/10.1038/sj.ejcn.1602667)
14. T. J. Cole, "The development of growth references and growth charts," _Annals of Human Biology_, vol. 39, no. 5, pp. 382–394, July 2012, [https://doi.org/10.3109/03014460.2012.694475](https://doi.org/10.3109/03014460.2012.694475)
15. K. F. Wallis, "The Two-Piece Normal, Binormal, or Double Gaussian Distribution: Its Origin and Rediscoveries," vol. 29, no. 1, Feb. 2014, [https://doi.org/10.1214/13-sts417](https://doi.org/10.1214/13-sts417)
16. R. Koenker and K. F. Hallock, "Quantile Regression," _Journal of Economic Perspectives_, vol. 15, no. 4, pp. 143–156, Nov. 2001, [https://doi.org/10.1257/jep.15.4.143](https://doi.org/10.1257/jep.15.4.143)

