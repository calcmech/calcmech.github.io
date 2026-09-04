---
layout: post
title: "Testing Laughlin: On the Validity of the St. M.S.F. and Actual M.S.F."
author:
- Alexander Ahmann
date: 2025-12-16

journal: "Data Blogging and Working Technical Reports"
volume: 1
number: 1

draft: true

abstract: "Something of an \"open notebook\" for brainstorming ideas regarding the testing of the standard mean furlongs per second and quality of performance ratios. Here I ask: \"how well does the St. M. S. F. and Q.P. metrics do in terms of predicting more fundamental measures like time, in seconds, that it took a race horse to finish the race?\""
---

<p style="font-size:22px;">Table of Contents</p>

* contents
{:toc}

## Background

### Theoretical Measure: The Principle Added Functions

Laughlin devised what he called the _Principle of Added Functions_ for inventing "mathematical yardsticks," or a theoretical measure for complex phenomena that are composed of, or derived from, more fundamental measurements. The idea of these kinds of measuring tools can, to my knowledge, be traced back to physics. Rather than trying to directly observe a natural phenomena, scientists try to "infer" what a phenomena might look like with theoretical frameworks. 

For example, mechanical force, which is measured in netwons, is the product of a physical body's mass (typically measured in kilograms) and its acceleration (typically measured in metres per squared seconds). External mechanical forces acting on a body would then be "added up," and then divided by said body's mass to produce what Laughlin may have called a "mathematical yardstick" for acceleration, as measured by \\( \displaystyle \frac{[\text{metres}]}{[\text{second}]^2} \\), which is then used to derive more fundamental measures of velocity and displacement, measured in \\( \displaystyle \frac{[\text{metres}]}{[\text{second}]}\\) and \\( \displaystyle [\text{metres}] \\) respectively. 

To test the physics theory in question, the demonstrator would take one of the derived functions, like displacement, and compare its predictions to experimental results. If the displacement function can make testable and falsifiable predictions, and if they have yet to be disproven, then the demonstrator is justified in their belief that the theoretical framework is sound and a proper description of reality. I think that Laughlin applied reasoning to measuring quality of performance, and later racing capacity, in the thoroughbred horse.

## Laughlin's Assements of Racehorse Performace

### The Standard Mean Seconds per Furlong

Laughlin put his Principle of Added Functions to work by inventing a set of "mathematical yardsticks" that attempts to measure standard mean seconds per furlong. He went about constructing this measure by identifying what he thought were relevant features, writing down formulæ that described how these features affected the horse's racing capacity, and fitting the parameters of his formulæ to tabulated results from previous horse races. The _standard mean seconds per furlong_ \[[1, pp 59--60](https://archive.org/details/yearbookcarne28192829carn/page/60/mode/2up)\], or St. M.S.F., measures takes the basic form of:

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

### The Actual Mean Seconds per Furlong

### The Quality of Performance

\begin{equation}
  Q. P. = \frac{\text{Standard Mean Seconds per Furlong.}}{\text{Actual Mean Seconds Per Furlong.}}
\end{equation}

## Proposed Experiments

### Q.P. and Kinematic Features

Quality of performance ultimately measures an individual horse's performance to run a certain number of  furlongs in a certain amount of time. Horses that run the most furlongs in the least amount of time are expected to have a high Q.P. outcome. Likewise, horses that run the least furlongs in the most amount of time are expected to have a low Q.P. outcome. A test that I can perform is to analyse the correlation between quality of performance, and the number of furlongs ran divided by the number of seconds passed, or, the horse's _speed_. I will assume a Pearson product-moment correlation coefficient for linear, which is defined as:

$$\begin{equation}
\large{ r_{x \text{ vs. } y} = \frac{\sum_{(x, y) \in \omega}^{n} (x - \bar{x}) (y - \bar{y})}{ n \cdot \sqrt{\frac{\sum_{x} (x - \bar{x})^2}{n}} \sqrt{\frac{\sum_{y} (y - \bar{y})^2}{n}} } \Large}
\end{equation}$$

Specifically, I want to measure the strength of the correlation \\(r\\) of quality of performance versus racehorse speed, which I will formalise by making formula 2 into several hypothesis tests with features as shown in the following table:

| __Feature 1__ | __vs. Feature 2__ | __Null Hypothesis__ | __vs. Alt. Hypothesis__ |
|---------------|-------------------|---------------------|-------------------------|
| Q.P. | Time (sec.) | \\( H_{0} : r_{f1/f2} = 0 \\) | \\( H_{A} : r_{f1/f2} < 0 \\) |
| Q.P. | St. M.S.F. | \\( H_{0} : r_{f1/f2} = 0 \\) | \\( H_{A} : r_{f1/f2} > 0 \\) |
 

### Q.P. versus Race Performance Rankings

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

## Preliminary Results

## References

1. In "1928-1929 Year Book," _Carnegie Institution of Washington_, no. 28, pp. 59--60  1929, [https://archive.org/details/yearbookcarne28192829carn/page/58/mode/2up](https://archive.org/details/yearbookcarne28192829carn/page/58/mode/2up)
2. H. H. Laughlin, “Racing Capacity in the Thoroughbred Horse. Part I. The Measure of Racing Capacity.,” _The Scientific Monthly_, vol. 38, no. 3, pp. 210–222, Mar. 1934, Available: [https://www.jstor.org/stable/15639](https://www.jstor.org/stable/15639)

