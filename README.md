# Masters Thesis: A Graph RAG Benchmark Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Python 3.10 | 3.12](https://img.shields.io/badge/python-3.10%20%7C%203.12-blue)
![Status: Completed](https://img.shields.io/badge/Status-Thesis_Completed-green)

This repository serves as the **Research Compendium** for the Master's Thesis: **"A Graph RAG Benchmark Analysis"** (2024-2025).

It contains the source code, experimental setup, and datasets used to conduct a rigorous "apples-to-apples" comparison of state-of-the-art Graph Retrieval-Augmented Generation (RAG) frameworks against Naive RAG baselines.

## 🎓 Academic Context
* **Author:** Nila Akbari
* **Supervisor:** Prof. Nicolò Navarin
* **Co-Supervisor:** Dr. Davide Rigoni
* **Institution:** University of Padova, Department of Mathematics "Tullio Levi-Civita"
* **Degree:** Master of Science in Computer Science

## 📖 Project Overview

The "Knowledge-Locked" nature of Large Language Models (LLMs) necessitates external retrieval. [cite_start]However, standard **Naive RAG** often fails on complex, relational data[cite: 26]. This thesis benchmarks emerging **Graph RAG** paradigms that transform unstructured text into structured Knowledge Graphs.

**Frameworks Benchmarked:**
1.  [cite_start]**From Local to Global (GraphRAG):** Microsoft's community-detection approach[cite: 89].
2.  [cite_start]**LightRAG:** A dual-level (local/global) efficient retrieval framework[cite: 91].
3.  [cite_start]**StructRAG:** A dynamic, structure-aware framework for heterogeneous data[cite: 90].
4.  [cite_start]**Naive RAG:** Standard vector-similarity retrieval (Baseline)[cite: 26].
5.  [cite_start]**Simple LLM:** No retrieval (Baseline)[cite: 31].

**Datasets:**
* **UltraDomainCS:** Technical computer science documentation (Logical/Hierarchical).
* **NarrativeQA:** Long-form literary narratives (Temporal/Character-based).

## 📂 Repository Structure (Monorepo)

This repository is organized as a monorepo containing isolated environments for each framework to handle conflicting dependencies.

```text
MastersThesis-AGraphRAGBenchmark/
├── data/                             # Evaluation Datasets
│   ├── UltraDomainCS/
│   └── NarrativeQA/
├── evaluation/                       # Evaluation Scripts (LLM-as-a-Judge)
├── frameworks/                       # Core Implementations
│   ├── GraphRAG/                # [Env B] Microsoft GraphRAG (Python 3.10)
│   ├── LightRAG/                # [Env A] LightRAG Implementation
│   ├── StructRAG/               # [Env A] StructRAG Implementation
│   ├── Base-RAG/               # [Env A] StructRAG Implementation
│   └── SimpleLLM/               # [Env A] Naive RAG Baseline
└── README.md
