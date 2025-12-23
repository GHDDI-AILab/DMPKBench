# DMPKBench

A domain-specific benchmark for evaluating LLMs and multi-agent systems in drug discovery DMPK (Drug Metabolism and Pharmacokinetics) tasks.

## Overview

DMPKBench is a large-scale high-quality benchmark designed to systematically evaluate the performance of LLMs and multi-agent systems in drug discovery, with a particular focus on DMPK. Grounded in real-world pharmaceutical R&D workflows, DMPKBench translates industrial drug pipeline challenges into standardized, non-proprietary scientific tasks, enabling fair, reproducible, and application-relevant evaluation.

The benchmark emphasizes multi-disciplinary reasoning, multi-step quantitative analysis, and multi-modal understanding, addressing a critical gap in existing LLM benchmarks, which largely overlook drug development domains.

## Benchmark Scope and Core Modules

DMPKBench covers five expert-level competencies essential to DMPK practitioners:

1. DMPK experimental design and troubleshooting
Benchmark with expert-level exam questions and literature-derived CoT problems[2] on experiment planning, hypothesis formulation, and root-cause analysis.

2. Interpretation of experimental results
Benchmark needs analysis of DMPK parameter tables and PK curves then identification of anomalous signals and mechanistic reasoning.

3. ADMET multi-parameter optimization (MPO)
Benchmark covering absorption, distribution, metabolism, excretion, and toxicity (ADMET) assessment for drug candidates or chemicals, supported by experimental evidence from AI KongMing[3].

4. Pharmacokinetic (PK) modeling and simulation
Benchmark evaluating capabilities in multi-step quantitative reasoning, model construction, parameter derivation, and numerical calculation.

5. Preclinical-to-clinical PK translation to human body
Benchmark requiring integrated reasoning across species and data modalities for tasks like in vitro-in vivo extrapolation (IVIVE), first-in-human (FIH) dose prediction, and human drug–drug interaction (DDI) inference.

## Data Composition

### Public Benchmark Set

We have released the benchmark to the public for academic use only. As shown in the table, the benchmark covers five dimensions, and comprises a large-scale knowledge base of more than 120,000 question–answer pairs across multiple modalities, including compounds SMILES stuctures, multi-step quantitative formula calculation, real-world DMPK data tables and PK curves. All data were standardized into an LLM-compatible JSONL format, with multi-modal inputs (tables, figures, PK curves) stored in Markdown for enhanced accessibility. Rigorous quality control was ensured through multi-round expert validation, formula verification, and inter-rater agreement checks. Due to licensing constraints, the ADMET MPO subset is released with questions and options without answers. Your own testing accuracy can be provided upon request.

| Domain              | Resource         | MCQ     | Quality             |
|---------------------|------------------|---------|---------------------|
| Experiment Design   | ABT Test         | 3190   | Expert QC           |
|                     | DrugBench[2]¹       | 701     | LLM QC              |
| Result Interpretation | Public Case    | 100     | Expert QC           |
| PK Modeling         | Public Case      | 200     | Expert QC           |
| ADMET MPO           | SPR Data         | 127,600 | Experimental evidence[3] |
| Human Translation   | Public Case      | 10     | Expert QC           |

<sup>1</sup> Derived from PubMed

### Unresolved Challenge Subset
Unresolved challenge subset comprises questions that were answered incorrectly by all evaluated models in the paper (OpenAI o3, GPT-4.1, Claude 4 Sonnet, DeepSeek-R1, and DeepSeek-V3). These results are based on a single run and may vary across runs. The prevalence of unresolved questions differs markedly by task type: knowledge-driven tasks (e.g., ABT test and DrugBench from PubMed CoT) account for only 4.8% of all questions, whereas multi-modal QA constitutes 28.26%. This indicates that multi-modal tasks remain a major limitation for current LLMs. This subset is intended for frontier model evaluation and multi-agent system research.

### Prompting and Evaluation
To ensure reproducibility and reduce prompt-related variability, relevant validation prompts used in this study are also available. The benchmark and validated prompts enable large-scale evaluation through close-set accuracy testing, LLM-assisted automated assessment of open-ended responses, and expert-driven qualitative analysis, while remaining fully compatible with SFT, RFT, and agent-based system optimization.

## Reference
[1] Jie Li, Baiming chen, Zhiyang Zou, Rumin Zhang, Sheng Ding, Jinjiang Guo. DMPKBench: A Multi-Modal Benchmark for Evaluating LLMs and Agents in Drug Discovery DMPK Tasks. NeurIPS 2025, Workshop: AI for Science.

[2] Jie Li, Baiming Chen, Renhe Liu, Zhiyang Zou, Jinjiang Guo. DrugBench: A Data-Mining Pipeline for Generating CoT-driven LLM Benchmark in Drug Discovery.

[3] AI KongMing (http://datascience.ghddi.org)
