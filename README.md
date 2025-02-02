# <img src="https://lilinwang.github.io/image/tigerLabLogo.png" height="24px" style="padding-top:4px"/>TigerLab - Open Source LLM Toolkit
<br/>
<div align="center">
    <img src="https://lilinwang.github.io/image/TigerLab.png" width="80%"  style="padding: 40px"/>
</div>
<br/>
<p align="center">
  🐅🚀<em>Framework for Trustworthy LLM development: RAG + FineTune + AI Safety Measurement</em>🚀🐅
</p>
<div align="center">
    <a href="https://discord.gg/GnwH2STv">
    <img src="https://img.shields.io/badge/discord-join%20chat-blue.svg?style=for-the-badge" alt="Join our Discord" height="20">
    </a>
    <a href="https://twitter.com/TigerLabAI">
    <img alt="Twitter Follow" src="https://img.shields.io/twitter/follow/TigerLabAI?style=for-the-badge" height="20">
    <a href="https://github.com/tigerlab-ai/tiger">
    <img alt="GitHub" src="https://img.shields.io/github/stars/tigerlab-ai/tiger?style=for-the-badge&color=gold" height="20">
    </a>
    <a href="https://github.com/tigerlab-ai/tiger/commits/main">
    <img alt="GitHub" src="https://img.shields.io/github/last-commit/tigerlab-ai/tiger/main?style=for-the-badge" height="20">
    </a>
    <a href="https://github.com/tigerlab-ai/tiger/blob/main/README.md" target="_blank">
    <img src="https://img.shields.io/static/v1?label=license&message=Apache License 2.0&color=green&style=for-the-badge" alt="License" height="20">
    </a>
</div>

## 🙌 AI Safety Report

**Request Safety Evaluation for your LLMs & Chatbots at ⭐ [TigerLab.ai](https://www.tigerlab.ai/) ⭐**

Details can be found at: [Metrics Defination](TigerArmor/#rating-guideline)

[<img width="1439" alt="TigerLab AI Safety Report" src="https://github.com/tigerlab-ai/tiger/assets/3810505/a20d6e9a-47b2-43e5-a501-92717e1650e1">](https://airtable.com/app8zluNDCNogk4Ld/shrYRW3r0gL4DgMuW/tblpLubmd8cFsbmp5)




## ✨ Demo
Find more demos at [TigerLab.ai](https://www.tigerlab.ai/)

### Demo 1 - Enhanced Retrieval Capabilities w/ EBR, RAG and GAR
[Demo 1 - Youtube](https://youtu.be/gi8P1i0hm70)

https://github.com/tigerlab-ai/tiger/assets/4805931/e7c35117-269a-437d-99ab-10407a901cc5

### Demo 2 - Fine-tuning Llama2 and DistilBERT
[Demo 2 - Youtube](https://youtu.be/0v0Qe-cbvRs)

https://github.com/tigerlab-ai/tiger/assets/148816206/4835b876-77e2-4483-9773-ea0b1d625f6c



## 🔬 Tech stack
<img width="2046" alt="Untitled-2" src="https://github.com/tigerlab-ai/tiger/assets/148816206/6616f960-1dc0-4e70-b44e-b34e20730152">

- **TigerRAG**: Use embeddings-based retrieval (EBR), retrieval-augmented generation (RAG), and generation-augmented retrieval (GAR) to fulfill queries. The demo used `BERT` for embedding, `FAISS` for indexing, `text-davinci-003` for generation.
- **TigerTune**: Python SDK to fine-tune, make inference, and evaluate Text Generation models and Text Classification models. The notebook demo fine-tuned `Llama2` and `DistilBERT`.
- **TigerDA**: Data Augmentation Toolkit. The generation-based augmenter supports data augmentation with fine-tuned (instruction-based) `GPT2`. `Top-k and Top-p Sampling` has been used for decoding. Perturbation-based augmenter coming soon!
- **TigerArmor** AI safety Toolkit. It contains metrics, datasets, evaluation tools for measure AI safety for LLMs, like Llama 2, GPT-4, Mistral, etc.

## 👨‍🚀 Prerequisites

Before you begin setting up this project, please ensure you have completed the following tasks:

### 0. Setup Tutorial

- [Tutorial - YouTuBe](https://youtu.be/fztXswkYz7c)

### 1. LLM -  OpenAI API Token
<details><summary>👇click me</summary>
This application utilizes the OpenAI API to access its powerful language model capabilities. In order to use the OpenAI API, you will need to obtain an API token.

To get your OpenAI API token, follow these steps:

1. Go to the [OpenAI website](https://beta.openai.com/signup/) and sign up for an account if you haven't already.
2. Once you're logged in, navigate to the [API keys page](https://beta.openai.com/account/api-keys).
3. Generate a new API key by clicking on the "Create API Key" button.
4. Copy the API key and store it safely.
5. Add the API key to your environment variable, e.g. `export OPENAI_API_KEY=<your API key>`

</details>

## 💿 Installation
- **Step 1**. Clone the repo
   ```sh
   git clone https://github.com/tigerlab-ai/tiger.git
    ```
- **Step 2**. Install TigerRAG
    - Install all Python requirements
      
    ```sh
    cd tiger/TigerRAG
    pip install .
    ```
    Demo:
    ```
    cd demos/movie_recs
    python demo_ebr.py
    python demo_rag.py
    python demo_gar.py
    ```
- **Step 3**. Install TigerTune
    - Install all Python requirements
    ```sh
    cd tiger/TigerTune
    pip install --upgrade -e .
    ```
    Demo:
    ```
    python examples/classification_example.py 
    python examples/generation_example.py 
    ```
    CUDA GPU is needed to run generation_example.py. If you don't have a CUDA GPU connected, you can leverage our notebooks in [notebooks/](TigerTune/notebooks/).

- **Step 4**. Install TigerDA
    - Install all Python requirements
    ```sh
    cd tiger/TigerDA
    pip install --upgrade -e .
    ```
    Demo:
    ```
    python examples/text_generation_augmenter_example.py 
    ```


## 📍 Roadmap
- [x] Launch v0.0.1
- [x] Release TigerDA
- [x] Release TigerArmor
- [ ] Add additional model support in TigerTune
- [ ] Add perturbation-based augmenters in TigerDA
- [ ] Release GPT Text Completion Models comparisions
- [ ] TigerLab Safety dataset crowd sourcing program
- [ ] TigerLab AI Safety Leaderboard for LLMs
- [ ] TigerLab Leaderboard for dataset contributors
- [ ] VectorDB for TigerRAG
- [ ] WebApp

## 🫶 Contribute to TigerLab
Please check out our [Contribution Guide](CONTRIBUTING.md)!

For bug fixes and feature requests, please file a Github issue.

In addition to the mentioned roadmap, we also maintain a backlog at https://github.com/tigerlab-ai/tiger/issues.

## 💪 Contributors
<a href="https://github.com/tigerlab-ai/tiger/graphs/contributors">
  <img src="https://contrib.rocks/image?repo=tigerlab-ai/tiger" />
</a>

## 🎲 Community
- Join us on [Discord](https://discord.gg/GnwH2STv)

## 📝 Citation
```
@misc{TigerLabAI_2023,
  title={TigerLab AI Repository},
  author={TigerLab AI},
  howpublished={GitHub. Available online: https://github.com/tigerlab-ai/tiger},
  year={2023}
}
```

A significant gap has arisen between general Large Language Models (LLMs) and the data stores that provide them with contextual information. Bridging this gap is a crucial step towards grounding AI systems in factual and safety domains, where their value lies not only in their generality but also in their specificity and uniqueness.

In pursuit of this goal, we are thrilled to introduce the Tiger toolkit (TigerRAG, TigerTune, TigerDA, TigerArmor) as an open-source resource for developers to create trustworthy AI models and language applications tailored to their specific needs.

We believe that our efforts will play a pivotal role in shaping the next phase of language modeling. This phase involves organizations customizing AI systems to align with their unique intellectual property and safety requirements, ushering in a new era of AI precision and safety.
