---
layout: post
title: "Some Notes on the Manerkonic Probability Resultant"
author:
- Alexander Ahmann
date: 2025-12-17

journal: "Data Blogging and Working Technical Reports"
volume: 1
number: 2

draft: true

---

<p style="font-size:22px;">Table of Contents</p>

* contents
{:toc}

## Background

H. H. Laughlin published a paper onto the _Proceedings of the National Academy of Sciences_ \[[1](https://doi.org/10.1073/pnas.21.11.601)\] in where he introduces the _probability resultant_ and the _probability repetant_. The main idea is that given a number "\\(n\\)" of Manerkonic cross-section distributions with a prediction-basis "\\(M\\)," it is possible to combine their evidences into a single "resultant" or "repetant" distribution. Such a distribution, expressed in terms of a "pattern formula," will, in theory, have a higher \\(K_{fc}\\)-value for its fluctuation centre "\\(FC\\)."

The __problem statement__ is as follows: \[todo\]

## Calculation Procedure

### Procedure Outline 

### The F.C.-value for the Highest Common Probability

The following method comes from the Carnegie Yearbooks 1936-1937 \[[1, pp. 65-66](https://archive.org/details/yearbookcarne36193637carn/page/64/mode/2up)\]: the application of calculus and optimization techniques to working out the _F.C._ value such that it represents the "highest common probability," or the H.C.P., of the resulting probability-resultant distribution:

Given a set of _M_-values for manerkonic parameter estimating equations that parameterize a Manerkonic cross-section distribution of the form: \begin{equation}
K = K_{fc} \cdot \LARGE{\epsilon^{\frac{-(FC \sim R)^2}{2\sigma_\text{lft. or rgt.}^{2}}}}
\end{equation}

where \\(\displaystyle K_{fc} = \frac{n \text{ or area}}{\sigma \cdot \sqrt{2n}}\\)

## Examples

### Thoroughbred Inheritance of Racing Capacity

Laughlin \[[1](https://doi.org/10.1073/pnas.21.11.601)\] gave the following four (4) manerkons as an example for computing a probability-resultant and a probability-repetant distribution:

| __n__ | __Distribution Cross-section Formula__ |
|-------|----------------------------------------|
| \\( M_1 = 117.5 \\) | Racing Capacity of the Dam's Sire: \\[K = .1625 \LARGE{ \epsilon^{\frac{-(109.6367 \sim R)^2}{2\Big(12.27525 + \frac{109.6367 - R}{109.6367 \sim R} \cdot 1.54675\Big)^2}} }\\] |
| \\( M_2 = 97.5 \\) | Racing Capacity of the Sire: \\[K = .1488 \LARGE{ \epsilon^{\frac{-(98.0676 \sim R)^2}{2 \Big( 13.40495 + \frac{R - 98.0676}{R \sim 98.0676} \cdot 5.06325 \Big)^2}} }\\] |
| \\( M_3 = 127.5 \\) | Racing Capacity of the Dam: \\[ K = .1822 \LARGE{ \epsilon^{\frac{-(117.2577 \sim R)^2}{2 \Big( 10.9445 + \frac{117.2577 - R}{117.2577 \sim R} \cdot 6.06285 \Big)^2}} } \\] |
| \\( M_4 \\) | Any other independent \\( K = f(M, R) \\) Quality whatsoever: \\[ K = .10 \LARGE{ \epsilon^{\frac{-(99.0 \sim R)^2}{2(19.9470)^2}} } \\] |

## Changelog

* 1.0. Initial Publishing, archives: \[1\]\[2\]\[3\]

## References

1. H. H. Laughlin, "The Probability-Resultant," _Proceedings of the National Academy of Sciences_, vol. 21, no. 11, pp. 601--610, Nov. 1935, doi: [https://doi.org/10.1073/pnas.21.11.601]([https://doi.org/10.1073/pnas.21.11.601)
2. In "Year Book (Jul. 1, 1936--Jun. 30, 1937)," pp. 62--69, _Carnegie Institution of Washington_, no. 36, 1927, [https://archive.org/details/yearbookcarne36193637carn/mode/2up](https://archive.org/details/yearbookcarne36193637carn/mode/2up)

## Appendix: Resultant and Repetant Distribution Formulæ

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

