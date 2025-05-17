# CTSE Lecture Notes Chatbot

## Overview

This project implements a simple chatbot that answers questions based on CTSE (Current Trends in Software Engineering - SE4010) lecture notes. The chatbot uses the Gemini AI model along with Retrieval-Augmented Generation (RAG) to provide accurate, context-aware answers derived directly from the lecture materials.

## Features

- **Document Processing**: Automatically processes PDF and PowerPoint (PPT/PPTX) files from your lecture notes
- **Intelligent Retrieval**: Uses vector embeddings to find the most relevant content for each question
- **AI-Powered Responses**: Leverages Gemini AI to generate natural, coherent answers based on retrieved context
- **Interactive Interface**: Simple command-line interface within a Jupyter notebook

## Project Structure

```
CTSE-LECTURENOTE-CHATBOT/
├── datasets/            # Folder containing lecture notes (PDF, PPT, PPTX)
├── .env                 # Environment variables file (API key)
├── .gitignore           # Git ignore file
├── chatbot.ipynb        # Jupyter notebook with the chatbot implementation
├── LICENSE              # License file
├── README.md            # This file
└── requirements.txt     # Required packages
```

## Requirements

- Python 3.8+
- Gemini API key
- Dependencies listed in `requirements.txt`

## Installation

1. Clone this repository:
   ```
   git clone https://github.com/yourusername/CTSE-LECTURENOT.git](https://github.com/teshanj7/CTSE-LectureNote-Chatbot.git
   cd CTSE-LECTURENOT
   ```

2. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

3. Create a `.env` file in the project root and add your Gemini API key:
   ```
   GEMINI_API_KEY=your_gemini_api_key_here
   ```

4. Place your CTSE lecture notes (PDF and PowerPoint files) in the `datasets` folder.

## Usage

1. Start Jupyter Notebook:
   ```
   jupyter notebook
   ```

2. Open `chatbot.ipynb` and run all cells.

3. Once the notebook has processed your lecture notes, you can ask questions about CTSE topics. Type your question at the prompt and press Enter. Type 'exit' to end the conversation.

Example questions:
- What is cloud computing?
- What is priority queue pattern?
- What is an Artificial Neural Network?

## How It Works

1. **Document Loading**: The system loads all PDF and PowerPoint files from the `datasets` folder.
2. **Processing**: Documents are split into manageable chunks and converted to vector embeddings.
3. **Query Processing**: When you ask a question, the system:
   - Searches for the most relevant chunks from your lecture notes
   - Retrieves these chunks as context
   - Uses Gemini AI to generate a response based on this context

## Acknowledgments

- Gemini AI for providing the language model
- LangChain for document processing and RAG implementation (Ref: https://python.langchain.com/docs/tutorials/rag/)
- Google Colab for providing the infrastructure to test the RAG
