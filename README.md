# open-hub: AI for Under-Resourced Languages

This repository serves as an index and documentation center for our open-source initiative dedicated to developing Artificial Intelligence and Natural Language Processing (NLP) tools for under-preserved languages.

Our mission is to bridge the digital divide by building robust speech and text technologies from dataset creation to state-of-the-art model training and educational tools.

---

## 📂 Project Structure & Repositories

Our work is modularized into several main repositories, covering the entire pipeline of AI development:

| Category | Repository | Description |
| :--- | :--- | :--- |
| **Data Prep** | [**Segmentation**](https://github.com/cawoylel/Segmentation) | Audio preprocessing, Voice Activity Detection (VAD), and segmentation. |
| **Data Prep** | [**FulaSpeechCorpora**](https://github.com/cawoylel/FulaSpeechCorpora) | Scripts and pipelines for building aligned speech corpora. |
| **Modeling** | [**windanam**](https://github.com/cawoylel/windanam) | Multi-dialectal Automatic Speech Recognition (ASR) models. |
| **Tutorials and Education** | [**nlp4all**](https://github.com/cawoylel/nlp4all) | Step-by-step guides, tutorials, and code to reproduce our work|
| **Synthetic Data Pipelie** | [**oolel-translator**](https://github.com/soynade-research/oolel-translator) | Batch inference pipeline for generating synthetic translation data at scale|

---

## Repository Details

### 1. Segmentation (Audio Preprocessing)
**🔗 Link:** [github.com/cawoylel/Segmentation](https://github.com/cawoylel/Segmentation)

Before training speech models, raw audio must be cleaned and segmented. This repository provides a two-step preprocessing pipeline designed to prepare high-quality audio data for ASR training.

*   **Core Function:** Splits long audio files into sentence-level segments and filters out non-speech audio (music, noise).
*   **Key Technologies:**
    *   **inaSpeechSegmenter:** For initial classification (Speech vs. Music vs. Noise) and gender detection.
    *   **Silero VAD:** For precise, enterprise-grade voice activity detection on longer segments.
*   **Use Case:** Use this tool to process raw radio broadcasts, podcasts, or recordings into clean `.wav` files ready for model training.

### 2. FulaSpeechCorpora (Dataset Creation)
**🔗 Link:** [github.com/cawoylel/FulaSpeechCorpora](https://github.com/cawoylel/FulaSpeechCorpora)

High-quality data is the bottleneck for under-resourced languages. This repository contains the specific scripts and methodology we used to create the **Fula Speech Corpora**.

*   **Core Function:** Automates the alignment of audio with text and manages the curation of speech datasets.
*   **Key Features:**
    *   Utilizes **MMS Aligner** (Massively Multilingual Speech) for forced alignment.
    *   Includes adaptation scripts to apply this process to other low-resource languages.
*   **Use Case:** Use this if you have raw audio and text and need to build a structured dataset for machine learning.

### 3. windanam (ASR Models)
**🔗 Link:** [github.com/cawoylel/windanam](https://github.com/cawoylel/windanam)

This is the core repository containing our work on Automatic Speech Recognition (ASR) for Fula language.

*   **Core Function:** Training and fine-tuning speech-to-text models.
*   **Key Technologies:** Built on top of **Fairseq**.
*   **Key Features:**
    *   **Multi-dialectal Support:** Models designed to recognize different varieties of Fula.
    *   Training recipes and inference scripts.
*   **Use Case:** Researchers and developers looking to deploy Fula speech recognition or fine-tune models on their own dialect data.

### 4. nlp4all (Education & Tutorials)
**🔗 Link:** [github.com/cawoylel/nlp4all](https://github.com/cawoylel/nlp4all)

We believe in democratizing access to AI. This repository is an implementation of our "NLP for All" concept which consists in openly sharing our journey and the methodologies behind building AI technologies for underpresented languages with step by step tutorials and guidelines.

*   **Core Function:** Offer readily usable templates that other communities can leverage to develop similar technologies for their languages.

### 5. oolel-translator (LLMs)
**🔗 Link:** [github.com/cawoylel/nlp4all](https://github.com/soynade-research/oolel-translator)

Oolel-Translator is a batch inference pipeline for generating synthetic translation data at scale. Point it at a Hugging Face dataset, pick your model, and it produces parallel text - thousands, if not millions, of rows.

*   **Core Function:**

- Runs on vLLM with a PyTorch fallback
- Reads JSONL, JSON, or CSV inputs
- Pulls datasets from the Hub and pushes outputs back automatically
- Multi-GPU sharding and configurable memory utilization built in

You can use it to build translation pairs for any language pair and fine-tune models on the output, or expand an existing dataset.

---

## Contributing

We welcome contributions from developers, linguists, and native speakers! Whether you notice a bug in a script or an improvement in a given documentation, your help is vital.

## 📄 License

Unless otherwise noted in the specific repository, our work is open-source. Please check the individual repositories for specific license details (typically MIT or Apache 2.0).
