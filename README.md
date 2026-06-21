# Gradient-Free Adversarial Prompt Injection on Retrieval-Augmented Generation via Differential Evolution

## Abstract

Retrieval-augmented generation (RAG) systems improve question answering by grounding language models in retrieved documents, but this dependence on retrieval exposes them to prompt-based adversarial manipulation. We propose a method name**DeRAG** (KDD 2025 Workshop), and extend for QRS 2026 as **DEER**, a gradient-free attack that uses Differential Evolution (DE) to optimize adversarial prompt suffixes that promote a targeted incorrect or harmful document in the retrieval ranking, requiring only query-level access to the retriever's ranking scores. Evaluated on BEIR QA benchmarks across both sparse and dense retrievers, our method matches or surpasses recent baselines, including GGPP and Pandora. We further introduce a readability-aware suffix construction that improves attack stealth by increasing fluency, and show that the resulting suffixes evade a RoBERTa-based safety classifier, driving detection performance to near-chance accuracy. Finally, we show that successful promotion of harmful content materially alters downstream RAG responses, highlighting the risks of prompt-level vulnerabilities in retrieval-centric QA pipelines.

## Repository Structure and Instructions

### Clone the Repository

```bash
git clone https://github.com/pen9rum/Rag_attack_DeRag
cd Rag_attack_DeRag
```

## Run the Evaluation Notebooks

Open Jupyter Notebook and execute the following two notebooks in order:

1. **`DE_attack_evaluation.ipynb`**  
   Evaluates the attack performance of the DE-based method on the selected RAG datasets.

2. **`Loss_Comparison.ipynb`**  
   Compares different loss behaviors across baseline and DE-optimized suffixes.

## Environment Setup

Please ensure all dependencies are installed. Requirements are in **DE_attack_evaluation.ipynb** 


## Datasets

This repository supports experiments on the following datasets:

- **MS MARCO**: A real-world large-scale QA dataset.
- **BEIR Benchmark**: A suite of information retrieval datasets spanning multiple domains and tasks.

Instructions for downloading and preprocessing the datasets are included in the notebooks where applicable.
