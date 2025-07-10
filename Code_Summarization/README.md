# Code Summarization using Transformer-Based Models

This project explores the fine-tuning of pre-trained Transformer-based models—**PLBART** and **CodeT5**—for the task of summarizing Python code snippets into natural language docstrings. The objective is to enhance code readability and documentation using automated summarization.

## 📚 Dataset

- **Source**: [CodeXGLUE - Code-to-Text (Python)](https://github.com/microsoft/CodeXGLUE)
- **Subset Used**: First 1% to reduce training time
- **Split**:
  - Training: 2,518 samples
  - Validation: 139 samples
  - Test: 149 samples
- **Each sample**: Python code snippet + corresponding docstring

## ⚙️ Preprocessing

- Used `Salesforce/codet5-small` tokenizer
- Max sequence length: `512`
- Tokenized code as input, docstring as target
- Formatted data for Hugging Face `Transformers` compatibility

## 🧠 Models and Training

Two models were fine-tuned:

1. **PLBART**
2. **CodeT5 (Salesforce/codet5-small)**

Training settings:
- **Optimizer**: AdamW
- **Learning Rate**: 5e-5
- **Epochs**: 3
- **Batch Size**: 4 (due to hardware constraints)

Evaluation metrics:
- **BLEU**
- **ROUGE (ROUGE-1, ROUGE-2, ROUGE-L, ROUGE-Lsum)**

## 📊 Results

| Model   | BLEU  | ROUGE-1 | ROUGE-2 | ROUGE-L | ROUGE-Lsum |
|---------|-------|----------|----------|----------|-------------|
| PLBART  | 0.956 | 0.904    | 0.904    | 0.907    | 0.905       |
| CodeT5  | 0.969 | 0.992    | 0.991    | 0.991    | 0.992       |

✅ **CodeT5 outperformed PLBART** in both BLEU and ROUGE metrics, showing superior performance in capturing code semantics and generating meaningful summaries.

## 📝 Conclusion

Fine-tuning pre-trained models like CodeT5 yields strong performance in code summarization tasks. CodeT5, in particular, demonstrates high effectiveness and recall, making it a better choice for practical applications in code documentation and comprehension.

---

