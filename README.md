# ODSC - Labelling Sparse Data at Scale using Semantic Search

This repository contains the presentation slides for the ODSC West 2024 talk titled "Labelling Sparse Data at Scale using Semantic Search" by Shubham Goel. 

## Problem Statement

The primary concern addressed is the need for robust models that can classify content accurately across several risk categories like profanity, hate speech, adult content, drugs, alcohol, and tobacco, amongst others. Brands seek to avoid their advertisements appearing next to harmful content, which could negatively affect consumer perceptions and sales.

## Data Challenges

The document also illustrates the immense scale of data involved and the complexity of searching and indexing relevant content that could potentially violate brand safety norms.

## Semantic Search Solution

To tackle these challenges, the implementation of OpenAI's CLIP model for extracting embeddings is discussed. The CLIP model, pre-trained on 400 million image-text pairs, can be used to extract embeddings from text and images to enable semantic search.

## Indexing Strategy

For efficient searching, embeddings extracted from some frames across platforms are indexed using a  Approximate Nearest Neighbors (ANN) algorithm known as Hierarchical Navigable Small Worlds (HNSW) graph. Qdrant, an open-source, scalable, and efficient vector search engine supports this operation, facilitating real-time serving and complex filtering queries.

## Usage

The system is used for labeling data which then feeds into a Vision Transformer (ViT) model for making predictions across several risk categories. This setup helps in identifying and correcting incorrect labels by providing additional similar images to the next round of labeling.

## Future Goals

Future enhancements include large-scale fine-tuning of the CLIP model, scaling to over 1 billion vectors, and adding additional metadata to enable more complex filters.