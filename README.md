**LLM Validation and Narrative Synthesis in Pain Neuroscience Education**

This repository contains data, code, and documentation related to a study that explores the use of large language models (LLMs) to analyze and synthesize pain neuroscience education (PNE) survey responses, based on the dataset described in Weisman et al., 2022.

Overview

This repository provides the tools and dataset supporting a three-part study investigating how large language models such as ChatGPT and Claude can:

Backward validate free-text pain education responses by classifying original group, valence, and statement.

Generate synthetic narratives representative of specific group-valence combinations.

Evaluate cross-model narrative interpretability via blind classification of synthetic responses.

These tasks were conducted on a free-text dataset derived from a previously published survey on attitudes toward ten pain neuroscience education (PNE) statements.

Repository Structure

data/
Q1_texts.txt to Q10_texts.txt - Raw free-text responses grouped by statement

results/
accuracy_tables.csv - Performance metrics per experiment
synthetic_narratives.csv - Model-generated narratives for all group-valence combinations

prompts/
optimized_prompts.md - Final prompt designs used in each experiment

analysis/
llm_evaluation_scripts.py - Scripts to process classification outputs and scores

Manuscript/
Manuscript_V5.docx - Full manuscript describing the study

README.md - This file

Data Summary

Participants: 1,319 respondents
Free-text entries: 4,252
PNE Statements: Q1 to Q10, inspired by metaphors used in pain neuroscience education

Groups (coded as integers):

Group 0 = Controls: individuals with no clinical background and no current pain

Group 1 = Patients: individuals with persistent or chronic pain

Group 2 = Healthcare Professionals without Pain (HCNoPain): licensed clinicians who are not currently in pain

Group 3 = Healthcare Professionals with Pain (HCPain): licensed clinicians who also report living with pain

Valence Codes:

1 = Positive response: supportive, constructive, or affirming attitudes toward the PNE statement

0 = Neutral response: mixed, evaluative, or undecided responses that lack strong emotional direction

-1 = Negative response: critical, dismissive, confused, or emotionally adverse reactions

Experiments

Experiment 1 – Blinded Context Prediction
LLMs were given anonymized free-text responses and tasked with predicting:

Which PNE statement (Q1–Q10) the narrative was responding to

Which group (0–3) wrote it

What emotional valence (-1, 0, +1) it expressed

Experiment 2 – Synthetic Narrative Generation
Claude Sonnet and Opus were prompted to generate short narratives simulating responses from specific group-valence combinations. These synthetic narratives were then tested blindly using the same classification task as in Experiment 1.

Experiment 3 – Cross-Model Validation
ChatGPT models were asked to classify Claude-generated narratives by predicting group, valence, and statement ID, testing the interpretability of synthetic outputs across models.

Key Findings

Valence classification was reliable across models (70 to 100 percent).
Statement classification accuracy varied from 60 to 80 percent, with ChatGPT-o3 and Claude Opus performing best.
Synthetic narratives were correctly classified in 65 to 73 percent of cases.
Narratives from Group 3 (HCPain) were the hardest to classify due to dual-perspective complexity (clinical and lived experience).

How to Cite

If you use this repository or its contents, please cite the following publication:

**Weisman, A., Yona, T., Gottlieb, U., and Masharawi, Y. (2022).
Attitudinal responses to current concepts and opinions from pain neuroscience education on social media.
Musculoskeletal Science and Practice, 59, 102551.
https://doi.org/10.1016/j.msksp.2022.102551**
