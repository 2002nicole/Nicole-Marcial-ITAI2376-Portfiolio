# Requirements and Dependencies — Final Project Cookie Recipe Adaptation Agent

## Full Project Repository

The complete final project repository is available here:

```text
https://github.com/2002nicole/NicoleMarcial_Solo_ITAI2376
```

The full repository contains the actual `requirements.txt` file used for the final project.

## Recommended Environment

The project was developed in:

```text
Python 3.11+
Google Colab
```

The notebook was designed to run in Google Colab and uses Google Drive for some dataset/project file storage.

## Dependency List

The final project `requirements.txt` includes:

```text
pandas==2.2.2
langchain==1.2.17
langchain-openai==1.2.1
langchain-huggingface==1.2.2
langchain-chroma==1.1.0
langchain-text-splitters==1.1.2
sentence-transformers==5.4.1
tiktoken==0.12.0
gradio==6.14.0
```

## Installation Command

To install dependencies in the full project repository, run:

```bash
pip install -r requirements.txt
```

## Environment Variables

The project requires an OpenAI API key.

Create a `.env` file based on `.env.example` in the full project repository.

Example:

```env
OPENAI_API_KEY=your_key_here
```

Do not upload a real `.env` file to GitHub.

## Main Libraries and Their Purpose

### pandas

Used for loading, cleaning, filtering, and working with recipe data.

### LangChain

Used to build the single-agent workflow, define tools, and connect the agent components.

### langchain-openai

Used to connect the agent to the OpenAI language model provider.

### langchain-huggingface

Used to connect Hugging Face embedding models to the LangChain workflow.

### langchain-chroma

Used to connect LangChain with the Chroma vector database.

### langchain-text-splitters

Used to split recipe and baking knowledge documents into smaller chunks for retrieval.

### sentence-transformers

Used for the embedding model:

```text
sentence-transformers/all-MiniLM-L6-v2
```

### tiktoken

Used for token-related processing with OpenAI-compatible workflows.

### gradio

Used to build the optional user-facing interface for the demo.

## How to Run the Agent

In the full project repository:

1. Open `agent.ipynb`.
2. Install dependencies.
3. Add your OpenAI API key.
4. Run the notebook from top to bottom.
5. Run the optional Gradio section if you want the interface.

## Notes

This file is included in the ITAI 2376 portfolio repository as a dependency summary. The authoritative dependency file is the `requirements.txt` file in the full final project repository.
