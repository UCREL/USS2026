# LLM Prompting Techniques: RTCF, Few-shot, CoT, RAG and Constraints

**Tutorial team:** Chenji Jin, Pourya Farzi, and Dr Scott Piao
**Contact:** `{p.jin, p.farzi, s.piao}@lancaster.ac.uk`

---

## Contents

- [Introduction](#introduction)
- [Structure of the Tutorial](#structure-of-the-tutorial)
  - [Part 1: Techniques](#part-1--techniques--4045-minutes)
  - [Part 2: Hands-on Practice](#part-2--hands-on-practice)
- [Software, Sample Data, and Computing Environment](#software-sample-data-and-computing-environment)
  - [Prerequisites](#prerequisites)
- [Data Privacy and Security](#data-privacy-and-security)
- [Takeaways](#takeaways)
- [Guideline: How to Get an OpenRouter API Key](#guideline-how-to-get-an-openrouter-api-key)
  - [Step 1: Create an Account](#step-1--create-an-openrouter-account)
  - [Step 2: Open the API Keys Page](#step-2--open-the-api-keys-page)
  - [Step 3: Configure the API Key](#step-3--configure-the-api-key)
  - [Step 4: Copy the API Key](#step-4--copy-the-api-key)
  - [Step 5: Use the API Key in Python](#step-5--use-the-api-key-in-python)
  - [Step 6: Using Free Models](#step-6--using-free-models)

---

## Introduction
[Slides](/assets/presentations/SummerSchool_Version20July.pdf)
With the emergence of ChatGPT in November 2022, generative AI has advanced at an unprecedented pace, and a series of Large Language Models (LLMs) have been developed and increasingly deployed across a growing range of real-world applications. The knowledge embedded within today's LLMs opens up extensive possibilities for solving a wide variety of problems.

While there are many ways to access LLMs and retrieve the knowledge stored within them, **prompting** remains the principal means for most users to access and use LLMs quickly and conveniently. These approaches range from simple question answering to more advanced techniques such as Chain-of-Thought (CoT) prompting and Retrieval-Augmented Generation (RAG).

When addressing highly complex tasks, advanced prompting techniques become necessary to obtain accurate, high-quality outputs while mitigating issues such as hallucination and bias. Understanding and mastering a range of prompting techniques is, therefore, critical to applying LLMs effectively.

In this tutorial, you will discuss a range of LLM prompting techniques and gain first-hand experience by applying selected techniques to specific tasks. A freely available LLM is used for testing, with sample data provided by the team or your own data. Practical guidance is also given on connecting to an LLM API and querying models with your own prompts in Python.

---

## Structure of the Tutorial

The Dataset and the Google Colab notebooks for this tutorial are available [here](/assets/notebooks/Prompt%20Engineering/).

The tutorial has **two main parts**.

### Part 1: Techniques (≈ 40–45 minutes)

A presentation of the main LLM prompting techniques in wide use today, giving insight into how different prompt types are structured and the rationale behind those structures and coding designs. The techniques covered are:

- **RTCF Framework**
  - **R**ole: Who is the LLM expected to act as?
  - **T**ask: What specific objective should the LLM accomplish?
  - **C**ontext: What information helps the LLM interpret the task and produce an appropriate response?
  - **F**ormat: How should the LLM respond?
- **Few-shot Prompting** — Beyond specifying the task, provide illustrative examples to guide the response.
- **Constraints**: Constrain and standardise the content and format of outputs so downstream tasks can use them more easily.
- **Chain-of-Thought (CoT) Prompting**: For harder tasks, guide the LLM to reason step by step.
- **RAG (Retrieval-Augmented Generation)**: Provide external knowledge to ground responses, improving accuracy and reducing hallucinations.

### Part 2: Hands-on Practice

You develop and apply your own prompts with the team's help, using either the provided
sample data or your own data and an LLM of your choice. Two practice scenarios are
provided:

1. **Attribute extraction**: Given an input text describing an entity (e.g. a city or commercial item), extract all of its attributes (e.g. a city's population, location, and other features).
2. **Aspect-based sentiment analysis**: Given a text containing comments on an entity (e.g. a mobile phone or car), extract sentiment about its different aspects (e.g. the colour is appealing; the size is too small; the sound quality is poor).

> ⚠️ **Privacy:** Avoid using any data containing personal or private information during
> practice — privacy cannot be guaranteed when accessing LLMs through external APIs.

---

## Software, Sample Data, and Computing Environment

Participants should have good knowledge and some experience of **Python**, which is the language used throughout.

- **Software:** A sample Python script is provided, which participants can modify or
  adapt for their own tasks in the hands-on session.

- **Environment:** The script is set up to run in **Google Colab** (<https://colab.google>) via [Jupyter notebooks](/assets/notebooks/Prompt%20Engineering/). Programs and the sample dataset can be downloaded to run locally.

- **Sample Dataset:** The [Yelp Restaurant Review Dataset](https://www.kaggle.com/datasets/farukalam/yelp-restaurant-reviews),
  an open-source set of Yelp restaurant reviews.


### Prerequisites

- A **Gmail account** (for accessing Colab and applying for an API key via OpenRouter), plus basic skills in using Colab and Jupyter notebooks.
- An **OpenRouter API key**, obtained in advance (see the guide below).

---

## Data Privacy and Security

An open-source dataset is provided for practice. If you wish to use your own data, ensure it contains **no personal or private information**, as it will be uploaded to Google Cloud and processed via LLM APIs. To process private or sensitive data, download and run an LLM **locally** instead.

---

## Takeaways

On completion, you will have knowledge and hands-on experience in designing and using a range of LLM prompting techniques to solve problems, such as extracting key information and aspect-based sentiment from input texts. These are transferable skills applicable to a wide range of research and practical tasks.

---
---

# Guideline: How to Get an OpenRouter API Key

*For the tutorial "LLM Prompting Techniques"*
**Contact:** `{p.farzi, p.jin, s.piao}@lancaster.ac.uk`

This guide briefly explains how to create an API key from OpenRouter for use in Python
projects and LLM experiments.

### Step 1: Create an OpenRouter Account

1. Go to the [OpenRouter website](https://openrouter.ai).
2. Click **Sign Up**. You can register with Google, GitHub, or Email.
3. Tick the legal consent box and press **Continue**.

### Step 2: Open the API Keys Page

After logging in, go to the [API Keys page](https://openrouter.ai/settings/keys) and click
**"New Key"**.

### Step 3: Configure the API Key

You may optionally configure:

| Field | Recommendation |
|-------|----------------|
| Key name | Something descriptive, e.g. `ChatBot Key` |
| Credit limit | No need to fill |
| Expiration date | No expiration |

### Step 4: Copy the API Key

After creation, OpenRouter displays the key **once**. It looks like:

```
sk-or-v1-xxxxxxxxxxxxxxxx
```

Copy and save it securely.

> 🔒 **Important security note** — Never:
> - share your API key publicly,
> - upload it to GitHub, or
> - hardcode it in public notebooks.
>
> OpenRouter recommends storing keys in **environment variables** or **`.env` files**.

### Step 5 — Use the API Key in Python

Install the required library:

```bash
pip install openai
```

Example Python code:

```python
from openai import OpenAI

client = OpenAI(
    api_key="{YOUR_OPENROUTER_API_KEY}",
    base_url="https://openrouter.ai/api/v1"
)

response = client.chat.completions.create(
    model="meta-llama/llama-3.3-70b-instruct:free",
    messages=[
        {
            "role": "user",
            "content": "Explain what embeddings are."
        }
    ]
)

print(response.choices[0].message.content)
```

### Step 6 — Using Free Models

OpenRouter provides a rotating selection of **free** models. Their IDs end in the
`:free` suffix, and they are rate-limited (typically **20 requests/minute** and
**200 requests/day**). The exact catalogue changes over time — the current list is at
<https://openrouter.ai/models?max_price=0>.

A selection of free models available as of June 2026:

```python
model="meta-llama/llama-3.3-70b-instruct:free"   # solid general-purpose
model="qwen/qwen3-coder:free"                    # strong for coding (1M context)
model="openai/gpt-oss-120b:free"                 # OpenAI open-weight, tool use
model="openai/gpt-oss-20b:free"                  # lighter open-weight option
model="google/gemma-4-31b-it:free"               # multimodal (vision + tools)
model="nvidia/nemotron-3-super-120b-a12b:free"   # large, 1M context
model="z-ai/glm-4.5-air:free"
model="meta-llama/llama-3.2-3b-instruct:free"    # very lightweight
```

Or let OpenRouter pick one automatically:

```python
model="openrouter/free"   # auto-selects an available free model
```

> 💡 **Note:** Free tiers are subsidized and intended for experimentation and learning,
> not production workloads — availability and rate limits can change without notice.

### Useful Notes

OpenRouter provides:

- access to many LLMs through one API,
- OpenAI-compatible APIs (works with the OpenAI SDK by changing the base URL),
- support for Qwen, DeepSeek, Llama, Gemini, Mistral, and many others.

> ℹ️ The model IDs in earlier drafts of this guide (e.g. `anthropic/claude-opus-4.8`,
> `openai/gpt-5.2`, `x-ai/grok-4.3`, `qwen/qwen3.5-plus-...`) are **paid** models or are
> not in the free catalogue, and will return errors if used as free models. The IDs above
> were verified against OpenRouter's free-model list in June 2026; always confirm the
> current `:free` IDs before the session.
