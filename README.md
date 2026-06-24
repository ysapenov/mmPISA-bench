# mmPISA-bench

**Do LLMs Reason Equally Well Across 43 Languages?**

mmPISA-bench is a multilingual reasoning benchmark derived from publicly available OECD PISA assessments. The benchmark contains reasoning-focused multiple-choice questions represented in **43 languages**, using both **official human translations** and **machine-translated counterparts**.

The dataset was created to support systematic evaluation of multilingual reasoning capabilities of Large Language Models (LLMs) across languages, domains, and reasoning difficulty levels.

## Overview

Multilingual reasoning remains significantly less studied than English reasoning. Existing benchmarks often rely on machine-translated data, cover a limited number of languages, or focus on tasks that require less complex reasoning.

mmPISA-bench addresses these limitations by leveraging official OECD PISA translations that have undergone extensive localization and validation procedures, providing a high-quality foundation for cross-lingual evaluation.

The benchmark enables researchers to investigate:

* Cross-lingual reasoning consistency
* Effects of machine translation on reasoning performance
* Reasoning behavior across languages
* Token usage and inference cost disparities
* Language-specific strengths and weaknesses of LLMs

## Dataset Statistics

| Property              | Value |
| --------------------- | ----- |
| Languages             | 43    |
| Questions             | 25    |
| Human translations    | 1,075 |
| Machine translations  | 1,075 |
| Total data points     | 2,150 |
| Mathematics questions | 11    |
| Reading questions     | 14    |

### Languages

Albanian, Arabic, Azerbaijani, Basque, Bokmål, Bosnian, Bulgarian, Catalan, Chinese, Croatian, Czech, Danish, Dutch, English, Estonian, Finnish, French, Galician, Georgian, German, Greek, Hebrew, Hungarian, Icelandic, Indonesian, Italian, Japanese, Kazakh, Korean, Latvian, Lithuanian, Malay, Nynorsk, Polish, Portuguese, Russian, Serbian, Slovak, Slovenian, Spanish, Swedish, Thai, and Turkish.

## Data Source

The benchmark is constructed from publicly released questions from the OECD Programme for International Student Assessment (PISA):

* **PISA 2022 Mathematics**
* **PISA 2018 Reading**

Questions were selected according to the following criteria:

* Availability in a large number of official language translations
* Text-only format
* Multiple-choice answers
* Reasoning required to answer correctly

Only languages with complete coverage across both Reading and Mathematics subsets were retained.

## Dataset Structure

Each example contains:

* Question identifier
* Language
* Category (Mathematics or Reading)
* Difficulty level
* Context text
* Question text
* Answer options
* Correct answer
* Translation type (Human or Machine)

The benchmark is designed to facilitate controlled multilingual experiments while maintaining consistency across languages.

## Research Questions

The benchmark was developed to investigate three primary research questions:

### RQ1: Cross-Language Reasoning

How stable are frontier LLMs when answering reasoning-intensive questions across many languages?

### RQ2: Translation Effects

How does model performance on machine-translated questions compare to performance on official human translations?

### RQ3: Reasoning Length and Cost

Do reasoning length, token usage, and inference cost vary systematically across languages?

## Key Findings

Experiments involving over **107,000 model evaluations** revealed several important findings:

### Multilingual Reasoning is Strong

Modern frontier LLMs demonstrate robust reasoning capabilities across all 43 evaluated languages, achieving accuracy levels comparable to human PISA test-takers.

### Machine Translation Does Not Reduce Accuracy

Machine-translated questions perform similarly to official human translations, suggesting that high-quality synthetic translations may be sufficient for large-scale multilingual evaluations.

### Difficulty Matters

Question difficulty remains a strong predictor of model performance regardless of language or translation type.

### Reading Outperforms Mathematics

Both evaluated models achieved higher accuracy on reading comprehension tasks than on mathematics reasoning tasks.

### Cost and Accuracy Vary by Language

Some languages require substantially more tokens and higher inference costs while simultaneously producing lower accuracy.

These findings highlight the importance of evaluating both effectiveness and efficiency when comparing multilingual reasoning performance.

## Potential Applications

The dataset can be used for:

* Multilingual LLM benchmarking
* Cross-lingual reasoning research
* Translation quality evaluation
* Reasoning cost analysis
* Tokenization studies
* Low-resource language research
* Language-specific model diagnostics

## Citation

If you use this dataset, please cite:

```bibtex
@article{sapenov2026mmpisa,
  title={mmPISA-bench: Do LLMs Reason Equally Well Across 43 Languages?},
  author={Sapenov, Yerzhan and Savelka, Jaromir},
  journal={arXiv preprint arXiv:2606.07069},
  year={2026}
}
```

## License

This repository contains benchmark data derived from publicly available OECD PISA materials. Users are responsible for complying with the OECD terms and conditions governing the original assessment content.

## Acknowledgments

We thank the Organisation for Economic Co-operation and Development (OECD) for conducting the PISA assessments worldwide and for providing public access to assessment materials in numerous languages.



[Link to the paper](https://arxiv.org/abs/2606.07069)
