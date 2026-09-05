---
layout: post
title: "Inquiries into the Manerkon (and related notions)"
author:
- Alexander Ahmann
date: 2025-12-16

journal: "Data Blogging and Working Technical Reports"
volume: 1
number: 1

draft: true

abstract: "This is something of an \"open notebook\" for inquiries into the Manerkon and related constructs developed by the controversial Harry H. Laughlin of the Eugenics Record Office. The Manerkon is a probability or correlation surface used for modelling the probability of an event given some prediction basis. Here, I will further research and develop the Manerkon and related ideas by Laughlin."
---

<p style="font-size:22px;">Table of Contents</p>

* contents
{:toc}

# Background

## Social and Historical Context

The publication of Charles Darwin's groundbreaking monograph, _On the Origin of Species by Means of Natural Selection, or the Preservation of Favoured Races in the Struggle for Life_, has inspired new interpretations of social science from a biological perspective. A key figure in this Victorian-era social science was Sir Francis Galton, Darwin's half-cousin, who helped to formulate systematic and quantitative studies into the nature of biological inheritance. 

From Galton's interests, he coined the term "eugenics," a term deriving from Greek that roughly translates to "good birth." Eugenics is the application of selective breeding principles to humans, and eventually turned out to be a highly unethical approach to social engineering, culminating into the Holocaust and Ackton T4 in Nazi Germany. Laughlin developed the Manerkon surface as a tool to study heredity of complicated traits and to apply selective breeding principles, starting with thoroughbred horses to those abstract traits like intelligence or "work ethic" in humans. This should be kept in mind when reading this work.

## Caveat Lector

Of course, it should be noted that this author is fallible, and will definately make mistakes when writing this draft. Readers are encouraged to scrutinize every claim made, and keep in mind that this is an incomplete writing. Take caution when citing, and specifically regarding policymakers, _please do not cite this for legal proceedings_.

# The Manerkon Surface

__Key Formulae__

_The Manerkonic Cross-section formula:_ \\[ K = K_{fc} \cdot \LARGE{ \epsilon^{ \frac{-(FC \sim R)^2}{2 \left[ \sigma_1 + 2(\sigma_s - \sigma_1) \cdot \delta \right]^2} } } \\]

where \\( \displaystyle \sigma_s = \frac{1}{K_{fc}\sqrt{2\pi}} \\),

and $$ \delta = \begin{cases}
    0 & \text{ if } R \geq FC \\
    1 & \text{ if } R < FC \\
\end{cases} $$

__The Specific Formulae of Heredity:__ each follows the basic form of: \\( f(M) = (aM + bM^2)(C_{-M}) + (cM + dM^2)(C_{+M}) + e \\)

* \\( FC = f_1(M) = (fM + gM^2)(C_{-M}) + (hM + iM^2)(C_{+M}) + j \\)
* \\( K_{fc} = f_2(M) = (kM + lM^2)(C_{-M}) + (mM + nM^2)(C_{+M}) + o \\)
* \\( \sigma_1 = f_3(M) = (pM + qM^2)(C_{-M}) + (rM + sM^2)(C_{+M}) + t \\)

__(obviously, still more work to do)__

# The Metroporic Formula for Racing Capacity

## Theoretical Measure: The Principle Added Functions

Laughlin devised what he called the _Principle of Added Functions_ for inventing "mathematical yardsticks," or a theoretical measure for complex phenomena that are composed of, or derived from, more fundamental measurements. The idea of these kinds of measuring tools can, to my knowledge, be traced back to physics. Rather than trying to directly observe a natural phenomena, scientists try to "infer" what a phenomena might look like with theoretical frameworks. 

For example, mechanical force, which is measured in netwons, is the product of a physical body's mass (typically measured in kilograms) and its acceleration (typically measured in metres per squared seconds). External mechanical forces acting on a body would then be "added up," and then divided by said body's mass to produce what Laughlin may have called a "mathematical yardstick" for acceleration, as measured by \\( \displaystyle \frac{[\text{metres}]}{[\text{second}]^2} \\), which is then used to derive more fundamental measures of velocity and displacement, measured in \\( \displaystyle \frac{[\text{metres}]}{[\text{second}]}\\) and \\( \displaystyle [\text{metres}] \\) respectively. 

To test the physics theory in question, the demonstrator would take one of the derived functions, like displacement, and compare its predictions to experimental results. If the displacement function can make testable and falsifiable predictions, and if they have yet to be disproven, then the demonstrator is justified in their belief that the theoretical framework is sound and a proper description of reality. I think that Laughlin applied reasoning to measuring quality of performance, and later racing capacity, in the thoroughbred horse.

Laughlin put his Principle of Added Functions to work by inventing a set of "mathematical yardsticks" that attempts to measure standard mean seconds per furlong. He went about constructing this measure by identifying what he thought were relevant features, writing down formulæ that described how these features affected the horse's racing capacity, and fitting the parameters of his formulæ to tabulated results from previous horse races. The _standard mean seconds per furlong_ \[[1, pp 59--60](https://archive.org/details/yearbookcarne28192829carn/page/60/mode/2up)\], or ``St. M.S.F.``, measures takes the basic form of:

\begin{equation} 
St. M.S.F._\text{s.x.} = \text{antilog} \big( [f_1(a) + c_3 ] \cdot \log d + [f_2(w) + f_3(a) + c_8] \big)
\end{equation}

where \\( \displaystyle f_1(a) = \frac{(a - c_1)^2}{c_2} \\), \\( \displaystyle f_2(w) = \frac{(w - c_4)^2}{c_5} \\), \\( \displaystyle f_3(a) = \frac{(a - c_6)^2}{c_7} \\), \\(a = \\) age in years, \\(w = \\) weight carried on the horse's back (in pounds), \\(d = \\) distance traveled in furlongs, and \\( c_1, c_2, c_3, c_4, c_5, c_6, c_7, \\) and \\(c_8\\) are constants fitting the model into empirical data. The _antilog_ is a function defined as \\( f(x) = 10^{x} \\)

An interesting bit of fact is that Laughlin could not express sex in terms of a ratio or interval measure, so he created three seperate St. M.S.F. formulæ to account for how sex affects racing capacity. The subscript \\(s.x.\\) denotes the biological sex of the thoroughbred horse--- with them being classified as "colts," "fillies," and "geldings."

Laughlin presented the following formulæ for working out the St. M.S.F. in thoroughbred racehorses, by biological sex:

<p style="font-size:22px;">1. For Colts:</p>

\\( \displaystyle \quad \quad St. M.S.F._\text{colts} = \text{antilog} \Bigg[ \Bigg(\frac{(a - 4.25)^2}{200.2821} + 0.070331 \Bigg) \log d \\)

\\( \displaystyle \qquad \qquad + \Bigg( \frac{(w - 113)^2}{77107.0687} + \frac{(a - 4.25)^2}{-315.6272} + 1.01799 \Bigg) \Bigg] \\)

<p style="font-size:22px;">2. For Fillies:</p>

\\( \displaystyle \quad \quad St. M.S.F._\text{fillies} = \text{antilog} \Bigg[ \Bigg( \frac{(a - 4.00)^2}{7641.7546} + 0.92667 \Bigg) \log d\\) 

\\( \displaystyle \qquad \qquad + \Bigg(\frac{(w - 108)^2}{77107.0687} + \frac{(a - 4.00)^2}{1586.0428} + 1.000943 \Bigg) \Bigg] \\)

<p style="font-size:22px;">3. For Geldings:</p>

\\( \displaystyle \quad \quad St. M.S.F._\text{geldings} = \text{antilog} \Bigg[ \Bigg( \frac{(a - 4.50)^2}{744.5678} + 0.082613 \Bigg) \log d\\)

\\( \displaystyle \qquad \qquad + \Bigg(\frac{(w - 112)^2}{77107.0687} + \frac{(a - 4.50)^2}{-1759.6185} + 1.008309 \Bigg) \Bigg] \\)

## The Quality of Performance



\begin{equation}
  Q. P. = \frac{\text{Standard Mean Seconds per Furlong.}}{\text{Actual Mean Seconds per Furlong.}}
\end{equation}

### Mud Running Ability (M. R. A.)



## Proposed Experiments

### Q.P. and Kinematic Features

Quality of performance ultimately measures a specific instance of an individual thoroughbred horse's performance to run a certain number of  furlongs in a certain amount of time. Horses that run the most furlongs in the least amount of time are expected to have a high Q.P. outcome. Likewise, horses that run the least furlongs in the most amount of time are expected to have a low Q.P. outcome. A test that I can perform is to analyse the correlation between quality of performance, and the number of furlongs ran divided by the number of seconds passed, or, the horse's _speed_. I will assume a Pearson product-moment correlation coefficient for linear, which is defined as:

$$\begin{equation}
\large{ r_{x \text{ vs. } y} = \frac{\sum_{(x, y) \in \omega}^{n} (x - \bar{x}) (y - \bar{y})}{ n \cdot \sqrt{\frac{\sum_{x} (x - \bar{x})^2}{n}} \sqrt{\frac{\sum_{y} (y - \bar{y})^2}{n}} } \Large}
\end{equation}$$

Specifically, I want to measure the strength of the correlation \\(r\\) of quality of performance versus racehorse speed, which I will formalise by making formula 2 into several hypothesis tests with features as shown in the following table:

| __Feature 1__ | __vs. Feature 2__ | __Null Hypothesis__ | __vs. Alt. Hypothesis__ |
|---------------|-------------------|---------------------|-------------------------|
| Q.P. | Time (sec.) | \\( H_{0} : r_{f1/f2} = 0 \\) | \\( H_{A} : r_{f1/f2} < 0 \\) |
| Q.P. | St. M.S.F. | \\( H_{0} : r_{f1/f2} = 0 \\) | \\( H_{A} : r_{f1/f2} > 0 \\) |
 

### Q.P. versus Race Placement

Quality of performance ought to corresponding to the proper rankings of horses in a race. That is, given a set of horses in a race, the horse who ranks in first place ought to have the highest Q.P., the horse who ranks in second place ought to have the second highest Q.P., the horse who ranks in last place ought to have the lowest Q.P., et cetera. The following table (adapted from \[[2, Fig. 3](https://www.jstor.org/stable/15639)\]) shows an example of what is expected of the Q.P.:

<br/>

| __Place__ | __Name__ | __Sex__ | __Weight (lb.)__ | __Time (sec.)__ | __Q. P.__ |
|-----------|----------|---------|------------------|-----------------|-----------|
| 1. | Canter | Colt | 117 | 100.8 | .9649 |
| 2. | Bubbling Over | " | 122 | 100.8+ | .9675 |
| 3. | Display | " | 119 | 101.1 | .9629 |
| 4. | Penstick | " | 119 | 101.3 | .9610 |
| 5. | Crusader | " | 117 | 101.4 | .9589 |
| 6. | Espino | " | 119 | 101.6 | .9582 |
| 7. | Mars | " | 119 | 101.8 | .9563 |
| 8. | Dress Parade | " | 119 | 102.0 | .9544 |
| 9. | Edith Cavell | Filly | 116 | 102.3 | .9597 |
| 10. | Acrostic | Colt | 119 | 102.4 | .9507 |
| 11. | Lancaster | " | 117 | 103.2 | .9425 |
| 12. | Flight of Time | " | 119 | 103.4 | .9414 |
| 13. | Marygrace | Filly | 119 | 105.0 | .9365 |
| 14. | Prince of Wales | Colt | 119 | 105.2 | .9254 |

# The Probability Resultant

H. H. Laughlin published a paper onto the _Proceedings of the National Academy of Sciences_ \[[1](https://doi.org/10.1073/pnas.21.11.601)\] in where he introduces the _probability resultant_ and the _probability repetant_. The main idea is that given a number "\\(n\\)" of Manerkonic cross-section distributions with a prediction-basis "\\(M\\)," it is possible to combine their evidences into a single "resultant" or "repetant" distribution. Such a distribution, expressed in terms of a "pattern formula," will, in theory, have a higher \\(K_{fc}\\)-value for its fluctuation centre "\\(FC\\)."

The __problem statement__ is as follows: \[todo\]

## General Method for Computing the Probability Resultant

### The F.C.-value for the Highest Common Probability

The following method comes from the Carnegie Yearbooks 1936-1937 \[[3, pp. 65-66](https://archive.org/details/yearbookcarne36193637carn/page/64/mode/2up)\]: the application of calculus and optimization techniques to working out the _F.C._ value such that it represents the "highest common probability," or the H.C.P., of the resulting probability-resultant distribution:

Given a set of _M_-values for manerkonic parameter estimating equations that parameterize a Manerkonic cross-section distribution of the form: \begin{equation}
K = K_{fc} \cdot \LARGE{\epsilon^{\frac{-(FC \sim R)^2}{2\sigma_\text{lft. or rgt.}^{2}}}}
\end{equation}

where \\(\displaystyle K_{fc} = \frac{n \text{ or area}}{\sigma \cdot \sqrt{2n}}\\)

## Examples

### Thoroughbred Inheritance of Racing Capacity

Laughlin \[[3](https://doi.org/10.1073/pnas.21.11.601)\] gave the following four (4) manerkons as an example for computing a probability-resultant and a probability-repetant distribution:

| __n__ | __Distribution Cross-section Formula__ |
|-------|----------------------------------------|
| \\( M_1 = 117.5 \\) | Racing Capacity of the Dam's Sire: \\[K = .1625 \LARGE{ \epsilon^{\frac{-(109.6367 \sim R)^2}{2\Big(12.27525 + \frac{109.6367 - R}{109.6367 \sim R} \cdot 1.54675\Big)^2}} }\\] |
| \\( M_2 = 97.5 \\) | Racing Capacity of the Sire: \\[K = .1488 \LARGE{ \epsilon^{\frac{-(98.0676 \sim R)^2}{2 \Big( 13.40495 + \frac{R - 98.0676}{R \sim 98.0676} \cdot 5.06325 \Big)^2}} }\\] |
| \\( M_3 = 127.5 \\) | Racing Capacity of the Dam: \\[ K = .1822 \LARGE{ \epsilon^{\frac{-(117.2577 \sim R)^2}{2 \Big( 10.9445 + \frac{117.2577 - R}{117.2577 \sim R} \cdot 6.06285 \Big)^2}} } \\] |
| \\( M_4 \\) | Any other independent \\( K = f(M, R) \\) Quality whatsoever: \\[ K = .10 \LARGE{ \epsilon^{\frac{-(99.0 \sim R)^2}{2(19.9470)^2}} } \\] |

## Appendix A: Resultant and Repetant Distribution Formulæ

1. Cumulative Area: \\[
K_c = \sum_{i = 1}^{n} \left[ K_{fc.i.} \cdot \LARGE{ \epsilon^{\frac{ -(FC_i - R)^2 }{2[\sigma_{s.i.} \pm (\sigma_{s.i.} - \sigma_\text{rgt.i.})]^2}} } \right]
\\]
    * Smoothed Cumulative Area: \\[
K_{c.s.} = K_{fc\Sigma} \cdot \LARGE{ \epsilon^{\frac{-(FC_\Sigma - R)^2}{2[\sigma_{s.c.} \pm ( \sigma_{s.c.} - \sigma_\text{rgt.c.} )]^2} }}
\\]
2. Resultant Area: \\[
K_P = \sum_{i = 1}^{n} \left[ \frac{K_{fc.i.}}{\sqrt{n}} \cdot \LARGE{\epsilon^{\frac{-[FC_i - [R + (\sqrt{n} - 1)(R - FC_\Sigma)]]^2}{2[\sigma_{s.i.} \pm (\sigma_{s.i.} - \sigma_\text{rgt.i.})]^2}}} \right]
\\]
     * Smoothed Resultant Area: \\[
K_{P.s.} = \frac{K_{FC_\Sigma}}{\sqrt{n}} \cdot \LARGE{ \epsilon^{\frac{-(FC_\Sigma - R)^2}{2\bigg[\frac{\sigma_{s.c.}}{\sqrt{n}} \pm \bigg( \frac{\sigma_{s.c.}}{\sqrt{n}} - \frac{\sigma_\text{rgt.c.}}{\sqrt{n}} \bigg)\bigg]^2}} }
\\]
3. Repetant Area: \\[
K_{R} = \left[ \sum_{i = 1}^{n} \frac{K_{fc.i.}}{n} \cdot \LARGE{ \epsilon^{\frac{-(FC_i - R)^2}{2[\sigma_{s.i.} \pm (\sigma_{s.i.} - \sigma_\text{rgt.i.})]^2} } } \right]
\\]
    * Smoothed Repetant Area: \\[
K_{R.s.} = \frac{K_{fc_\Sigma}}{n} \cdot \LARGE{ \epsilon^{\frac{-(FC_\Sigma - R)^2}{2[\sigma_{s.c.} \pm (\sigma_{s.c.} - \sigma_\text{rgt.c.})]^2}} }
\\]

where \\( n = \\) number of manerkons for each individual \\(M\\) predictor,

\\[ \displaystyle \sigma_s = \frac{q}{K_{fc} \cdot \sqrt{2\pi}} \\]
 
and 

\\[ \displaystyle \sigma_\text{rgt} = \frac{AP_r - q}{K_{fc} \cdot \sqrt{2\pi}} \\]

# References

1. In "1928-1929 Year Book," _Carnegie Institution of Washington_, no. 28, pp. 59--60  1929, [https://archive.org/details/yearbookcarne28192829carn/page/58/mode/2up](https://archive.org/details/yearbookcarne28192829carn/page/58/mode/2up)
2. H. H. Laughlin, “Racing Capacity in the Thoroughbred Horse. Part I. The Measure of Racing Capacity.,” _The Scientific Monthly_, vol. 38, no. 3, pp. 210–222, Mar. 1934, Available: [https://www.jstor.org/stable/15639](https://www.jstor.org/stable/15639)
3. H. H. Laughlin, "The Probability-Resultant," _Proceedings of the National Academy of Sciences_, vol. 21, no. 11, pp. 601--610, Nov. 1935, doi: [https://doi.org/10.1073/pnas.21.11.601]([https://doi.org/10.1073/pnas.21.11.601)
4. In "Year Book (Jul. 1, 1936--Jun. 30, 1937)," pp. 62--69, _Carnegie Institution of Washington_, no. 36, 1927, [https://archive.org/details/yearbookcarne36193637carn/mode/2up](https://archive.org/details/yearbookcarne36193637carn/mode/2up)

