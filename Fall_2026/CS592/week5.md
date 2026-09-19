# SomAtt: A Foundation Model for the Tumor Genome

David Arredondo, University of New Mexico Health Sciences Center

SomAtt: somatic attention

## Questions

1. How are they turning genes into vectors? Is it really as simple as 
   GATC -> 0, 1, 2, 3?

## Goal

- Risk StratificaitonHow high of a risk given some sample?
- Drug Response Prediction: how susceptible to certain drugs?

## Somatic Mutations

- Occur randomly during lifetime

## Types of Mutations/Alterations

1. Sequence Variants: a sequence gets altered (akin to bit flip)
2. Broad Copy Number Alteration
3. Focol Copy Number Amplification: Can copy a protein encoded by a gene 
    - Makes gene more active

## Cancer = Synergistic Gene ALterations

## Precision Oncology

- BRaf protein: responsible for cell replication
- BRAFp.V600E: turns BRaf constantly on -> constant cell replication

## Precision Oncology = Single-Biomarker Lookup

- Certain mutations are more responsive to certain drugs
- Goal: characterize the patient:
    - What is the exact mutation that has a five percent response?

## Data + Model Architechture

### Goal

- Transformers are good at modeling context, handling variable length input 
  sequences, and sparse data -> lends itself to gene processing
  
### Transformer-based Language Models

- Transformer takes input embedding vectors and turn them into contextualized 
  embedding vectors

### SomAtt: A Tumor Language Model

- Predict cancer type based on some set of mutations
- 
