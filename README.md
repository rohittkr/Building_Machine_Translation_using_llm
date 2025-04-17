# 🌐 Building Machine Translation using LLM (English to Hindi)

This project demonstrates how to build a machine translation system using pre-trained Large Language Models (LLMs). Specifically, we use the [Helsinki-NLP/opus-mt-en-hi](https://huggingface.co/Helsinki-NLP/opus-mt-en-hi) model to translate English sentences to Hindi using Hugging Face's `transformers`, TensorFlow, and the IITB English-Hindi dataset.

---

## 📌 Table of Contents

- [Overview](#overview)
- [Dataset](#dataset)
- [Model](#model)
- [Installation](#installation)
- [How to Run](#how-to-run)
- [Training Details](#training-details)
- [Few-Shot Fine-Tuning](#few-shot-fine-tuning)
- [Zero-Shot Inference](#zero-shot-inference)
- [LoRA Fine-Tuning](#lora-fine-tuning)
- [Translation Inference](#translation-inference)
- [Results](#results)
- [References](#references)

---
---

## 🔗 Google Colab Links

You can open and run the complete notebooks on Google Colab using the links below:

- 🚀 **English to Hindi Translation (Full Training & Inference)**  
  [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1lFLhJqSDZU0SJ0NnZ-EjXCkRV1YmJiVF?usp=sharing)

- ⚙️ **LoRA Fine-Tuning Notebook**  
  [![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1At45am6mjqDRfk7W5RLq7TmulyJI65xA?usp=sharing)

> Make sure you're logged into a Google account with Colab access. If you see a “permission denied” error, request access to the notebook via the share button in Colab.

---


## 📖 Overview

Machine translation is one of the core applications of natural language processing. In this project, we:

- Load and explore the **IITB English-Hindi parallel corpus**.
- Preprocess and tokenize the data using Hugging Face's tokenizer.
- Train and fine-tune the **Helsinki-NLP English-to-Hindi translation model**.
- Perform zero-shot and few-shot translation.
- Apply **LoRA** (Low-Rank Adaptation) for efficient fine-tuning.
- Save and reload the trained model for future inference.

---

## 📂 Dataset

We use the [cfilt/iitb-english-hindi](https://huggingface.co/datasets/cfilt/iitb-english-hindi) dataset available via Hugging Face `datasets`.

- Contains aligned sentence pairs in English and Hindi.
- Split into `train`, `test`, and `validation`.

---

## 🤖 Model

We use the following pre-trained model for translation:

- **Model**: `Helsinki-NLP/opus-mt-en-hi`
- **Type**: Sequence-to-Sequence (Encoder-Decoder)
- **Framework**: TensorFlow (TF)

---

## ⚙️ Installation

Install the necessary dependencies:

```bash
pip install tensorflow transformers datasets sentencepiece sacrebleu peft accelerate
