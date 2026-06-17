Stylized Image Captioning in Bengali

A deep learning system that generates stylized image captions in the Bengali language, combining a custom encoder-decoder architecture  for multi-style caption generation. Built as an undergraduate thesis project targeting the low-resource Bengali NLP landscape.


Overview

Standard image captioning systems produce a single factual description per image. This project extends that paradigm by generating captions in multiple style for say romantic, humorous and factual all in Bengali. The pipeline fuses visual feature extraction with a language generation backbone fine-tuned for Bangla, and leverages Gemini's instruction-following capability to enforce stylistic constraints.

Features

Visual feature extraction using pretrained Vision Transformer encoders
Bengali caption generation via a fine-tuned sequence-to-sequence model
Multi-style output from a single image
Evaluation using BLEU, METEOR, and BERTScore on Bengali captions
Low-resource language focus with custom dataset preprocessing for Bengali text

Architecture

Input Image
     │
     ▼
┌─────────────────────┐
│  Visual Encoder      │  (CNN / ViT backbone)
│  Feature Extraction  │
└─────────────────────┘
     │  image features
     ▼
┌─────────────────────┐
│  Caption Decoder     │  (Seq2Seq / Transformer)
│  Bengali LM Head     │  fine-tuned on Bengali captions
└─────────────────────┘
     │  base Bengali caption
     ▼
┌─────────────────────┐
│  Gemini API          │  style-conditioned rewriting
│  Style Controller    │  (formal / poetic / humorous / descriptive)
└─────────────────────┘
     │
     ▼
Stylized Bengali Caption
