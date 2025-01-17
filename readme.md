# Understanding the EU AI Act QA System Implementation

This code showcases a Question-Answering system designed specifically for analyzing the EU **AI Act**. 

The system combines several technologies to create an efficient and accurate document analysis tool. At its core, it uses **LangChain** for orchestration, the **Mistral-7B** language model for local processing, and **FAISS** for vector-based document search.

The system's workflow begins with document processing, where it loads and splits the AI Act PDF into manageable chunks of 10,000 characters each. These chunks are then transformed into numerical representations (embeddings) using HuggingFace's **all-MiniLM-L6-v2** model, creating a searchable database through FAISS vector storage. This enables efficient retrieval of relevant text sections when questions are asked.

The heart of the system lies in its use of the Mistral-7B instruction-tuned model, configured with specific parameters to balance response accuracy and creativity. When a question is asked, the system retrieves the two most relevant document chunks and uses them as context for the language model to generate informed answers. This approach ensures that responses are grounded in the actual content of the AI Act rather than relying on potentially outdated pre-trained knowledge.

The implementation includes practical examples, demonstrating the system's ability to answer various questions about the AI Act, from its fundamental purpose to specific regulations about AI-generated content and unacceptable practices. This makes it a valuable tool for anyone needing to understand or work with the EU AI Act, providing accurate, context-aware responses to their queries.