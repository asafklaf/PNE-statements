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
survey_feedback.txt - Responses entered at the end of the survey, reflecting on the overall experience

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
Free-text entries: 4,252 in Q1–Q10, plus additional entries in survey_feedback
PNE Statements: Q1 to Q10, inspired by metaphors used in pain neuroscience education

Groups (coded as integers):

Group 0 = Controls: individuals with no clinical background and no current pain

Group 1 = Patients: individuals with persistent or chronic pain

Group 2 = Healthcare Professionals without Pain (HCNoPain): licensed clinicians who are not currently in pain

Group 3 = Healthcare Professionals with Pain (HCPain): licensed clinicians who also report living with pain

Valence Codes:

1 = Positive response: supportive, constructive, or affirming attitudes toward the PNE statement or the survey

0 = Neutral response: mixed, evaluative, or undecided responses that lack strong emotional direction

-1 = Negative response: critical, dismissive, confused, or emotionally adverse reactions

Survey Feedback Responses

In addition to reactions to the ten PNE statements, the dataset includes a separate file with participants’ free-text feedback at the end of the survey. These entries capture overall impressions, frustrations, support, or confusion about the survey and its messages. Each of these feedback narratives has been coded with the same group and valence labels used for Q1–Q10 responses, enabling them to be analyzed with identical classification tasks.

How to Cite

If you use this repository or its contents, please cite the following publication:

Weisman, A., Yona, T., Gottlieb, U., and Masharawi, Y. (2022).
Attitudinal responses to current concepts and opinions from pain neuroscience education on social media.
Musculoskeletal Science and Practice, 59, 102551.
https://doi.org/10.1016/j.msksp.2022.102551

**Contact**

For questions or contributions, please contact:
Asaf Weisman
Spinal Research Laboratory
Tel Aviv University
Email: asafweisman@gmail.com

**License**

This project is licensed under the Creative Commons Attribution-NonCommercial 4.0 International License
https://creativecommons.org/licenses/by-nc/4.0/
