# Hackathon Challenge: Multilingual Named Entity Recognition

## Overview

This hackathon focuses on **multilingual Named Entity Recognition (NER)** using data from the [Universal NER](https://www.universalner.org/) project.

Participants will develop and evaluate an NER system on three disclosed languages and then test its ability to generalise to a fourth, previously unseen language.

## Task

Participants should train, adapt or prompt an NLP model to identify named entities in multilingual text.

Any reasonable modelling approach may be used, including:

- supervised model training;
- fine-tuning an existing multilingual model;
- Training with or without synthetic-data augmentation;
- few-shot or zero-shot prompting with a large language model;
- a combination of these approaches.

## Languages and datasets

| Role | Language | Dataset | Data availability |
|---|---|---|---|
| Disclosed | English | [UNER English-EWT](https://github.com/UniversalNER/UNER_English-EWT) | Train, development and test splits |
| Disclosed | Danish | [UNER Danish-DDT](https://github.com/UniversalNER/UNER_Danish-DDT) | Train, development and test splits |
| Disclosed | Simplified Chinese | [UNER Chinese-GSDSIMP](https://github.com/UniversalNER/UNER_Chinese-GSDSIMP) | Train, development and test splits |
| Surprise | Surprise | Surprise | Test data only |

The English, Danish and Simplified Chinese datasets may be used for model development and evaluation. The **surprise** language tests your model to generlize to an unseen language.

## Evaluation categories

Three awards are proposed:

1. **Best overall performance** across the three disclosed languages.
2. **Best performance on the surprise language**.
3. **Most innovative solution**, recognising originality rather than predictive performance alone.

The innovation award may consider approaches such as:

- zero-shot or few-shot methods;
- synthetic training data;
- unconventional model combinations;
- efficient or resource-conscious methods; and
- particularly creative approaches to multilingual transfer.

## Important notes

- Participants are free to choose their modelling strategy.
- A highly innovative submission does not need to achieve the highest score.
- The surprise dataset contains test data only.

## CodaBench - Competition Link

We are using CodaBench to host and run this hackathon, of which the link to our CodaBench page that we are running this hackathon from is here: [https://www.codabench.org/competitions/17588/?secret_key=de718acd-a2df-4dc6-b486-65a9f227d698](https://www.codabench.org/competitions/17588/?secret_key=de718acd-a2df-4dc6-b486-65a9f227d698)

The CodaBench page covers the following:

- Training, development, and test data release.
- Scoring submissions using the F1 score.
- Leadboard showing the performance of current submissions.
