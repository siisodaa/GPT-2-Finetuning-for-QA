
# GPT-2 Fine-Tuning for NarrativeQA

This project demonstrates how to fine-tune a GPT-2 model on the NarrativeQA dataset. The fine-tuning process involves tokenizing the dataset, training the model, and evaluating it after each epoch.

### Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Code Overview](#code-overview)
- [Model Saving and Evaluation](#model-saving-and-evaluation)
- [Results](#results)
- [Contributing](#contributing)

### Installation

#### Prerequisites

- Python 3.8+
- PyTorch
- Transformers library from Hugging Face
- Datasets library from Hugging Face
- tqdm
- pandas

#### Installation Steps

1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/gpt2-finetuning.git
    cd gpt2-finetuning
    ```

2. Create a virtual environment:
    ```bash
    python3 -m venv venv
    source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
    ```

3. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

### Usage

1. To fine-tune the GPT-2 model on the NarrativeQA dataset, simply run the main script:
    ```bash
    python main.py
    ```

    This will load the NarrativeQA dataset, preprocess the data, fine-tune the model, and save the best model based on the training process.

### Code Overview

The main script performs the following steps:

1. **Setup Logging**: Initializes logging for tracking the fine-tuning process.
2. **Set Seed**: Sets the random seed for reproducibility.
3. **Load and Parse Dataset**: Downloads and loads the NarrativeQA dataset from the internet.
4. **Preprocess Data**: Prepares the data for tokenization and model training.
5. **Tokenize Data**: Tokenizes the data using the GPT-2 tokenizer.
6. **Initialize Model**: Loads the pre-trained GPT-2 model and resizes token embeddings.
7. **Training Arguments**: Defines the training arguments for the Trainer.
8. **Initialize Trainer**: Sets up the Trainer with the model, training arguments, data collator, and tokenized dataset.
9. **Custom Training Loop**: Trains the model and evaluates it on the validation dataset after each epoch.
10. **Save Model and Tokenizer**: Saves the fine-tuned model and tokenizer.

### Model Saving and Evaluation

The model and tokenizer are saved during training based on the specified output directory. The evaluation results are logged after each epoch, and the best model is saved based on the training process.

### Results

After running the script, the fine-tuned model and tokenizer will be saved in the specified output directory.

### Contributing

Contributions are welcome! Please feel free to submit a Pull Request.
