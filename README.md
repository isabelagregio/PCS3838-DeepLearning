# Logic Circuit Classification with Qwen3-VL-8B

Multimodal classification of logic-circuit diagrams using **Qwen3-VL-8B-Instruct**, **4-bit QLoRA fine-tuning**, and **adaptive multiview inference**.

## Approach

- Fine-tune Qwen3-VL-8B with QLoRA on circuit images and questions.
- Predict gate counts (`0`–`7`) or binary circuit outputs (`True`/`False`) using constrained label scoring.
- Compare original, contrast-enhanced, and cropped image views.
- Use confidence-based thresholds to run additional views only when needed, calibrated on a validation split.

## Run

1. Open `qwen3-vl-8b-qlora-github.ipynb` in Kaggle.
2. Enable an NVIDIA T4 GPU and internet access.
3. Attach the dataset and run the notebook cells in order.

The notebook handles training, validation, inference, and CSV submission export. Dataset files and trained model weights are not included.

## Stack

Python · PyTorch · Hugging Face Transformers · PEFT · ms-swift · bitsandbytes
