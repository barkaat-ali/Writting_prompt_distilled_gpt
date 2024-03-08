## Creative Writing with DistilGPT-2

This repository contains code for fine-tuning a pre-trained DistilGPT-2 model from the Hugging Face Transformers library to assist in creative writing tasks. The model is trained on the WritingPrompts dataset, which consists of prompts and corresponding story continuations, making it suitable for text generation tasks.

### Key Components:

1. **Data Preprocessing**: The `load_and_preprocess_data` function is responsible for loading the WritingPrompts dataset, preprocessing it, and creating a DataFrame for training. The preprocessing steps include handling special characters, removing tags, lowercasing text, and lemmatization using spaCy.

2. **Tokenization and Dataset Creation**: The `load_dataset` function tokenizes the input sequences using the GPT2 tokenizer and creates train and validation datasets using the Hugging Face Datasets library. Tokenization is performed without splitting the text into tokens, preserving the original sequence structure.

3. **Model Training**: The fine-tuning process involves training the DistilGPT-2 model using the `Trainer` class from the Transformers library. Training arguments such as the number of epochs, batch size, and output directory are specified, along with a data collator for padding tokenized sequences.

4. **Model Saving**: Once training is complete, both the trained model and tokenizer are saved to the specified directory (`creative_writing_distilgpt2_story_gen`). The trained model is saved as `pytorch_model.bin`, containing the model architecture and parameters. The tokenizer is saved as `tokenizer_config.json`, storing tokenization settings and vocabulary.

### How to Use:

1. Download the ipynb file.
2. If you have Jupyter Notebook in your local enviroment and also have good gpu then you can try to run cell locally otherwise import in Kaggle.
3. Run all cells.
4. After training, the trained model and tokenizer will be saved in the specified output directory.

Feel free to experiment with different hyperparameters, models, or datasets to further improve text generation performance!
