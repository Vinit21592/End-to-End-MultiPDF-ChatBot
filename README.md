# End-to-End-MultiPDF-ChatBot
End to end multipdf chatbot application using langchain as framework and Pinecone as vectordb

# Introduction
------------
The MultiPDF Chat App is a Python application that allows you to chat with multiple PDF documents. You can ask questions about the PDFs using natural language, and the application will provide relevant responses based on the content of the documents. This app utilizes a language model to generate accurate answers to your queries. Please note that the app will only respond to questions related to the loaded PDFs.

# How It Works
------------
![PDF-LangChain](https://github.com/Vinit21592/End-to-End-MultiPDF-ChatBot/assets/78821357/c73f1d85-8d6f-426c-af4c-ab103d962a30)

The application follows these steps to provide responses to your questions:

1. PDF Loading: The app reads multiple PDF documents and extracts their text content.

2. Text Chunking: The extracted text is divided into smaller chunks that can be processed effectively.

3. Language Model: The application utilizes a language model to generate vector representations (embeddings) of the text chunks.

4. Similarity Matching: When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

5. Response Generation: The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.

# How to run?
------------
### STEPS:

Clone the repository

```bash
Project repo: https://github.com/Vinit21592/End-to-End-MultiPDF-ChatBot.git
```

### STEP 01 - Create a conda environment after opening the repository

```bash
conda create -n pdfchatbot python=3.9 -y
```

```bash
conda activate pdfchatbot
```

### STEP 02 - Install the requirements

```bash
pip install -r requirements.txt
```

### Create a `.env` file in the root directory and add your Pinecone, Huggingfacehub credentials as follows:

```ini
PINECONE_API_KEY = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
PINECONE_API_ENV = "xxxxxxxxxxxxxxxxxxxxxxxx"
HUGGINGFACEHUB_API_TOKEN = "xxxxxxxxxxxxxxxxxxxxxxxxxxxxxx"
```

### Download the quantize model from the link provided in model folder & keep the model in the model directory:

```ini
## Download the Llama 2 Model:

llama-2-7b-chat.ggmlv3.q4_0.bin

## From the following link:
https://huggingface.co/TheBloke/Llama-2-7B-Chat-GGML/tree/main
```

```bash
# Run the following command
python store_index.py
```

```bash
# Finally run the following command
python app.py
```

Now,
```bash
open up localhost:
```

# Techstack Used
------------
- Python
- LangChain
- Flask
- Meta Llama2 OR google/flan-t5-xxl
- Pinecone