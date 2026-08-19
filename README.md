# Semantic Similarity Analysis of the Mahabharata and the Iliad

## Overview

This project applies Natural Language Processing (NLP) and transformer-based semantic analysis to compare narrative structures, characters, and thematic similarities between two major epic traditions: the *Mahabharata* and the *Iliad*.

The system combines named entity recognition, transformer-based summarization, sentence embeddings, cosine similarity, cross-epic chapter retrieval, and character co-occurrence networks.

## Objectives

- Analyze large-scale epic narratives using NLP techniques
- Identify and visualize important characters and their relationships
- Generate automated chapter summaries using transformer models
- Represent chapters using semantic sentence embeddings
- Identify similar chapters within each epic
- Discover semantically related chapters across the *Mahabharata* and the *Iliad*
- Compare narrative similarity using quantitative metrics and visualizations

## Methodology

The project follows the pipeline:

Text Collection  
↓  
Chapter Segmentation  
↓  
Named Entity Recognition  
↓  
Character Extraction  
↓  
Transformer-based Summarization  
↓  
Sentence Embeddings  
↓  
Cosine Similarity  
↓  
Intra-Epic Similarity  
↓  
Cross-Epic Similarity  
↓  
Character Co-occurrence Networks  
↓  
Evaluation and Visualization

## Technologies Used

- Python
- spaCy
- Hugging Face Transformers
- Sentence Transformers
- PyTorch
- NetworkX
- PyVis
- Matplotlib
- Seaborn
- Gradio
- Pandas
- NumPy
- Scikit-learn

## Models

### Named Entity Recognition

spaCy `en_core_web_sm` is used to identify named entities, particularly:

- PERSON
- GPE

### Text Summarization

The project uses:

`sshleifer/distilbart-cnn-12-6`

for transformer-based chapter summarization.

### Semantic Embeddings

Chapter representations are generated using:

`all-MiniLM-L6-v2`

Cosine similarity is then used to identify semantically similar chapters.

## Analysis

The system supports three major forms of comparison:

### Intra-Epic Similarity

Identifies chapters with similar semantic representations within the same epic.

### Cross-Epic Similarity

Maps chapters from the *Mahabharata* to semantically similar chapters in the *Iliad*, and vice versa.

### Character Network Analysis

Character co-occurrence networks are constructed using named entities detected across chapters.

Network centrality measures are used to examine the structural importance of characters within the narrative.

## Evaluation

The project includes:

- ROUGE-1
- ROUGE-2
- ROUGE-L
- Cosine similarity analysis
- Similarity distributions
- Character network analysis
- Comparative visualizations

## Interactive Demo

A Gradio-based interface allows users to:

1. Select an epic
2. Enter a chapter number
3. Generate a chapter summary
4. Retrieve similar chapters within the epic
5. Retrieve semantically similar chapters from the other epic

## Repository Structure

```text
mahabharata-iliad-nlp/
│
├── epic_nlp_analysis.ipynb
├── README.md
├── requirements.txt
└── .gitignore
