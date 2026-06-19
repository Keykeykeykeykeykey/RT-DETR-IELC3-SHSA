Official PyTorch implementation of the paper:

> **Robust Object Detection in Optical Remote Sensing Imagery via Partial-Channel Self-Attention and Intensity-Enhanced Feature Fusion**

---

## Overview

Optical remote sensing object detection remains challenging due to sparse object distribution, large scale variation, and complex background interference. To address these issues, we propose **AIRT-Det**, a lightweight CNN–Transformer hybrid detector built upon the RT-DETR framework.

AIRT-Det introduces two complementary modules:

### SHSAIFI
**Single-Head Self-Attention-based Internal Feature Interaction**

- Performs self-attention on only a subset of informative feature channels.
- Reduces redundant global interactions.
- Improves contextual representation efficiency.
- Maintains low computational overhead.

### IFusion
**Intensity Enhance Fusion**

- Introduces intensity-regulated nonlinear feature modulation.
- Stabilizes cross-scale feature interaction.
- Enhances discriminative object responses.
- Improves multi-scale feature fusion for small and low-contrast targets.

The proposed framework achieves superior detection performance while preserving real-time inference capability.

---

## Framework

The overall architecture consists of:

1. CNN Backbone Feature Extraction
2. SHSAIFI-enhanced Transformer Encoder
3. IFusion-based Multi-scale Feature Fusion
4. RT-DETR Decoder

---

## Key Features

- End-to-End Object Detection
- Real-Time Inference
- Lightweight Design
- Efficient Global Context Modeling
- Adaptive Multi-scale Feature Fusion
- State-of-the-Art Performance on Remote Sensing Benchmarks

---


---

## Dataset Preparation

### DOTA-v1.5

Download:

https://captain-whu.github.io/DOTA/

Directory structure:

```text
datasets/
└── DOTA-v1.5/
    ├── images/
    ├── labels/
    └── split/
```

### HRSC2016

Download:

http://www.escience.cn/people/liuzikun/DataSet.html

```text
datasets/
└── HRSC2016/
    ├── images/
    ├── annotations/
    └── labels/
```

### DIOR

Download:

https://gcheng-nwpu.github.io

```text
datasets/
└── DIOR/
    ├── JPEGImages/
    ├── Annotations/
    └── labels/
```


---

## Evaluation

```bash
python val.py \
    --weights runs/train/best.pt \
    --data dota.yaml
```



---



## Code Availability

The source code associated with this study is publicly available at:

```text
https://github.com/yourname/AIRT-Det
```

Archived version (DOI):

```text
https://doi.org/xxxxxxxx
```

---

## Citation

If you find this work useful, please cite:

```bibtex
@article{xu2026airtdet,
  title={Robust Object Detection in Optical Remote Sensing Imagery via Partial-Channel Self-Attention and Intensity-Enhanced Feature Fusion},
  author={Xu, Keke and Zhu, Yongzhen and Liu, Xianglei and Zheng, Wei and Li, Huanxu and Zhao, Jiaqi and Chen, Mengchao},
  journal={Scientific Reports},
  year={2026}
}
```

---

## Acknowledgements

This work is built upon the following excellent open-source projects:

- RT-DETR
- Ultralytics
- PyTorch

We sincerely thank the authors for making their code publicly available.

