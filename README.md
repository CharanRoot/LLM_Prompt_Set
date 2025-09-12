# Prompt Library for “[Your Paper Title]”

This repository contains the full set of prompts used in our research paper:  
**“[Full Paper Title]”**  
*Authors:* [Your Names]  
*Published in:* IEEE [Conference/Journal Name], [Year]  
[Link to the paper / DOI]

---

## Table of Contents

- [Overview](#overview)  
- [Prompt Dataset](#prompt-dataset)  
- [Repository Structure](#repository-structure)  
- [Usage](#usage)  
- [License](#license)  
- [How to Cite](#how-to-cite)  
- [Contributing](#contributing)

---

## Overview

The prompt library is intended to support reproducibility, transparency, and further research in LLM security and safety. The prompts were used to probe large language models across various tasks, including standard NLP tasks and adversarial scenarios designed to expose vulnerabilities.  

This repo includes **baseline**, **adversarial**, and **evaluation** prompts matching those in the paper.

---

## Prompt Dataset

- The set contains *N* unique prompts used in our experiments (e.g., *500+ prompts*).  
- Categories include:  
  - Baseline tasks (summarisation, translation, reasoning)  
  - Adversarial / red-teaming prompts (probing for harmful/gaming / jailbreak scenarios)  
  - Evaluation prompts (tasks to measure bias, logical consistency, etc.)  
- Languages: [mention languages if more than one]  
- Format: plain text files, one prompt per line or per file depending on category.

---

## Repository Structure

```
├── prompts/
│   ├── baseline/
│   │   ├── summarization.txt
│   │   ├── translation.txt
│   │   └── reasoning.txt
│   ├── adversarial/
│   │   ├── jailbreak.txt
│   │   ├── bias_probe.txt
│   │   └── malicious_content.txt
│   ├── evaluation/
│   │   ├── logical_consistency.txt
│   │   ├── inference_time.txt
│   │   └── fairness.txt
│   └── README-prompts.md  # descriptions of each prompt file/category
└── README.md               # this file
```

---

## Usage

You can plug these prompts into any LLM or evaluation pipeline. Below is a minimal example using Python:

```python
# Example usage with a generic LLM API

with open("prompts/adversarial/jailbreak.txt") as f:
    prompt_text = f.read()

response = llm_client.generate(
    prompt=prompt_text,
    max_tokens=100,
    temperature=0.7
)

print(response)
```

To reproduce experiments from the paper:

1. Use the exact prompt texts as stored.  
2. Match any preprocessing (if described in Methods).  
3. Use the same evaluation metrics.

---

## License

This prompt library is released under the **[Your Chosen License]** (e.g., *Apache-2.0* or *MIT*). You are free to use, distribute, and modify the prompts under these terms, with proper citation.

---

## How to Cite

If you use these prompt sets in your work, please cite our paper:

```bibtex
@inproceedings{yourlastname2025,
  title        = {Your Full Paper Title},
  author       = {Your Name and Co‑authors},
  booktitle    = {Proceedings of IEEE [Conference/Journal]},
  year         = {2025},
  doi          = {xx.xxxx/xxxxxxx}
}
```

---

## Contributing

We welcome contributions, feedback, and suggestions.  

If you create new prompt sets (e.g., in new languages or probing new vulnerability types), feel free to open a pull request.  

Please adhere to the same style and formatting used in this repo (one prompt per line / text file per category), and include clear metadata (e.g., category, purpose) in any additions.

---

## Content Warning

Some prompts in this dataset are adversarial or designed to probe harmful or biased content. They may include language or ideas that are offensive, disturbing, or inappropriate for some audiences. Use discretion.
