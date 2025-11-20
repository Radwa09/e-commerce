# e-commerce
RAG project for Brazilian e-commerce question answering using FAISS and FLAN-T5
Brazilian E-Commerce RAG Project
Project Overview

This project implements a Retrieval-Augmented Generation (RAG) system for answering questions about Brazilian e-commerce data.
It combines FAISS vector search over order summaries with a FLAN-T5 language model to generate accurate and grounded answers.
A public Gradio interface allows users to interact with the system in natural language.

Features

Answer user questions about orders, customers, products, and prices.

Retrieve relevant information from a knowledge base of top 1000 orders.

Compare two LLMs: FLAN-T5-Base and FLAN-T5-XL.

Publicly accessible deployment via Gradio.

Lightweight and fast using FLAN-T5-Base for practical deployment.

Project Structure
brazilian-ecommerce-rag/
│
├─ app_gradio_rag_brazilian_ecommerce_fast1000_fixed.py  # Main RAG script
├─ requirements.txt                                      # Required Python packages
├─ README.md                                             # Project description
├─ dataset/                                              # Optional: CSV files for top 1000 orders

Setup Instructions

Make sure Python 3.8 or higher is installed.

Install all required libraries listed in requirements.txt.

Open the main Python script (app_gradio_rag_brazilian_ecommerce_fast1000_fixed.py) in your IDE or Python environment.

Run the script to launch the Gradio interface.

Follow the on-screen instructions to ask questions about the Brazilian e-commerce dataset.

Example Queries

"Which products did customer 12345 order?"

"What is the total price of order 987?"

"Show me all orders containing Electronics and Toys."

Model Comparison
Feature	FLAN-T5-Base	FLAN-T5-XL
Model Size	250M params	3B params
Accuracy on multi-product queries	Medium	High
Reasoning & Context Handling	Medium	High
Inference Speed	Fast	Slow
Deployability	Easy	Challenging

Conclusion: FLAN-T5-Base was chosen for deployment due to speed, lower resource requirements, and practical stability, while FLAN-T5-XL is better for research-level evaluation.

Deployment

Public Gradio app: [Insert your link here]

Accepts natural language questions and returns grounded answers.

Full pipeline: dataset → embeddings → FAISS retrieval → LLM generation → Gradio UI.

Acknowledgments

Hugging Face Transformers

LangChain

FAISS by Facebook AI

Sentence-Transformers
