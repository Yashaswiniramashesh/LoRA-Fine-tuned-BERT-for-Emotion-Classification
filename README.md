Developed an emotion classification workflow by implementing **Parameter-Efficient Fine-Tuning (PEFT)** on a **BERT-base-uncased** architecture. By utilizing **Low-Rank Adaptation (LoRA)**, I focused training on a minimal subset of parameters, specifically targeting the query and value layers, which drastically reduced resource consumption while maintaining high performance across six emotional states: joy, sadness, anger, love, fear, and surprise. I managed the end-to-end pipeline—including data tokenization, dataset mapping for the `dair-ai/emotion` corpus, and a custom training configuration via the Hugging Face **Trainer API**. Fine-Tuning improved accuracy significantly from 68% to 79% in just over 5 epochs.


| **Base Model** | `bert-base-uncased` |
| **Fine-Tuning Strategy** | LoRA (Low-Rank Adaptation) |
| **LoRA Rank ($r$)** | 8 |
| **LoRA Alpha** | 16 |
| **Target Modules** | Query, Value layers |
| **Dataset** | `dair-ai/emotion` (3,000 training samples) |
| **Final Accuracy** | **79.0%** (at Epoch 5) |
| **Primary Frameworks** | PyTorch, Hugging Face Transformers, PEFT, Evaluate |
