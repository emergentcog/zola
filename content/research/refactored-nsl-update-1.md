+++
title="Refactored Neural Scaling Laws -- Update 1"
date=2026-05-08
draft=false
[taxonomies]
tags=["blog", "ai", "machine intelligence", "neural scaling laws"]
+++


This is a short update about my research: [Critical Depth and the Scaling Law Paradox: A Refactored Resource Model](https://doi.org/10.20944/preprints202512.1471.v1)

My proposed refactored model of the [*Chinchilla*](https://doi.org/10.48550/arXiv.2203.15556)-based NSL may have some empirical data/grounding.

Indeed, a piece of research by [A. Karpathy](https://github.com/karpathy/nanochat/discussions/420) seems to bring some backing to the predictions of my refactored model. Here follows my [reply](https://github.com/karpathy/nanochat/discussions/420#discussioncomment-15454282)--reproduced to his experiments:

---

Hi Andrej,

Thank you for sharing your detailed and granular empirical analysis.

Building on an earlier piece of research: _[A Resource Based Model For Neural Scaling Laws](https://doi.org/10.48550/arXiv.2402.05164)_
I've come up with a [refined NSL profile](https://doi.org/10.20944/preprints202512.1471.v1) for the NSL, as follows:

- Structural Phase (below critical depth): ℓ ∝ N<sub>p</sub><sup>-2/3</sup>
- Redundancy Phase (standard scaling): ℓ ∝ N<sub>p</sub><sup>-1/3</sup>
- Width-Only Scaling: ℓ ∝ N<sub>p</sub><sup>-1/2</sup>

From my theoretical derivation with width-only scaling (fixed depth): N<sub>p</sub> ∝ N<sup>2</sup>

This implies that N ∝ N<sub>p</sub><sup>1/2</sup>. Since FLOPS (C) is grows proportionally to the resources (neurons) (N) this means that N ∝C<sup>0.5</sup> which is pretty close to your 0.49 for the optimal model size exponent.

This seems to suggest that width-only scaling beyond critical depth is not just theoretically sound but also matches (at least in your setting) the optimal scaling behavior you've observed in practice.
The slight deviation from 0.5 (0.49) is consistent with real-world constraints while validating the core theoretical framework.

Additionally, here is an illustration(from my preprint) graph / projection in relation with the Chinchilla paper:

<img width="5461" height="2298" alt="neural_scaling_external_labels" src="https://github.com/user-attachments/assets/e9954627-d508-45b6-b217-5732673690e2" />

This alignment between theory and empirical evidence reinforces the value of your miniseries approach -- it's helping to bridge the gap between theoretical understanding and practical implementation of scaling laws.

Best regards,
Tolga

---

In addition, another piece of research that echoes my refactored model predictions is a paper from the DeepSeek-AI team: [DeepSeek LLM: Scaling Open-Source Language Models with Longtermism](https://doi.org/10.48550/arXiv.2401.02954). Here is one element echoing my model's predictions.

- The 0.5243 exponent is within a measurement error of my model's -1/2 for the width-only scaling prediction.

Finally, there are other research that fall in line with my model's predictions. This may allow/require for a new preprint on the NSL. This subject could be even more important if one wants to "align" policies/governance stuff based on [evals](https://www.apolloresearch.ai/science/we-need-a-science-of-evals/).



