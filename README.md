# DeRAG: Black-box Adversarial Attacks on Retrieval-Augmented
 Generation Applications via Prompt Injection

## Abstract

Adversarial prompt attacks can significantly alter the reliability of Retrieval-Augmented Generation (RAG) systems by re-ranking them to produce incorrect outputs. In this work, we present a novel method that applies Differential Evolution (DE) to optimize adversarial prompt suffixes for RAG-based question answering.

Our approach is gradient-free, treating the RAG pipeline as a black box and evolving a population of candidate suffixes to maximize the retrieval rank of a targeted incorrect document. We demonstrate that DE can achieve high attack success rates without requiring access to model gradients. Experiments are conducted on the BEIR QA datasets and the MS MARCO dataset, evaluating attack success at various retrieval rank thresholds under multiple applications. Results show that DE-based prompt optimization attains competitive, and in some cases higher, success rates compared to gradient-based methods such as GGPP, while using only a small number of tokens (≤ 5) in the adversarial suffix.

These findings suggest that differential evolution offers a promising and effective alternative for prompt-based adversarial attacks on RAG systems, contributing to the broader goal of evaluating and improving the robustness of retrieval-augmented large language models.

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
