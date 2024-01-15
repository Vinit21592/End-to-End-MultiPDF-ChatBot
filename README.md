# End-to-End-MultiPDF-ChatBot
End to end multipdf chatbot application using langchain as framework and Pinecone as vectordb

# How to run?
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

### Techstack Used:

- Python
- LangChain
- Flask
- Meta Llama2 OR google/flan-t5-xxl
- Pinecone