# Chat With a Book (RAG)

Chat with any book using this RAG model, this model uses LangChain and an LLM to generate smart answers to your questions based on the given book.

The book has to be in the data directory and it shoud be in markdown format.

You can find books online from website's such as [Project Gutenberg](https://www.gutenberg.org/) or [Annas Archive](https://annas-archive.org/)

Convert your 'epub' book into markdown using this [website](https://www.zamzar.com/convert/epub-to-md/).

## Install Dependencies 

1. Create a virtual environment, this project was created using Python 3.11.9
2. Install all depencencies listed in `requirements.txt` file using this command.

    ```bash
    pip install -r requirements.txt
    ````
3. Install markdown dependency after installing the above dependencies for parsing the book in markdown.
    ```bash
    pip install "unstructure[md]"
    ```

## Create Data Embeddings
1. Create the [Chroma](https://docs.trychroma.com/) database using [`create_db.py`](./create_db.py) script.

    ```bash
    python3 create_db.py
    ```

## Ask Questions
1. Ask your questions using the [`query_data.py`](./query_data.py) script
    ```bash
    python3 query_data.py "Who is the main character ?"
