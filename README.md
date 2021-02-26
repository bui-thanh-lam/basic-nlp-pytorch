# Implementation of basic NN model for NLP tasks

## Motivation:

This repository is aim for personal practicing deep learning with PyTorch. I followed some tutorials and tried to reproduce their results.

## Contents:

1. Word2Vec SG model.
2. Seq2Seq: Vanilla seq2seq, Seq2Seq with Attention (Luong et al version). Training for machine translation task.
3. Transformer: Conv NN with Attention, Transformer with Attention only. Training for single doc abstractive summarization task.

All models have been trained from scratch. I've used some libraries for data preprocessing and evaluating (i.g: transformers, datasets, rouge...).

## Results summary:

#### Machine translation:

These models have been trained under the same hardware and hyperparams.
I've set: Adam optimizer with init lr 0.0005, batch size 128, 10 epochs, max input length 32, max output length 64, teacher forcing ratio 0.1.
I've used entire huggingface's mt_eng_vietnamese dataset for training, validating and testing.

1. Uni-Uni Seq2Seq w/o attention: last valid loss 4.059; test loss: 4.054
2. Bi-Uni Seq2Seq w/o Attention: last valid loss ; test loss
3. Bi-Uni Seq2Seq with Global Attention: last valid loss ; test loss

You can find these results on my notebooks in this repo.

#### Abstractive summarization:

