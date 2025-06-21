<!-- Hugging Face + Project Header -->
<p align="center">
  <img src="https://huggingface.co/front/assets/huggingface_logo-noborder.svg" width="120"/>
  <h1 align="center">Finance Assistant LLM with LoRA Adapter Fine-Tuning</h1>
  <p align="center">
    Fine-tuned <b>TinyLlama-1.1B-Chat</b> on the <i>Finance-Instruct-500k</i> dataset using efficient adapter-based training.
  </p>
</p>

---

## 🔧 Project Overview

This project demonstrates how to fine-tune a lightweight language model using [PEFT](https://github.com/huggingface/peft)'s **LoRA** (Low-Rank Adaptation) on financial instruction data.

- ✅ Efficient fine-tuning with LoRA adapters (only ~0.1% of weights trained)
- ✅ Uses [TinyLlama-1.1B-Chat](https://huggingface.co/TinyLlama/TinyLlama-1.1B-Chat-v1.0)
- ✅ Trained on finance domain instructions: definitions, comparisons, concepts
- ✅ Hugging Face ecosystem: `transformers`, `peft`, `datasets`

---

## 🧠 Model Architecture

- **Base model**: `TinyLlama-1.1B-Chat-v1.0`
- **Training method**: LoRA Adapter Training (`r=16`, `alpha=32`, `dropout=0.05`)
- **Target modules**: `q_proj`, `v_proj`
- **Precision**: FP16 (no quantization)

---

## 📦 Dataset

Dataset used:

- 📂 [Finance-Instruct-500k](https://huggingface.co/datasets/Josephgflowers/Finance-Instruct-500k)
- Instruction-based financial Q&A pairs

> Example:
```json
{
  "system": "You are a financial assistant.",
  "user": "What is the difference between stocks and bonds?",
  "assistant": "Stocks represent ownership in a company, while bonds are a form of debt."
}
```



## 📚 Citation

```bibtex
@dataset{josephgflowers2025financeinstruct,
  title={Finance-Instruct-500k},
  author={Joseph G. Flowers},
  year={2025},
  url={https://huggingface.co/datasets/Josephgflowers/Finance-Instruct-500k}
}
```
---

## 🧑‍💻 Author & Links

- 📖 Medium Blog: [How I Fine-Tuned TinyLlama with Finance-Instruct-500k](https://medium.com/@sharmaachintya49e)
- 🔗 LinkedIn: [Achintya Sharma](https://www.linkedin.com/in/achintyasharma47)

<p align="center">
  <img src="https://img.shields.io/badge/Made_with-LoRA-blue?style=flat-square">
  <img src="https://img.shields.io/badge/Platform-HuggingFace-orange?style=flat-square">
  <img src="https://img.shields.io/badge/Blog-Medium-black?style=flat-square&logo=medium">
</p>
