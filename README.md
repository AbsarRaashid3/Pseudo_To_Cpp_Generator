# TranslodeP2C <br>

## Overview <br>

TranslodeP2C is an AI-powered pseudocode-to-C++ conversion system. <br>
Leveraging a Transformer-based seq2seq model,  <br>
it translates pseudocode descriptions into structured C++ programs. <br>
The project includes preprocessing, vocabulary building, training, <br>
and inference, with an interactive Streamlit UI. <br>

## Features 
* Transformer-based sequence-to-sequence model for code generation. <br>
* Converts pseudocode to C++ using deep learning. <br>
* Preprocessing and vocabulary management for structured learning. <br>
* Training pipeline with customizable hyperparameters. <br>
* Inference system with greedy decoding. <br>
* Streamlit-based web UI for user-friendly interactions. <br>

## Installation 

### Prerequisites

Ensure you have the following installed:
* Python 3.8+ <br>
* PyTorch <br>
* Streamlit <br>
* tqdm <br>


## Setup
1. Clone the repository:
   git clone https://github.com/absarraashid3/translodep2c.git
   cd translodep2c
2. Install dependencies:
   pip install -r requirements.txt
3. Prepare your dataset and place it in data/train/split/.

   
## Usage

### Preprocessing
Convert TSV trInaining data into paired pseudocode-code format:
** python src/preprocess.py --input_tsv "C:\Projects\GenAi\data\train\split\spoc-train-train.tsv" --output_txt "C:\Projects\GenAi\data\train_pairs.txt" **

### Building Vocabulary
Generate vocabulary pickle files from training pairs:
** python src/vocab.py --pairs_file "C:\Projects\GenAi\data\train_pairs.txt" --src_vocab_file "src/src_vocab.pkl" --tgt_vocab_file "src/tgt_vocab.pkl" **

## Training the Model
Train the Transformer model for pseudocode-to-C++ conversion:
** python src/train.py --pairs_file "C:\Projects\GenAi\data\train_pairs.txt" --src_vocab_file "src/src_vocab.pkl" --tgt_vocab_file "src/tgt_vocab.pkl" --epochs 10 --batch_size 8 **

## Inference
Generate C++ code from input pseudocode:
** python src/infer.py --model_checkpoint transformer_seq2seq.pt --src_vocab_file "src/src_vocab.pkl" --tgt_vocab_file "src/tgt_vocab.pkl" --pseudocode "read n print factorial of n" **

## Web Application
Launch the Streamlit UI:
** streamlit run src/app.py **

Enter pseudocode and get auto-generated C++ code!

## Future Enhancements
* Implement beam search decoding for better predictions.
* Fine-tune with more programming languages.
* Optimize the model for faster inference.

# 🚀 Transform pseudocode into real C++ with TranslodeP2C!


![1](https://github.com/user-attachments/assets/996f509a-a77e-458e-a17b-d584c4bfada4)
![2](https://github.com/user-attachments/assets/77483e06-6686-4fd1-9e08-b58ae5547b19)
![3](https://github.com/user-attachments/assets/abd103cc-14db-4d4a-be9e-adcb0c9f13ba)
![4](https://github.com/user-attachments/assets/54e100f7-2a13-4834-a623-a00d84acc226)
