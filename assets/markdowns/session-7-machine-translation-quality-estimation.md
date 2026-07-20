## Session 7: Machine Translation Quality Estimation in Low-Resource Scenarios

**Facilitators:** Dr Tharindu Ranasinghe and Damith Dola Mullage  
**Repository:** [UCREL/Session-7-Machine-Translation-Quality-Estimation](https://github.com/UCREL/Session-7-Machine-Translation-Quality-Estimation)  
**Notebook:** [Open the practical notebook in Google Colab](https://colab.research.google.com/github/UCREL/Session-7-Machine-Translation-Quality-Estimation/blob/main/MT_and_QE_Practical_Session_UCREL.ipynb)

This session explores the full life cycle of a machine translation output: producing a translation, evaluating it against a human reference, and estimating its quality when no reference translation is available.

The practical uses deliberately challenging **Spanish–English** examples, including idioms and lexical ambiguities, to demonstrate why fluent machine-generated text is not necessarily accurate. Participants compare open multilingual translation systems, examine the strengths and weaknesses of standard evaluation metrics, and experiment with modern reference-free quality estimation methods.

### What the notebook covers

The notebook guides participants through three connected stages:

1. **Machine translation**
   - translating Spanish source sentences into English;
   - working with the multilingual **M2M100** and **NLLB** models;
   - comparing system outputs on straightforward and deliberately difficult examples; and
   - identifying errors involving idioms, ambiguity and meaning preservation.

2. **Reference-based evaluation**
   - comparing machine translations with human reference translations;
   - computing the classic **BLEU** metric;
   - using **BERTScore** for semantic similarity;
   - examining cases where automatic scores agree or disagree with human judgement; and
   - understanding the limitations of reference-based evaluation.

3. **Reference-free quality estimation**
   - estimating translation quality using only the source sentence and machine-translated output;
   - applying **COMET-Kiwi** as a learned quality-estimation model;
   - exploring **GEMBA-MQM**, an LLM-as-judge approach inspired by the Multidimensional Quality Metrics framework;
   - identifying and categorising translation errors; and
   - comparing metric scores with qualitative error analysis.

### Learning outcomes

By the end of the session, participants should be able to:

- explain the difference between machine translation evaluation and quality estimation;
- run multilingual neural machine translation models on new text;
- assess translations using BLEU and BERTScore;
- use reference-free quality-estimation methods such as COMET-Kiwi;
- interpret LLM-based translation judgements and error categories;
- recognise why high fluency can conceal serious translation errors;
- compare metric-based and human-centred approaches to translation quality; and
- understand the importance of translation literacy in high-stakes and low-resource settings.

### Main technologies and resources

The practical draws on:

- `transformers` for running multilingual translation models;
- **M2M100** and **NLLB** for Spanish-to-English translation;
- **BLEU** for lexical, reference-based evaluation;
- **BERTScore** for semantic, reference-based evaluation;
- **COMET-Kiwi** for reference-free translation quality estimation; and
- **GEMBA-MQM** for LLM-assisted error identification and quality assessment.

### Why this matters

Machine translation has progressed from rule-based systems to neural models and large language models, but increased fluency has not removed the risk of confident, difficult-to-detect errors. This is especially important in legal, medical, public-service and low-resource-language contexts, where mistranslation can have serious consequences.

The session therefore emphasises that the future is not translation without humans, but translation supported by better evaluation instruments and users who understand how to interpret them.

### Running the practical

The notebook is designed for Google Colab. A GPU runtime is recommended because the practical loads multiple multilingual models:

`Runtime → Change runtime type → T4 GPU`

Participants should expect model downloads to take some time during the first run.
