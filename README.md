<div align="center">

# 🧭 Awesome Test-Time Adaptation

[![Awesome](https://awesome.re/badge-flat2.svg)](https://awesome.re)
[![GitHub stars](https://img.shields.io/github/stars/0917Ray/Awesome-Test-Time-Adaptation?style=social)](https://github.com/0917Ray/Awesome-Test-Time-Adaptation/stargazers)
[![Last commit](https://img.shields.io/github/last-commit/0917Ray/Awesome-Test-Time-Adaptation?logo=github)](https://github.com/0917Ray/Awesome-Test-Time-Adaptation/commits/main)
[![License: CC0-1.0](https://img.shields.io/badge/License-CC0--1.0-blue.svg)](LICENSE)
[![PRs welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**A curated, year-by-year map of Test-Time Adaptation (TTA), Test-Time
Training (TTT), and Continual Test-Time Adaptation (CTTA).**

Paper links, official implementations, and project pages in one place.

</div>

---

## 🚩 News

- **[2026-09] Initial release.** The first version covers representative work
  from the foundations of modern TTA through recent adaptation methods.
- **[Ongoing] Contributions are welcome.** See the
  [contribution guide](CONTRIBUTING.md) to add a paper or correct metadata.

## 🗺️ Navigation

- [Scope and terminology](#-scope-and-terminology)
- [Start here](#-start-here)
- [Browse by method](#-browse-by-method)
- [Papers by year](#-papers-by-year)
  - [2026](#2026)
  - [2025](#2025)
  - [2024](#2024)
  - [2023](#2023)
  - [2022](#2022)
  - [2021](#2021)
  - [2020](#2020)
- [Surveys and benchmarks](#-surveys-and-benchmarks)
- [Contributing](#-contributing)
- [Citation](#-citation)

## 🎯 Scope and terminology

This list focuses on methods that change a model, its statistics, prompts,
memory, or predictions using information available at deployment time.

| Term | Working definition |
| --- | --- |
| **TTA** | Adapts a trained model to unlabeled test data under distribution shift. |
| **TTT** | Uses a test-time learning objective, often prepared jointly with the source task during training. |
| **CTTA / OTTA** | Adapts continually to a non-stationary or temporally correlated test stream. |
| **TTPT** | Tunes prompts, caches, or other lightweight components of a vision-language model at test time. |

Conventional domain adaptation that requires simultaneous access to labeled
source data is outside the main scope. Closely related source-free methods are
included when they directly shaped modern TTA.

## 🌱 Start here

- **A practical first method:** **Tent** is a compact baseline built around
  entropy minimization and normalization statistics.
- **For per-sample adaptation:** **MEMO** adapts from augmented views of one
  test example.
- **For changing test streams:** **CoTTA**, **SAR**, and **RoTTA** are useful
  entry points for continual adaptation.
- **For evaluation:** **On Pitfalls of Test-Time Adaptation** and the
  **TTAB** codebase document failure modes and realistic protocols.

### Badge legend

![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)
![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)
![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)
![Project](https://img.shields.io/badge/Project-Website-0969da?logo=googlechrome&logoColor=white)
`Method family` ⭐ Landmark or especially useful starting point

## 🧩 Browse by method

| Method family | Representative papers |
| --- | --- |
| Self-supervision and consistency | TTT, TTT++, MEMO, SPA |
| Entropy and uncertainty | Tent, EATA, SAR, DeYO |
| Statistics, prototypes, and parameter-free adaptation | BN Adapt, T3A, LAME, TDA, FreeTTA |
| Continual and online adaptation | CoTTA, NOTE, RMT, EcoTTA, RoTTA, ViDA |
| Vision-language adaptation | TDA, DynaPrompt |
| Forward-only or black-box search | FOA |
| Evaluation and benchmarking | TTAB, Online TTA under time constraints |

## 📚 Papers by year

### 2026

- **SPeaR** - *Test-Time Adaptation with Steering Primitives for Realigning
  Representations*. arXiv 2026. `Representation steering`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2609.24111)
  - Keeps the pretrained network frozen and adapts lightweight steering
    modules inserted between stages.

### 2025

- **SPA** - *Self-Bootstrapping for Versatile Test-Time Adaptation*. ICML
  2025. `Self-training`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2504.08010)
  - Builds an adaptable supervisory signal from the model itself across
    multiple deployment settings.

- **ReCAP** - *Beyond Entropy: Region Confidence Proxy for Wild Test-Time
  Adaptation*. ICML 2025. `Wild TTA`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2505.20704)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/hzcar/ReCAP)
  - Uses regional confidence to select reliable adaptation signals in mixed
    and open-world test streams.

- **DynaPrompt** - *Dynamic Test-Time Prompt Tuning*. ICLR 2025. `TTPT`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2501.16404)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/zzzx1224/DynaPrompt)
  - Maintains dynamic prompts for online adaptation of vision-language
    models.

- **FreeTTA** - *Free on the Fly: Enhancing Flexibility in Test-Time
  Adaptation with Online EM*. CVPR 2025. `Training-free`
  [![Paper](https://img.shields.io/badge/Paper-CVPR-005a9c)](https://openaccess.thecvf.com/content/CVPR2025/html/Dai_Free_on_the_Fly_Enhancing_Flexibility_in_Test-Time_Adaptation_with_CVPR_2025_paper.html)
  - Uses online expectation-maximization to adapt predictions without
    gradient-based parameter updates.

### 2024

- ⭐ **DeYO** - *Entropy Is Not Enough for Test-Time Adaptation: From the
  Perspective of Disentangled Factors*. ICLR 2024. `Sample selection`
  [![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)](https://openreview.net/forum?id=9w3iw8wDuE)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/Jhyun17/DeYO)
  - Filters unreliable samples using prediction certainty and input-level
    information before entropy-based updates.

- **FOA** - *Test-Time Model Adaptation with Only Forward Passes*. ICML 2024.
  `Forward-only`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2404.01650)
  - Replaces backpropagation with derivative-free optimization over a small
    set of adaptation parameters.

- **TDA** - *Efficient Test-Time Adaptation of Vision-Language Models*. CVPR
  2024. `Cache-based`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2403.18293)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/kdiAAA/TDA)
  - Adapts CLIP predictions through positive and negative caches without
    gradient updates.

- **TEA** - *TEA: Test-Time Energy Adaptation*. CVPR 2024. `Energy-based`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2311.14402)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/yuanyige/tea)
  - Uses an energy-based objective to align the model with the test
    distribution.

- **ViDA** - *Homeostatic Visual Domain Adapter for Continual Test Time
  Adaptation*. ICLR 2024. `CTTA`
  [![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)](https://openreview.net/forum?id=sJ88Wg5Bp5)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/Yangsenqiao/vida)
  - Uses complementary adapters to balance plasticity and retention in a
    changing test stream.

- **Universal TTA** - *Universal Test-Time Adaptation through Weight
  Ensembling, Diversity Weighting, and Prior Correction*. WACV 2024.
  `Universal TTA`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2306.00650)
  - Combines model ensembling and prior correction for diverse test-time
    shifts.

### 2023

- ⭐ **SAR** - *Towards Stable Test-Time Adaptation in Dynamic Wild World*.
  ICLR 2023. `Sharpness-aware`
  [![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)](https://openreview.net/forum?id=g2YraF75Tj)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/mr-eggplant/SAR)
  - Couples reliable entropy selection with sharpness-aware updates to resist
    model collapse.

- ⭐ **RoTTA** - *Robust Test-Time Adaptation in Dynamic Scenarios*. CVPR
  2023. `CTTA`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2303.13899)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/BIT-DA/RoTTA)
  - Uses a category-balanced memory and robust teacher updates for correlated
    streams.

- **EcoTTA** - *Memory-Efficient Continual Test-Time Adaptation via
  Self-Distilled Regularization*. CVPR 2023. `Efficient CTTA`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2303.01904)
  [![Project](https://img.shields.io/badge/Project-Website-0969da?logo=googlechrome&logoColor=white)](https://sites.google.com/view/junha/ecotta)
  - Adapts compact meta networks while regularizing intermediate features to
    reduce memory and forgetting.

- **RMT** - *Robust Mean Teacher for Continual and Gradual Test-Time
  Adaptation*. CVPR 2023. `CTTA`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2211.13081)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/mariodoebler/test-time-adaptation)
  - Stabilizes a teacher-student system with source prototypes and symmetric
    cross-entropy.

- **TTAB** - *On Pitfalls of Test-Time Adaptation*. ICML 2023.
  `Benchmarking`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2306.03536)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/LINs-lab/ttab)
  - Studies protocol choices and failure modes that can reverse conclusions
    about adaptation methods.

### 2022

- ⭐ **CoTTA** - *Continual Test-Time Domain Adaptation*. CVPR 2022. `CTTA`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2203.13591)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/qinenergy/cotta)
  - Combines weight-averaged teachers, augmentation, and stochastic model
    restoration for long test streams.

- ⭐ **EATA** - *Efficient Test-Time Model Adaptation without Forgetting*.
  ICML 2022. `Entropy minimization`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2204.02610)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/mr-eggplant/EATA)
  - Selects informative samples and constrains important parameters to improve
    efficiency and limit forgetting.

- ⭐ **MEMO** - *Test Time Robustness via Adaptation and Augmentation*.
  NeurIPS 2022. `Instance-wise`
  [![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)](https://openreview.net/forum?id=vn74m_tWu8O)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/zhangmarvin/memo)
  - Minimizes prediction entropy across augmentations of a single test
    example.

- **NOTE** - *Robust Continual Test-Time Adaptation Against Temporal
  Correlation*. NeurIPS 2022. `CTTA`
  [![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)](https://openreview.net/forum?id=E9HNxrCFZPV)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/TaesikGong/NOTE)
  - Addresses biased normalization statistics caused by temporally correlated
    test samples.

- **LAME** - *Parameter-Free Online Test-Time Adaptation*. CVPR 2022.
  `Parameter-free`
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2201.05718)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/fiveai/LAME)
  - Refines output probabilities through graph-based label assignment without
    updating model parameters.

### 2021

- ⭐ **Tent** - *Tent: Fully Test-Time Adaptation by Entropy Minimization*.
  ICLR 2021. `Entropy minimization`
  [![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)](https://openreview.net/forum?id=uXl3bZLkr3c)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/DequanWang/tent)
  - Updates normalization statistics and affine parameters by minimizing test
    prediction entropy.

- **T3A** - *Test-Time Classifier Adjustment Module for Model-Agnostic Domain
  Generalization*. NeurIPS 2021. `Prototypes`
  [![Paper](https://img.shields.io/badge/Paper-NeurIPS-652c8f)](https://proceedings.neurips.cc/paper/2021/hash/1415fe9fea0fa1e45dddcff5682239a0-Abstract.html)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/matsuolab/T3A)
  - Adjusts the classifier using pseudo-prototypes collected from unlabeled
    test samples.

- **TTT++** - *When Does Self-Supervised Test-Time Training Fail or Thrive?*
  NeurIPS 2021. `Self-supervision`
  [![OpenReview](https://img.shields.io/badge/Paper-OpenReview-8c1b13)](https://openreview.net/forum?id=86NHK__yFDl)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/vita-epfl/ttt-plus-plus)
  - Improves feature alignment and training design for more reliable
    self-supervised adaptation.

### 2020

- ⭐ **TTT** - *Test-Time Training with Self-Supervision for Generalization
  under Distribution Shifts*. ICML 2020. `Self-supervision`
  [![Paper](https://img.shields.io/badge/Paper-PMLR-0085ca)](https://proceedings.mlr.press/v119/sun20b.html)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/yueatsprograms/ttt_cifar_release)
  [![Project](https://img.shields.io/badge/Project-Website-0969da?logo=googlechrome&logoColor=white)](https://yueatsprograms.github.io/ttt/home.html)
  - Establishes the modern TTT setup by optimizing a self-supervised auxiliary
    task for each test input.

- **BN Adapt** - *Improving Robustness against Common Corruptions by Covariate
  Shift Adaptation*. NeurIPS 2020. `Normalization statistics`
  [![Paper](https://img.shields.io/badge/Paper-NeurIPS-652c8f)](https://proceedings.neurips.cc/paper/2020/hash/85690f81aadc1749175c187784afc9ee-Abstract.html)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/bethgelab/robustness)
  - Re-estimates normalization statistics from target batches as a simple
    adaptation baseline.

## 🔭 Surveys and benchmarks

- **A Comprehensive Survey on Test-Time Adaptation under Distribution
  Shifts**. IJCV 2024.
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2303.15361)
- **In Search of Lost Online Test-Time Adaptation: A Survey**. IJCV 2024.
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2310.20199)
- **Beyond Model Adaptation at Test Time: A Survey**. arXiv 2024.
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2411.03687)
- **Benchmarking Test-Time Adaptation against Distribution Shifts in Image
  Classification**. arXiv 2023.
  [![Paper](https://img.shields.io/badge/Paper-arXiv-b31b1b?logo=arxiv&logoColor=white)](https://arxiv.org/abs/2307.03133)
  [![Code](https://img.shields.io/badge/Code-GitHub-181717?logo=github)](https://github.com/yuyongcan/benchmark-tta)

## 🤝 Contributing

Paper additions, metadata fixes, and new categories are welcome. Please read
[CONTRIBUTING.md](CONTRIBUTING.md) before opening a pull request. Keep entries
chronological, link the primary paper, and prefer official code repositories.

## 🙏 Acknowledgements

The presentation is inspired by
[Awesome World Models](https://github.com/knightnemo/Awesome-World-Models) and
the broader [Awesome](https://github.com/sindresorhus/awesome) community.

Related collections include
[awesome-test-time-adaptation](https://github.com/tim-learn/awesome-test-time-adaptation)
and
[awesome-source-free-test-time-adaptation](https://github.com/YuejiangLIU/awesome-source-free-test-time-adaptation).

## 📝 Citation

If this collection helps your research, please cite the repository:

```bibtex
@misc{fang2026awesometta,
  title        = {Awesome Test-Time Adaptation},
  author       = {Changrui Fang},
  year         = {2026},
  howpublished = {\url{https://github.com/0917Ray/Awesome-Test-Time-Adaptation}}
}
```

---

<div align="center">

If this list is useful, consider giving it a ⭐ and sharing it with the TTA
community.

</div>
