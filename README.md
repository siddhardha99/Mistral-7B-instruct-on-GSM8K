# 🧠 Fine-Tuning Mistral 7B on GSM8K with LoRA 

This project fine-tunes the [Mistral 7B Instruct](https://huggingface.co/mistralai/Mistral-7B-Instruct-v0.1) large language model on the Grade School Math 8K (GSM8K) dataset using the Low-Rank Adaptation (LoRA) technique. The pipeline is optimized for Kaggle's GPU environment and leverages `bitsandbytes` for efficient 4-bit quantization.

---

## 📚 Dataset

**GSM8K**: A high-quality dataset of 8,500+ grade school math word problems created by OpenAI.

- 📂 Train: `main_train.csv`
- 📂 Test: `main_test.csv`
- 🧠 Source: [`thedevastator/grade-school-math-8k-q-a`](https://www.kaggle.com/datasets/thedevastator/grade-school-math-8k-q-a)

---

## 🔧 Model and Setup

- 🧠 Model: `Mistral-7B-Instruct-v0.1` (via Hugging Face)
- ⚙️ Quantization: 4-bit (NF4) using `bitsandbytes`
- 🧩 Fine-Tuning: LoRA via HuggingFace PEFT
- 🛠 Environment: Kaggle Notebook + CUDA GPU
- 📦 Libraries: `transformers`, `datasets`, `peft`, `trl`, `bitsandbytes`

---

## 🏗️ Prompt Format

Training prompt format:
```text
<QUESTION> [SEP] <ANSWER> <eos>
