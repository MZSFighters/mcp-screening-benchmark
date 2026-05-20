# MMTV-Breast Cancer Literature Screening Benchmark

A high-quality, expert-validated benchmark dataset for evaluating language model performance on complex biomedical literature classification tasks. This dataset was curated and used in this [preprint](https://arxiv.org/abs/2512.06502)


## 📋 Dataset Overview

This dataset consists of **100 medical research papers** (title–abstract pairs) with expert-adjudicated relevance labels indicating whether each paper's title and abstract contribute to understanding the potential role of **HMTV/MMTV-like viruses in causing human breast cancer**.

Labels were assigned through detailed, iterative expert discussions led by a specialist in infectious diseases and oncology, with ambiguous cases revisited to ensure consistency. The dataset is designed as a rigorous evaluation benchmark that requires interdisciplinary reasoning across virology, oncology, genetics, pathology, epidemiology, and immunology.

---

## 🏷️ Label Definitions

Each paper is assigned one of three labels:

| Label | Description |
|---|---|
| `Relevant` | Gives causal evidence (for or against) whether HMTV/MMTV-like virus or its species/family causes breast cancer or other cancers (in humans or animal models), **or** contains a theoretical model for how the virus might cause breast cancer. |
| <code>Somewhat&nbsp;Relevant</code> | Mentions both HMTV/MMTV-like virus and breast cancer without causal arguments, **or** examines whether other microbes cause breast cancer in a way that could plausibly generalise to HMTV/MMTV-like virus. |
| `Irrelevant` | Does not fulfil the criteria for Relevant or Somewhat Relevant. |

### Label Distribution

| Label | Count |
|---|---|
| Relevant | 38 |
| Somewhat Relevant | 15 |
| Irrelevant | 47 |
| **Total** | **100** |

---

## 📁 Dataset File

| File | Format | Description |
|---|---|---|
| `mmtv-breast-cancer-screening-benchmark.json` | JSON | filename, title, abstract, target_label|


## 🚀 Usage

### Python (JSON)

```python
import json

with open("dataset.json", "r") as f:
    data = json.load(f)

print(data[0])
```

## 📄 Citation
 
If you use this dataset in your research, please cite:
 
```bibtex
@article{dawood2025small,
  title={Small Language Models Can Use Nuanced Reasoning For Health Science Research Classification: A Microbial-Oncogenesis Case Study},
  author={Dawood, Muhammed Muaaz and Moonsamy, Mohammad Zaid and Kokkas, Kaela and Wang, Hairong and Breiman, Robert F and Klein, Richard and Sekyi, Emmanuel K and Bassett, Bruce A},
  journal={arXiv preprint arXiv:2512.06502},
  year={2025}
}
```
 
