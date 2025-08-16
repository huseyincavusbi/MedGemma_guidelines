# MedGemma_guidelines
# Fine-Tuning MedGemma with Clinical Guidelines

This repository contains a Jupyter notebook demonstrating the process of fine-tuning the `unsloth/medgemma-4b-pt` model on a dataset of clinical guidelines. The goal is to adapt the model to better understand and generate text based on the structure and content of medical guidelines.

## What This Notebook Does

This notebook walks through the following key steps:

1.  **Load the Pre-trained Model:** It starts by loading the `unsloth/medgemma-4b-pt` model, applying 4-bit quantization for efficient training.
2.  **Configure LoRA Adapters:** Low-Rank Adaptation (LoRA) is set up to enable efficient fine-tuning by adding a small number of trainable parameters to the model.
3.  **Prepare the Dataset:** The notebook loads the `epfl-llm/guidelines` dataset and formats it into a simple "Source" and "Guideline Text" structure for the model to learn from.
4.  **Fine-Tuning:** The model is then fine-tuned on the prepared dataset using the `SFTTrainer` from the TRL library.
5.  **Inference and Testing:** A simple test is performed to demonstrate the model's ability to generate guideline-style text based on a given source.
6.  **Save and Upload:** Finally, the notebook shows how to save the resulting LoRA adapters locally and upload them to the Hugging Face Hub for future use.

## Adapters on [Hugging Face](https://huggingface.co/huseyincavus/medgemma-4b-guidelines-lora)
## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
