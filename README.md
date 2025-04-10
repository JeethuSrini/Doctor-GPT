# Doctor GPT 🧠💬
A domain-specific language model prototype for clinical text generation, built as a fine-tunable extension of GPT-2. The project explores how transformer-based architectures can be adapted to medical contexts through preprocessing, tokenization, and scalable training methods.

## 🚀 What This Is

Doctor GPT is an experimental framework to build and eventually fine-tune a transformer model specifically for generating clinical or medically relevant text. Inspired by the success of GPT-2 and medical LLM applications, this project focuses on pre-fine-tuning infrastructure and model preparation.

Currently, this is a **pre-fine-tuning implementation** intended to test:
- Domain-adapted tokenization
- Training architecture optimizations
- Model scaling approaches for large corpora

## 🔍 Why I'm Doing This

As a Master's student in Data Science at NYU with a focus on Neural Statistics, I'm deeply interested in how LLMs can be applied to real-world challenges in healthcare. Doctor GPT is my way of diving into:
- How generative AI could support medical professionals
- What it takes to build task-adapted transformer systems
- How to stabilize and scale training efficiently

## 🏗️ How It’s Built

### Model Base
- GPT-2 architecture (124M parameters)
- Framework: PyTorch + HuggingFace Transformers

### Key Upgrades and Innovations
- **Custom Tokenizer**: Byte Pair Encoding (BPE) on medical corpora
- **Subword Vocabulary**: Trained using domain-specific text (PubMed abstracts, medical notes)
- **Training Optimizations**:
  - Multi-GPU distributed training
  - Mixed precision (FP16) via `torch.cuda.amp`
  - Gradient checkpointing + accumulation
  - Cosine annealing LR scheduler with warm-up
  - AdamW optimizer with weight decay
- **Stability Improvements**:
  - Dropout layers
  - Layer normalization
  - Gradient clipping

> 💡 Note: This version is not yet fine-tuned on medical-specific downstream tasks. The current focus is on architectural readiness and token-level language modeling.

## 🧪 Sample Input/Output

> **Input Prompt:**  
*“The patient presented symptoms of acute myocardial infarction and was administered...”*

> **Raw Model Output:**  
*“...aspirin and nitroglycerin before transfer to the emergency cardiac unit. Troponin levels were monitored along with ECG signals to assess ischemic risk.”*

> **(Note: Output is illustrative and generated from preliminary runs—not medically validated.)**

## 🧭 What’s Next

- Fine-tune on curated clinical datasets (e.g., MIMIC-III, PubMed QA)
- Evaluate output coherence and factual consistency
- Explore prompt-engineered applications for mental health support systems
- Integrate with downstream tools (e.g., chatbot interfaces, decision support)

---

## 🤝 Acknowledgments

Built using HuggingFace Transformers, PyTorch Lightning, and a lot of coffee-induced ambition.

---

*This project is an independent academic exploration and not intended for clinical use or deployment without further validation.*
