# DMPKBench

A comprehansive benchmark designed to evaluate LLM and multi-agent performance in DMPK-related tasks.

This repository hosts the benchmark datasets of DMPKBench, a multi-modal benchmark designed to evaluate large language models (LLMs) and multi-agents in the domain of drug discovery DMPK. DMPKBench covers five core competencies essential to domain experts: experimental design and testing, interpretation of experimental results, ADMET multi-parameter optimization, pharmacokinetic (PK) modeling and simulation, and preclinical-to-clinical translation to the human body. The benchmark comprises a large-scale knowledge base of more than 100,000 question–answer pairs across multiple modalities, including multi-step quantitative reasoning (e.g. human dose prediction), troubleshooting of real-world DMPK data tables and pharmacokinetic curves, and integrated problem-solving scenarios.

## Data Composition (Public)

| Domain              | Resource         | MCQ     | Quality             |
|---------------------|------------------|---------|---------------------|
| Experiment Design   | ABT Test         | 1000   | Expert QC           |
|                     | DrugBench¹       | 701     | LLM QC              |
| Result Interpretation | Public Case    | 100     | Expert QC           |
| PK Modeling         | Public Case      | 100     | Expert QC           |
| ADMET MPO           | SPR Data         | 650 | Experimental evidence |
| Human Translation   | Public Case      | --      | Expert QC           |

<sup>1</sup> Derived from PubMed

We have released partial data across five dimensions, as shown in the table. The complete dataset is available under request for academic use only upon acceptance of the related manuscript.
