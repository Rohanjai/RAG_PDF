# RAG-Based Streamlit App

This repository contains a Streamlit application built using a Retrieval-Augmented Generation (RAG) approach. The app allows users to upload a PDF document, parses its content, and provides answers to questions based on the uploaded PDF. The application leverages the Llama 3.2 model for question answering and ChromaDB to store and retrieve vector embeddings efficiently.

## Features
#### PDF Parsing:
-   Users can upload any PDF document, which is processed and split into smaller chunks for analysis.
#### Vector Store:
-	Uses ChromaDB to store vector embeddings of the PDF content, enabling efficient similarity search for relevant information.
#### Question Answering:
-	Employs the Llama 3.2 model to generate answers to user questions based on the PDF content.
#### RAG Architecture:
-	Combines retrieval from ChromaDB with the generative capabilities of Llama 3.2 to provide accurate and context-aware answers.

## Installation

### Prerequisites

Ensure the following tools are installed:
- Python 3.8 or higher
- pip (Python package manager)

### Steps
1.	Clone the Repository:
```bash
git clone https://github.com/Rohanjai/RAG_PDF.git
cd rag-streamlit-app
```

2.	Install Dependencies:
```bash
pip install -r requirements.txt
```

3.	Download Model Weights:
- Ensure the weights for the Llama 3.2 model are downloaded and available. Update the configuration in the app to point to the model path.
4.	Run the App:
```bash
streamlit run app.py
```
### How It Works
1.	Upload PDF:
	-	Users put the  PDF file in `/data` directory.
2.	PDF Parsing:
	-	The PDF is processed using a parsing function to extract and split content into manageable chunks.
3.	Vectorization:
	-	Each chunk is converted into embeddings using a pre-trained embedding model.
	-	Embeddings are stored in ChromaDB for efficient retrieval.
4.	Question Answering:
	-	When a question is asked, the app retrieves relevant chunks using a similarity search in ChromaDB.
	-	The retrieved content is passed to the Llama 3.2 model, which generates the answer.
5.	Display Results:
	-	The app displays the answer along with the context from the original document.

### Key Technologies
-	Streamlit: For creating a responsive and interactive web application.
-	Llama 3.2: A state-of-the-art language model used for generating answers.
-	ChromaDB: A powerful and scalable vector database for efficient information retrieval.
-	LangChain: For managing document loaders, text splitters, and RAG workflows.

