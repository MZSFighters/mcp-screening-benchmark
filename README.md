# mcp-screening-benchmark

# MMTV Breast Cancer Literature Screening Benchmark

A high-quality, expert-validated benchmark dataset for evaluating language model performance on complex biomedical literature classification tasks. This dataset was curated and used in the paper:

> **Democratizing Discovery: Cost-Efficient Scientific Literature Screening with Open-Weight SLMs**
> Mohammad Zaid Moonsamy, Muhammed Muaaz Dawood, Kaela Kokkas, Hairong Wang, Robert F. Breiman, Richard Klein, Emmanuel K. Sekyi, Bruce A. Bassett
> *University of the Witwatersrand, Johannesburg, South Africa*

---

## 📋 Dataset Overview

This dataset consists of **100 medical research papers** (title–abstract pairs) with expert-adjudicated relevance labels indicating whether each paper contributes to understanding the potential role of **HMTV/MMTV-like viruses in causing human breast cancer**.

Labels were assigned through detailed, iterative expert discussions led by a specialist in infectious diseases and oncology, with ambiguous cases revisited to ensure consistency. The dataset is designed as a rigorous evaluation benchmark that requires interdisciplinary reasoning across virology, oncology, genetics, pathology, epidemiology, and immunology.

---

## 🏷️ Label Definitions

Each paper is assigned one of three labels:

| Label | Description |
|---|---|
| `Relevant` | Gives causal evidence (for or against) whether HMTV/MMTV-like virus or its species/family causes breast cancer or other cancers (in humans or animal models), **or** contains a theoretical model for how the virus might cause breast cancer. |
| `Somewhat Relevant` | Mentions both HMTV/MMTV-like virus and breast cancer without causal arguments, **or** examines whether other microbes cause breast cancer in a way that could plausibly generalise to HMTV/MMTV-like virus. |
| `Irrelevant` | Does not fulfil the criteria for Relevant or Somewhat Relevant. |

### Label Distribution

| Label | Count |
|---|---|
| Relevant | 38 |
| Somewhat Relevant | 15 |
| Irrelevant | 47 |
| **Total** | **100** |

---

## 📁 Dataset Files

| File | Format | Description |
|---|---|---|
| `dataset.csv` | CSV | Title, abstract, label, and split columns |
| `dataset.json` | JSON | Same data in JSON format |

### Fields

- **`id`** — Unique paper identifier
- **`title`** — Paper title
- **`abstract`** — Paper abstract
- **`label`** — Expert-assigned relevance label (`Relevant`, `Somewhat Relevant`, `Irrelevant`)
- **`split`** — Dataset split (`train`, `val`, `test`)


## 🚀 Usage

### Python (JSON)

```python
import json

with open("dataset.json", "r") as f:
    data = json.load(f)

print(data[0])
```

---

## 📄 Citation

If you use this dataset in your research, please cite:

```bibtex
@inproceedings{moonsamy2025democratizing,
  title     = {Democratizing Discovery: Cost-Efficient Scientific Literature Screening with Open-Weight SLMs},
  author    = {Moonsamy, Mohammad Zaid and Dawood, Muhammed Muaaz and Kokkas, Kaela and Wang, Hairong and Breiman, Robert F. and Klein, Richard and Sekyi, Emmanuel K. and Bassett, Bruce A.},
  year      = {2025}
}
```

---

## 🔒 License

This dataset is released for academic and research purposes. Please refer to the `LICENSE` file for details.
