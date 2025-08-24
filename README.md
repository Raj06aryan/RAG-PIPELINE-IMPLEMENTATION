# RAG-PIPELINE-IMPLEMENTATION
📌 Overview

This project implements a Retrieval-Augmented Generation (RAG) pipeline to build a domain-specific, context-aware medical chatbot. The system leverages semantic search and an optimized language model to provide accurate, query-relevant medical responses from clinical text sources.

⚙️ Features

Domain-Specific RAG Chatbot: Tailored for medical queries using clinical text corpus.

Efficient Text Parsing:

Processed 600+ pages of clinical text with PyMuPDF and spaCy.

Generated ~800 sentence-level chunks optimized for semantic retrieval.

Semantic Search with FAISS:

Encoded chunks using all-mpnet-base-v2 embeddings.

Enabled top-k retrieval with dot-product similarity for fast and relevant results.

LLM Integration:

Integrated Gemma-2B model with prompt injection for accurate query answering.

Achieved ~7s response latency per query.

Performance Optimizations:

4-bit quantization (via bitsandbytes) for reduced memory footprint.

FlashAttention2 integration for efficient attention computation.

Resulted in ~20% faster inference and ~20% lower memory usage.

🏗️ Tech Stack

Python

PyMuPDF → PDF parsing

spaCy → NLP preprocessing

Sentence-Transformers (all-mpnet-base-v2) → Embedding generation

FAISS → Vector database for similarity search

Gemma-2B → Core LLM

bitsandbytes → 4-bit quantization

FlashAttention2 → Optimized attention mechanism
