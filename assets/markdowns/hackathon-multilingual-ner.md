# Hackathon Challenge: Multilingual Named Entity Recognition

## Overview

This hackathon focuses on **multilingual Named Entity Recognition (NER)** using data from the [Universal NER](https://www.universalner.org/) project.

Participants will develop and evaluate an NER system on three disclosed languages and then test its ability to generalise to a fourth, previously unseen language.

## Task

Participants should train, adapt or prompt an NLP model to identify named entities in multilingual text.

Any reasonable modelling approach may be used, including:

- supervised model training;
- fine-tuning an existing multilingual model;
- few-shot or zero-shot prompting with a large language model;
- synthetic-data augmentation; or
- a combination of these approaches.

## Languages and datasets

| Role | Language | Dataset | Data availability |
|---|---|---|---|
| Disclosed | English | [UNER English-EWT](https://github.com/UniversalNER/UNER_English-EWT) | Train, development and test splits |
| Disclosed | Danish | [UNER Danish-DDT](https://github.com/UniversalNER/UNER_Danish-DDT) | Train, development and test splits |
| Disclosed | Simplified Chinese | [UNER Chinese-GSDSIMP](https://github.com/UniversalNER/UNER_Chinese-GSDSIMP) | Train, development and test splits |
| Surprise | Japanese | [UNER Japanese-PUD](https://github.com/UniversalNER/UNER_Japanese-PUD) | Test data only |

The English, Danish and Simplified Chinese datasets may be used for model development and evaluation. Japanese is the **surprise language** and is intended to assess cross-lingual generalisation.

## Evaluation categories

Three awards are proposed:

1. **Best overall performance** across the three disclosed languages.
2. **Best performance on the surprise language**, Japanese.
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
- The Japanese dataset contains test data only and should not be treated as a standard supervised training set.

## Details still to be confirmed

The following should be announced before the hackathon begins:

- the official evaluation metric;
- the required prediction format;
- submission instructions and deadline;
- whether external training data are permitted;
- whether use of proprietary APIs is allowed; and
- how ties will be resolved.
