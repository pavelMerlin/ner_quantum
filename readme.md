# NER Model - Named Entity Recognition

## Overview
This NER (Named Entity Recognition) model identifies and labels named entities in text data. The model recognises entities such as mountain names. It performs well on text that describes landscape and nature.

The notebook performs three tasks at once: 
1) Generates data in the required format for solving the NER problem.
NER format. 
2) Processes this data by highlighting NER tags and tokenaiz sentences. 
3) Creates a BERT-based model for recognising mountain names in the text. 

## Features
- Recognition of mountain names.
- High accuracy in identifying mountains in unstructured text.

## Installation
### Requirements
- Python (version 3).
- Dependencies you can install below with command.

### Installation Steps
1. Install dependencies.
    ```bash
    pip install -r requirements.txt
    ```

## Dataset


## Usage
### Loading the Model
```python
from transformers import pipeline

# Load the NER pipeline
# ner_pipeline = pipeline("ner", model=model_path, tokenizer=tokenizer)
# =======OR========
ner_pipeline = pipeline("ner", model=model, tokenizer=tokenizer)

print(ner_pipeline(text, aggregation_strategy="max"))
```
## Examples
Model runtime examples:
```python
text = "In the heart of every mountain range lies a story \
      as ancient as time itself, inscribed within the very fabric of stone \
      and ice. These narratives weave tales of human endeavor, courage, and \
      the relentless pursuit of conquering the unconquerable. From the serene \
      and awe-inspiring Sierra Nevada to the rugged expanse of the Swiss Alps \
      these colossal peaks stand as testaments to human resilience and the enduring \
      power of nature. Their timeless grandeur bears witness to the indomitable spirit\
      of exploration that courses through humanity’s veins, a testament to our\
      unwavering quest for discovery amidst the vast and formidable landscapes of\
      this world."

'geo', 'score': 0.985183, 'word': 'sierra nevada', 'start': 279, 'end': 292,
'geo', 'score': 0.9863523, 'word': 'swiss alps', 'start': 322, 'end': 332
```