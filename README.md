🔍 ClimateRAG: A RAG Pipeline for Climate Article Analysis
ClimateRAG is a Retrieval-Augmented Generation (RAG) pipeline designed to assist in querying and understanding climate-related articles. This is also specific to my use case, as i tend to do much research on climate-tech. Of course, any document can be fed to achieve similar results. 

🚧 Note: This project is currently in development towards improving it's features.

🧠 Project Purpose
Climate literature is vast and growing. This RAG implementation would help distill knowledge from content fed, by combining retrieval-based search with generation using Llama3. This way, instead of relying solely on static search or generic AI models, answers are generated from the pdf content. 

🏗️ Current Tech Stack
1) LangChain is a framework for chaining together LLM workflows

2) Ollama is a lightweight LLM runner for local model inference, it is easy to host it on my computer.

3) HuggingFace Transformers provides a library of models and transformers to inference

4) ChromaDB is an open-source vector database used to store and retrieve document embeddings

5) Python was used as a core implementation language

LLaMA 3 (via Ollama) — Used for generating grounded answers from retrieved content, ideal for this use-case.

🧩Steps:

 Load and preprocess pdf/text file via langchain's splitting documents method

 Embed documents using HuggingFace embeddings, tokenisation and verification of llama3 model

 Store and query documents via ChromaDB (vector database)

 Retrieve relevant chunks with similarity search of >=0.5, no more than k = 3 docs

 Use a prompt template for standardized question answering

 llama3 generation strictly grounded in retrieved content

 Ensure ollama is running, and then pull the desired model from ollama (llama3). More instructions in notebook

 🧠**Improvements I'm working on**:
 Refine prompt templates for accuracy and consistency

 Build a front-end or API for user interaction, able to upload multiple docs at a time

 Fine-tuning implementation 

🐛 Some things i learnt and experienced:
llama3 model could not answer some questions I had, though it performed relatively well considering it's size. This is a work in progress.
llama3 runs slowly, my device's RAM is limited in that sense. On a 16GB RAM minimally, it would improve performance significantly. 
Prompts need to be better crafted, so that llama can be more accurate
