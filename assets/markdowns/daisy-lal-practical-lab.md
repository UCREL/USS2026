# Practical Lab: Text Classification and Sequence Labelling for Cancer Narratives

**Facilitator:** Daisy Lal

This practical session introduces two approaches for extracting structured information from unstructured cancer patient and caregiver narratives. Participants will work with large language models for multi-label text classification and with a sequence labelling model for clinical named entity recognition.

## 1. Multi-label Text Classification

[Open the Text Classification Notebook in Google Colab](https://colab.research.google.com/drive/1orHPPUeQvAfkBQgvDeDe6iHGYPqtOWQr?usp=sharing)

The text classification task is formulated as a **multi-label classification problem**. Prompt engineering is used with large language models to identify multiple, potentially overlapping themes in unstructured narratives written by cancer patients and caregivers.

This notebook demonstrates how LLM-based classification can support the analysis of narratives in which several themes may occur within the same document.

## 2. Sequence Labelling and Named Entity Recognition

[Open the Sequence Labelling Notebook in Google Colab](https://colab.research.google.com/drive/16IwfXaKsr5m4TFIvSvrNbw7KBlXzOvlb?usp=sharing)

The sequence labelling task is formulated as a **Named Entity Recognition (NER) problem**. LENS is used to identify and tag clinically relevant entities in unstructured skin cancer narratives.

The model assigns one of **24 predefined labels** to relevant text spans, enabling the structured extraction of information such as:

- symptoms
- treatments
- investigations

The extracted entities can subsequently be linked to biomedical terminologies such as **SNOMED CT**, including through clinical concept annotation tools such as **MedCAT**.