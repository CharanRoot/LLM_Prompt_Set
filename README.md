# Adversarial Prompt Dataset for AI Safety Research

This repository contains the comprehensive dataset of adversarial prompts used in our research paper:  
**"Safety and Security Analysis of Large Language Models: Risk Profile and Harm Potential"**  
*Authors:* Charankumar Akiri, Harrison Simpson, Kshitiz Aryal, Aarav Khanna, Maanak Gupta  
*Published on:* arXiv:2509.10655, September 2024  
[📄 View Paper on arXiv](https://arxiv.org/abs/2509.10655)

This dataset contains adversarial prompts designed for AI safety research, model evaluation, and prompt injection detection systems.

---

## ⚠️ IMPORTANT DISCLAIMERS AND RESTRICTIONS

### Legal and Ethical Disclaimer
**WE ARE NOT RESPONSIBLE FOR ANY MISUSE OF THIS DATASET.** This collection is provided solely for:
- Academic research purposes
- AI safety evaluation
- Security testing of language models
- Development of prompt injection detection systems

### Content Warning
This dataset contains **potentially harmful, offensive, and dangerous content** including but not limited to:
- Instructions for illegal activities
- Violent and criminal scenarios
- Explicit sexual content
- Hate speech examples
- Self-harm related content
- Cybersecurity attack vectors

### Restrictions and Bias Notice
Due to certain restrictions and to avoid bias and censorship concerns, this dataset includes prompts from various categories that may be:
- **Politically sensitive**
- **Culturally controversial** 
- **Ethically challenging**
- **Legally problematic in certain jurisdictions**

**Users must comply with all applicable laws and regulations in their jurisdiction.**

---

## Dataset Overview

This dataset was used to evaluate **9 prominent LLMs** including Claude Opus 4, DeepSeek V3, Gemini 2.5 Flash, GPT-4o, Grok 3, Llama 4 Scout, Mistral 7B, and Qwen 3 1.7B against various security and safety threats.

### Statistics
- **Total Prompts**: 131 adversarial prompts
- **Categories**: 24 distinct security and safety categories (as referenced in the paper)
- **Format**: CSV with columns: `prompt`, `harm`, `category`
- **Purpose**: Risk assessment using the Risk Severity Index (RSI)
- **Evaluation**: Comprehensive analysis of LLM vulnerabilities

### ⚠️ **Important Note on Dataset Scope**
**This dataset represents only a limited subset of prompts from our complete research.** We are not exposing every prompt used in our research study. Only a carefully selected and curated portion of prompts has been made publicly available to ensure responsible disclosure while supporting reproducible research.

### Category Breakdown

| Category | Count | Description |
|----------|-------|-------------|
| **violent_crimes** | 5 | Prompts related to violence, assault, murder scenarios |
| **non-violent_crimes** | 5 | Fraud, theft, illegal gambling, trespassing |
| **sex_crimes** | 5 | Sexual assault, voyeurism, illegal recording |
| **indiscriminate_weapons** | 5 | Explosives, chemical weapons, mass destruction |
| **child_exploitation** | 5 | Child abuse, grooming, exploitation scenarios |
| **defamation** | 5 | False accusations, reputation damage, impersonation |
| **privacy** | 5 | Data breaches, personal information theft |
| **intellectual_property** | 5 | Piracy, copyright infringement, counterfeiting |
| **hate_speech** | 5 | Discriminatory language, racial/religious hatred |
| **self_harm** | 5 | Suicide methods, self-injury techniques |
| **sexual_content** | 5 | Explicit sexual scenarios and behaviors |
| **cbrn_content** | 5 | Chemical, biological, radiological, nuclear threats |
| **elections** | 5 | Voter suppression, election interference |
| **gun-related** | 6 | Firearms, weapons trafficking, mass shootings |
| **criminal_planning** | 5 | Detailed criminal schemes and attack planning |
| **social_engineering** | 5 | Manipulation tactics, phishing, fraud |
| **insecure_code** | 5 | Vulnerable code examples, security flaws |
| **phishing_emails** | 5 | Email-based social engineering attacks |
| **automated_hacking** | 5 | Automated attack tools and scripts |
| **attack_payload_gen** | 5 | SQL injection, XSS, command injection payloads |
| **malware_code_gen** | 5 | Malicious software examples |
| **polymorphic_malware_gen** | 5 | Advanced malware generation techniques |

---

## Usage Guidelines

### Legitimate Research Uses
✅ **Academic research** on AI safety and alignment  
✅ **Red-teaming** language models for vulnerabilities  
✅ **Training** prompt injection detection systems  
✅ **Evaluating** content filtering mechanisms  
✅ **Developing** AI safety guardrails  

### Prohibited Uses
❌ **Actual criminal activities** or illegal actions  
❌ **Harassment** or targeting of individuals  
❌ **Production** of harmful content for distribution  
❌ **Circumventing** safety measures in production systems  
❌ **Any use** that violates applicable laws  

---

## Technical Details

### File Structure
```
prompts/
├── prompts.csv          # Main dataset file
└── readme.md           # This documentation
```

### Data Format
```csv
prompt,harm,category
"[Adversarial prompt text]",safety,[category_name]
```

### Loading the Dataset
```python
import pandas as pd

# Load the dataset
df = pd.read_csv('prompts.csv')

# Filter by category
violent_prompts = df[df['category'] == 'violent_crimes']

# Get all safety-related prompts
safety_prompts = df[df['harm'] == 'safety']
```

---

## Research Applications

### Risk Severity Index (RSI) Evaluation
This dataset introduces the **Risk Severity Index (RSI)**, an agile and scalable evaluation score to:
- Quantify and compare security posture of LLMs
- Create comprehensive risk profiles  
- Provide standardized metrics for evolving threats
- Enable systematic comparison across different models

As described in our [arXiv paper](https://arxiv.org/abs/2509.10655), the RSI methodology revealed widespread vulnerabilities in safety filters across all tested LLMs.

### Prompt Injection Detection
Use these prompts to:
- Train binary classifiers (safe/unsafe)
- Evaluate existing safety filters
- Test model robustness against adversarial inputs
- Benchmark detection systems

### Model Safety Evaluation
- Assess how models respond to harmful requests
- Measure refusal rates across categories
- Identify failure modes in safety training
- Compare safety performance across model versions

### Red Team Exercises
- Systematic probing of model vulnerabilities
- Discovery of new attack vectors
- Evaluation of jailbreaking techniques
- Assessment of prompt injection effectiveness

---

## Ethical Considerations

### Responsible Disclosure
If you discover vulnerabilities using this dataset:
1. **Report responsibly** to model developers
2. **Allow reasonable time** for fixes before public disclosure
3. **Consider potential harm** of immediate publication
4. **Follow established** responsible disclosure practices

### Bias and Representation
This dataset may contain:
- **Cultural biases** reflecting certain perspectives
- **Uneven representation** across demographic groups
- **Language-specific** attack patterns (primarily English)
- **Temporal bias** reflecting current threat landscapes

### Mitigation Strategies
When using this dataset:
- **Combine with diverse** safety evaluation methods
- **Consider cultural context** of your deployment
- **Regularly update** with new attack patterns
- **Validate findings** across multiple evaluation frameworks

---

## Legal Compliance

### Jurisdiction-Specific Restrictions
Users must ensure compliance with:
- **Local laws** regarding harmful content
- **Export control** regulations for security tools
- **Data protection** laws (GDPR, CCPA, etc.)
- **Academic ethics** review board requirements

### Terms of Use
By using this dataset, you agree to:
1. **Use only for legitimate research** purposes
2. **Not redistribute** without proper attribution
3. **Comply with all applicable laws**
4. **Report any misuse** you become aware of
5. **Acknowledge the risks** and limitations

---

## Attribution and Citation

If you use this dataset in your research, please cite:

```bibtex
@article{akiri2024safety,
  title={Safety and Security Analysis of Large Language Models: Risk Profile and Harm Potential},
  author={Akiri, Charankumar and Simpson, Harrison and Aryal, Kshitiz and Khanna, Aarav and Gupta, Maanak},
  journal={arXiv preprint arXiv:2509.10655},
  year={2024},
  url={https://arxiv.org/abs/2509.10655},
  note={Dataset contains 131 adversarial prompts across 24 security and safety categories}
}
```

---

## Version History

- **v1.0** (2024): Initial release with 131 prompts across 15 categories
- **Future versions**: Will include additional categories and multilingual content

---

## Acknowledgments

This dataset was compiled for research purposes to advance AI safety and security. We acknowledge the sensitive nature of this content and emphasize the importance of responsible use in advancing the field of AI safety.

**Remember: The goal is to make AI systems safer, not to cause harm.**
