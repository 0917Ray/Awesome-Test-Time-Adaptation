# 🧩 Topics in Test-Time Adaptation

This index is the topic-oriented view of the collection. The year sections in
the [main README](README.md#papers-by-year) are the canonical paper records;
the links below point back to those records so that metadata stays in one
place.

> A paper may appear under more than one topic. This is intentional: TTA
> methods often combine an objective, an adaptation mechanism, and a deployment
> protocol.

## 🧪 Self-supervision and consistency

Methods that learn from auxiliary tasks, augmentations, or self-generated
signals at deployment time.

- [TTT](README.md#ttt) (2020) - self-supervised auxiliary task.
- [TTT++](README.md#ttt-plus-plus) (2021) - self-supervised feature alignment.
- [MEMO](README.md#memo) (2022) - augmentation consistency for one sample.
- [SPA](README.md#spa) (2025) - self-bootstrapped supervision.
- [EcoTTA](README.md#ecotta) (2023) - self-distilled regularization.

## 📉 Entropy, uncertainty, and sample selection

Methods that use confidence, entropy, uncertainty, or reliability filtering to
decide which test examples should influence adaptation.

- [Tent](README.md#tent) (2021) - entropy minimization.
- [EATA](README.md#eata) (2022) - informative sample selection.
- [SAR](README.md#sar) (2023) - reliable entropy selection and sharpness awareness.
- [DeYO](README.md#deyo) (2024) - disentangled-factor sample selection.
- [ReCAP](README.md#recap) (2025) - regional confidence proxy.
- [TEA](README.md#tea) (2024) - energy-based confidence signal.

## 🧮 Statistics, prototypes, and parameter-free adaptation

Methods that adapt normalization statistics, classifier prototypes, cached
examples, or output probabilities without full model updates.

- [BN Adapt](README.md#bn-adapt) (2020) - target-domain normalization statistics.
- [T3A](README.md#t3a) (2021) - pseudo-prototype classifier adjustment.
- [LAME](README.md#lame) (2022) - parameter-free graph label assignment.
- [Universal TTA](README.md#universal-tta) (2024) - weight ensembles and prior correction.
- [TDA](README.md#tda) (2024) - positive and negative CLIP caches.
- [FreeTTA](README.md#freetta) (2025) - online expectation-maximization.

## 🔄 Continual and online streams

Methods designed for sequential, non-stationary, or temporally correlated test
data.

- [CoTTA](README.md#cotta) (2022) - teacher averaging and stochastic restoration.
- [NOTE](README.md#note) (2022) - temporal-correlation robustness.
- [RMT](README.md#rmt) (2023) - robust mean teacher.
- [RoTTA](README.md#rotta) (2023) - category-balanced memory.
- [EcoTTA](README.md#ecotta) (2023) - memory-efficient continual adaptation.
- [ViDA](README.md#vida) (2024) - homeostatic visual domain adapters.
- [ReCAP](README.md#recap) (2025) - wild test-stream adaptation.
- [DynaPrompt](README.md#dynaprompt) (2025) - dynamic online prompts.

## 👁️ Vision-language and prompt adaptation

Methods that adapt CLIP-like models through prompt parameters, caches, or
vision-language representations.

- [TDA](README.md#tda) (2024) - efficient CLIP test-time adaptation.
- [DynaPrompt](README.md#dynaprompt) (2025) - dynamic prompt tuning.
- [ViDA](README.md#vida) (2024) - adapter-based visual adaptation.

## ⚡ Efficient and forward-only adaptation

Methods that reduce gradient cost, memory, or the number of updated
parameters.

- [FOA](README.md#foa) (2024) - forward-only derivative-free adaptation.
- [LAME](README.md#lame) (2022) - no parameter updates.
- [FreeTTA](README.md#freetta) (2025) - online EM without gradients.
- [EcoTTA](README.md#ecotta) (2023) - compact meta networks.
- [EATA](README.md#eata) (2022) - efficient updates with anti-forgetting constraints.

## 🧬 Representation steering and lightweight components

Methods that adapt a small set of modules, adapters, or representation-level
components while keeping most of the pretrained model stable.

- [SPeaR](README.md#spear) (2026) - lightweight representation steering.
- [ViDA](README.md#vida) (2024) - homeostatic visual domain adapters.
- [DynaPrompt](README.md#dynaprompt) (2025) - lightweight dynamic prompts.

## 📊 Surveys, evaluation, and benchmarks

Resources that define protocols, compare methods, or document common failure
modes.

- [TTAB](README.md#ttab) (2023) - pitfalls and evaluation protocols.
- [A Comprehensive Survey on TTA](README.md#surveys-and-benchmarks) (2024).
- [In Search of Lost Online TTA](README.md#surveys-and-benchmarks) (2024).
- [Beyond Model Adaptation at Test Time](README.md#surveys-and-benchmarks) (2024).
- [Benchmarking TTA against Distribution Shifts](README.md#surveys-and-benchmarks) (2023).

## ➕ Adding a topic

When adding a paper, keep its primary record under the appropriate year in the
[README](README.md), add a stable anchor, and then link it from one or more
topic sections here. See [CONTRIBUTING.md](CONTRIBUTING.md) for the entry
format.
