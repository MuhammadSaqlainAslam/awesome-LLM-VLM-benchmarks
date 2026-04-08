# Global MMLU: Understanding and Addressing Cultural and Linguistic Biases in Multilingual Evaluation (2024)

## Problem
Multilingual LLM evaluations have relied on machine-translated MMLU — but MMLU itself is deeply Western-centric: 28% of its questions require culturally-sensitive knowledge, 84.9% of geography questions focus on North America or Europe, and 73.9% of cultural questions specifically require knowledge of the United States. Simply translating a biased English benchmark into other languages does not yield culturally representative multilingual evaluation. Model rankings on translated MMLU are misleading, especially for low-resource languages and culturally sensitive domains.

## Method
**200+ professional and community annotators** verified translation quality and labelled each of 2,850 sampled MMLU questions for cultural sensitivity across three categories: Cultural Knowledge, Geographical/Regional Knowledge, and Dialect Knowledge. Each question was reviewed by at least 3 annotators (96.4% by more than 3); inter-annotator agreement measured by Krippendorff's Alpha. Language coverage uses a three-tier approach: 14 languages professionally translated with post-edits, 11 languages crowdsourced, and 16 languages machine-translated. Two evaluation subsets are released: **CS (Culturally Sensitive)** and **CA (Culturally Agnostic)**. A compact **Global-MMLU Lite** subset is also provided. Published by **Cohere For AI** and partners including EPFL, Hugging Face, MIT, KAIST, and Meta AI Research (arXiv: 2412.03304, December 2024).

## Benchmarks / Datasets
- **601,734 total instances across 42 languages**
  - Test split: 589,764 (14,042 per language × 42 languages)
  - Dev split: 11,970 (285 per language × 42 languages)
- **42 languages** spanning high-resource (20), mid-resource (9), and low-resource (13): including Arabic, Bengali, Chinese (Simplified), French, German, Hindi, Indonesian, Japanese, Korean, Portuguese, Russian, Spanish, Swahili, Turkish, Vietnamese, Yoruba, Amharic, Hausa, Igbo, Kyrgyz, Malagasy, Nepali, Sinhala, Somali, and 18 more
- **57 subjects** across 6 categories: STEM, Humanities, Social Sciences, Medical, Business, Other
- **Annotated subset:** 2,850 questions labelled for cultural sensitivity (CS: 33,264 total instances; CA: 86,436 total instances across annotated portion)
- Two subsets: **CS** (Culturally Sensitive) and **CA** (Culturally Agnostic)

## Key Results

**Cultural bias findings:**
- **28%** of MMLU questions are Culturally Sensitive
- Geography questions: 64.5% require North American knowledge; 20.4% European
- Cultural questions: **86.5% Western-centric**; 73.9% specifically require U.S. knowledge
- Humanities: 68% culturally sensitive; STEM: only 3.15%

**Model ranking instability (14 frontier models evaluated):**
- On CA datasets: average **3.4 rank changes, 3.7 position shifts** vs. standard MMLU
- On CS datasets: average **5.7 rank changes, 7.3 position shifts** — model rankings become unreliable
- Conclusion: MMLU-based multilingual rankings are not trustworthy, especially for CS subsets and low-resource languages

## FoxBrain Relevance
Global MMLU's Culturally Agnostic (CA) subset is the appropriate evaluation set for FoxBrain's multilingual deployments across Foxconn's global manufacturing sites — it strips out Western cultural bias that would artificially deflate non-English performance measurements. The low-resource language coverage is particularly relevant for Foxconn's Southeast Asian manufacturing facilities (Indonesian, Vietnamese, Filipino). The 7.3 average rank-position shift on CS tasks warns that standard multilingual benchmark rankings should not be used to choose FoxBrain's language capabilities — domain-specific CA evaluation is mandatory for accurate capability measurement across Foxconn's operational languages.

---
*Back to [Main Digest](../README.md)*
