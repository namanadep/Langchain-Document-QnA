# Document Q&A with LangChain and Groq

A Streamlit application that enables question-answering on PDF documents using LangChain, Groq's Llama3 model, and Google's Generative AI for embeddings.

## Features

- PDF document processing and vectorization
- Question-answering using Groq's Llama3-8b-8192 model
- Vector embeddings using Google's Generative AI
- Interactive Streamlit interface
- FAISS vector store for efficient document retrieval

## Setup

1. Clone this repository
2. Install the required dependencies:

```sh
pip install streamlit langchain-groq langchain langchain-community faiss-cpu python-dotenv langchain-google-genai
```

3. Create a `.env` file in the root directory with your API keys:

```
GROQ_API_KEY=your_groq_api_key_here
GOOGLE_API_KEY=your_google_api_key_here
```

## Usage

1. Run the Streamlit app:

```sh
streamlit run app.py
```

2. Upload your PDF documents through the web interface
3. Ask questions about the documents' content

## Project Structure

- `app.py`: Main application file containing the Streamlit interface and Q&A logic
- `.env`: Configuration file for API keys
- `requirements.txt`: List of Python dependencies

## Dependencies

- streamlit
- langchain-groq
- langchain
- langchain-community
- faiss-cpu
- python-dotenv
- langchain-google-genai

## How It Works

1. Documents are loaded using PyPDFDirectoryLoader
2. Text is split into chunks using RecursiveCharacterTextSplitter
3. Google's Generative AI creates embeddings for document chunks
4. FAISS stores the vector embeddings for efficient retrieval
5. User questions are processed using Groq's Llama3 model
6. Relevant document sections are retrieved and used to generate answers

## License

MIT
