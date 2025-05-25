🔍 ClimateRAG: A RAG Pipeline for Climate Article Analysis
ClimateRAG is a Retrieval-Augmented Generation (RAG) pipeline designed to assist in querying and understanding climate-related articles. This is also specific to my use case, as i tend to do much research on climate-tech. Of course, any document can be fed to achieve similar results. 

🚧 Note: This project is currently in development. Core components have been implemented, and I'm working on solving dependency issues and bugs.

🧠 Project Purpose
Climate literature is vast and growing. This RAG implementation would help distill knowledge from content fed, by combining retrieval-based search with generation using Llama3. This way, instead of relying solely on static search or generic AI models, answers are generated from the pdf content. 

🏗️ Current Tech Stack
LangChain — Framework for chaining together LLM workflows

Ollama — Lightweight LLM runner for local model inference

HuggingFace Transformers — For model loading and tokenisation

ChromaDB — Open-source vector database used to store and retrieve document embeddings, easy to use and setup

Python — Core implementation language

LLaMA 3 (via Ollama) — Used for generating grounded answers from retrieved content, ideal for this use-case.

🧩Steps (WIP)
 Load and preprocess pdf/text file via langchain's splitting documents method

 Embed documents using HuggingFace embeddings, tokenisation and verification of llama3 model

 Store and query documents via ChromaDB (vector database)

 Retrieve relevant chunks with similarity search of >=0.5, no more than k = 3 docs

 Use a prompt template for standardized question answering

 llama3 generation strictly grounded in retrieved content

 Potential improvements:
 Improve chunking and semantic splitting

 Refine prompt templates for accuracy and consistency

 Build a front-end or API for user interaction

 Add more evaluation scripts and benchmarks for debugging

 Fine-tuning implementation 


🐛 Known Issues / Work in Progress
Prompt tuning for optimal relevance

Chunking strategy improvements to reduce context fragmentation

Bugs in retrieval logic and embedding mismatch

UI/API integration not yet implemented
