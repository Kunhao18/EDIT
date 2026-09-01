# EDIT: Evidence-Diagnosed Intervention Training for Rule-Faithful LLM Grading

[![Project Page](https://img.shields.io/badge/Project-Page-blue)](https://kunhao.site/EDIT/)
[![arXiv](https://img.shields.io/badge/arXiv-2606.06350-red)](https://arxiv.org/abs/2606.06350)
[![Conference](https://img.shields.io/badge/Findings-EMNLP%202026-green)](https://2026.emnlp.org/)

Official repository for the EMNLP 2026 Findings paper
**"EDIT: Evidence-Diagnosed Intervention Training for Rule-Faithful LLM Grading"**
by Zhihao Wu\*, Linhai Zhang\*, Taiyi Wang\*, Runcong Zhao, Peter Andrews, Cesare Aloisi, and Yulan He
(\*equal contribution).

> **🚧 Code coming soon.** We are cleaning up the training and evaluation pipeline and will
> release it here. In the meantime, see the [project page](https://kunhao.site/EDIT/) and the
> [paper](https://arxiv.org/abs/2606.06350).

## Overview

Reliable rubric grading requires more than accurate score prediction: each judgement must be
grounded in the mark scheme and evidence from the student answer. **EDIT** (Evidence-Diagnosed
Intervention Training) is a two-phase framework for training rubric-faithful LLM graders:

- **EDIT-SFT — Rule-Aware Atomic Intervention.** Locates problematic reasoning steps using the
  model's own internal signals — a posterior belief probe over the final mark and mask-based
  grounding audits — then revises only those local steps with a rubric checklist as privileged
  context, and fine-tunes on the corrected trajectories.
- **EDIT-RL — Belief-Guided Reward Shaping.** Calibrates the grader with GRPO, augmenting the
  outcome reward with a penalty on large harmful mid-trajectory belief drifts while still
  allowing benign exploration.

![The EDIT pipeline](https://raw.githubusercontent.com/Kunhao18/EDIT/page/static/images/method.png)

On two real-world, multi-subject grading benchmarks (SAS-Bench and a proprietary GCSE science
collection), EDIT consistently outperforms strong SFT and RL baselines on both in-domain and
out-of-domain splits, and under deterministic rubric-edit interventions it is the most
rule-responsive of all evaluated systems.

## Citation

```bibtex
@inproceedings{wu2026edit,
  title     = {{EDIT}: Evidence-Diagnosed Intervention Training for Rule-Faithful {LLM} Grading},
  author    = {Wu, Zhihao and Zhang, Linhai and Wang, Taiyi and Zhao, Runcong and Andrews, Peter and Aloisi, Cesare and He, Yulan},
  booktitle = {Findings of the Association for Computational Linguistics: EMNLP 2026},
  publisher = {Association for Computational Linguistics},
  year      = {2026},
  url       = {https://arxiv.org/abs/2606.06350}
}
```

## Contact

For questions, please contact [zhihao.2.wu@kcl.ac.uk](mailto:zhihao.2.wu@kcl.ac.uk) or open an issue.
