# DMPKBench

A domain-specific benchmark for evaluating LLMs and multi-agent systems in drug discovery DMPK (Drug Metabolism and Pharmacokinetics) tasks.

## Overview

DMPKBench is a large-scale high-quality benchmark designed to systematically evaluate the performance of large language models (LLMs) and multi-agent systems in drug discovery, with a particular focus on DMPK. Grounded in real-world pharmaceutical R&D workflows, DMPKBench translates industrial drug pipeline challenges into standardized, non-proprietary scientific tasks, enabling fair, reproducible, and application-relevant evaluation.

The benchmark emphasizes multi-disciplinary reasoning, multi-step quantitative analysis, and multi-modal understanding, addressing a critical gap in existing LLM benchmarks, which largely overlook drug development domains.

## Benchmark Scope and Core Modules

DMPKBench covers five expert-level competencies essential to DMPK practitioners:

1. DMPK experimental design and troubleshooting
Benchmark with expert-level exam questions and literature-derived CoT problems on experiment planning, hypothesis formulation, and root-cause analysis.

2. Interpretation of experimental results
Benchmark needs analysis of DMPK parameter tables and PK curves then identification of anomalous signals and mechanistic reasoning.

3. ADMET multi-parameter optimization (MPO)
Benchmark covering absorption, distribution, metabolism, excretion, and toxicity (ADMET) assessment for drug candidates or chemicals, supported by experimental evidence.

4. Pharmacokinetic (PK) modeling and simulation
Benchmark evaluating capabilities in multi-step quantitative reasoning, model construction, parameter derivation, and numerical calculation.

5. Preclinical-to-clinical PK translation to human body
Benchmark requiring integrated reasoning across species and data modalities for tasks like in vitro-in vivo extrapolation (IVIVE), first-in-human (FIH) dose prediction, and human drug–drug interaction (DDI) inference.

## Data Composition (Public)

The benchmark comprises a large-scale knowledge base of more than 100,000 question–answer pairs across multiple modalities, including multi-step quantitative reasoning (e.g. human dose prediction), troubleshooting of real-world DMPK data tables and pharmacokinetic curves, and integrated problem-solving scenarios.


| Domain              | Resource         | MCQ     | Quality             |
|---------------------|------------------|---------|---------------------|
| Experiment Design   | ABT Test         | 3190   | Expert QC           |
|                     | DrugBench¹       | 701     | LLM QC              |
| Result Interpretation | Public Case    | 100     | Expert QC           |
| PK Modeling         | Public Case      | 200     | Expert QC           |
| ADMET MPO           | SPR Data         | 127,600 | Experimental evidence |
| Human Translation   | Public Case      | 10     | Expert QC           |

<sup>1</sup> Derived from PubMed

We have released partial data across five dimensions, as shown in the table. The complete dataset is available under request for academic use only upon acceptance of the related manuscript.

## Reference
[1] Jie Li, Baiming chen, Zhiyang Zou, Rumin Zhang, Sheng Ding, Jinjiang Guo. DMPKBench: A Multi-Modal Benchmark for Evaluating LLMs and Agents in Drug Discovery DMPK Tasks. NeurIPS 2025, Workshop: AI for Science.
[2] Jie Li, Baiming Chen, Renhe Liu, Zhiyang Zou, Jinjiang Guo. DrugBench: A Data-Mining Pipeline for Generating CoT-driven LLM Benchmark in Drug Discovery.
[3] AI Kongming (http://datascience.ghddi.org)
