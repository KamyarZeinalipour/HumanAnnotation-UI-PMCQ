# PersianMCQ-Instruct · Human evaluation

[![Paper](https://img.shields.io/badge/LoResLM_2025-paper-b31b1b)](https://aclanthology.org/2025.loreslm-1.27/)
[![Main repo](https://img.shields.io/badge/GitHub-Persian__MCQ-181717?logo=github)](https://github.com/KamyarZeinalipour/Persian_MCQ)
[![Collection](https://img.shields.io/badge/%F0%9F%A4%97_Collection-PersianMCQ--Instruct-orange)](https://huggingface.co/collections/Kamyar-zeinalipour/persianmcq-instruct-loreslm-2025-6af481273fff746c25e21f62)

Human-evaluation protocol and results for [*PersianMCQ-Instruct: A Comprehensive Resource for Generating
Multiple-Choice Questions in Persian*](https://aclanthology.org/2025.loreslm-1.27/). Code, data and models are in the main repository,
[Persian_MCQ](https://github.com/KamyarZeinalipour/Persian_MCQ).

## Protocol

Two native Persian speakers, both postgraduate students, rated questions on a five-level scale
(inspired by Wang et al., 2022):

| Rating | Score | Definition (from the paper) |
|---|---:|---|
| A | 5 | Questions and answers are factually accurate and directly relate to significant concepts from the source text; meaningful and precise without grammatical issues |
| B | 4 | Mostly factual and related to the text, with minor grammatical issues or incomplete parts, but still meaningful |
| C | 3 | Loosely related to the text, addressing topics tangentially, or with serious grammatical issues, or incorrect answers |
| D | 2 | Factual inaccuracies, or minimally relevant to the text |
| E | 1 | Not generated, demonstrably wrong or misleading, or no clear connection to the text |

**Dataset quality.** 600 PersianMCQ-Instruct questions were rated (400 per expert, 200 shared;
agreement 0.96, Cohen's κ 0.86): 86.8% received an A.

**Model outputs.** 200 questions from each model before and after fine-tuning were rated (750 per
expert, 300 shared; agreement 0.96, Cohen's κ 0.95).

## Results (mean rating, A = 5 … E = 1)

| Model | Base | Fine-tuned |
|---|---:|---:|
| Gemma-2-9B-it | 2.72 | **2.78** |
| Llama-3.1-8B-Instruct | 3.31 | **4.51** |
| Mistral-7B-Instruct-v0.3 | 1.30 | **4.32** |
| PersianMCQ-Instruct (GPT-4o reference) | | 4.75 |

## Citation

```bibtex
@inproceedings{zeinalipour-etal-2025-persianmcq,
    title = "{P}ersian{MCQ}-Instruct: A Comprehensive Resource for Generating Multiple-Choice Questions in {P}ersian",
    author = "Zeinalipour, Kamyar  and
      Jamshidi, Neda  and
      Akbari, Fahimeh  and
      Maggini, Marco  and
      Bianchini, Monica  and
      Gori, Marco",
    editor = "Hettiarachchi, Hansi  and
      Ranasinghe, Tharindu  and
      Rayson, Paul  and
      Mitkov, Ruslan  and
      Gaber, Mohamed  and
      Premasiri, Damith  and
      Tan, Fiona Anting  and
      Uyangodage, Lasitha",
    booktitle = "Proceedings of the First Workshop on Language Models for Low-Resource Languages",
    month = jan,
    year = "2025",
    address = "Abu Dhabi, United Arab Emirates",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2025.loreslm-1.27/",
    pages = "344--372"
}
```
