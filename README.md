<div align="center">

# FAS-R1

### Difficulty-Adaptive Reinforcement Learning for Multi-Task Face Anti-Spoofing

Hongyang Wang · Yichen Shi · Hongrui Li · Yiru Huo · Jun Feng · Zitong Yu

</div>

FAS-R1 is a difficulty-adaptive reinforcement learning framework for **multi-task face anti-spoofing**. A shared multimodal large language model supports **authenticity classification**, **attack-type recognition**, and **attack-region localization**, returning an image-related rationale followed by the task-specific prediction.

## Framework

FAS-R1 first establishes a rationale-before-answer response format through annotation-constrained CoT supervised fine-tuning on **FAS-R1-23K**. Reinforcement learning then combines two complementary components:

- **Degradation-Simulated Augmentation (DSA):** generate responses from original and degraded images for joint reward comparison, while keeping policy updates conditioned on the original image.
- **Difficulty-Aware GRPO (DA-GRPO):** track task–attack subgroup proficiency and increase the relative update weights of lower-proficiency groups.

![Fig. 5: DSA and DA-GRPO in the reinforcement learning stage](assets/fig5.png)

## Qualitative Examples

### Authenticity Classification

A replay-attack example comparing model predictions and their explanations. FAS-R1 predicts spoof and describes screen-like reflections as supporting evidence.

![Authenticity predictions and explanations on a replay attack](assets/qualitative_authenticity.png)

### Attack-Region Localization

A partial-eye attack example comparing predicted regions. Green boxes indicate ground-truth annotations; red boxes indicate model predictions.

![Attack-region localization comparisons on a partial-eye attack](assets/qualitative_localization.png)

## Citation

If you find this work useful, please cite:

```bibtex
@misc{wang_fasr1,
  title  = {FAS-R1: Difficulty-Adaptive Reinforcement Learning for Multi-Task Face Anti-Spoofing},
  author = {Hongyang Wang and Yichen Shi and Hongrui Li and Yiru Huo and Jun Feng and Zitong Yu}
}
```

## Code Release

**Code will be released soon.**
