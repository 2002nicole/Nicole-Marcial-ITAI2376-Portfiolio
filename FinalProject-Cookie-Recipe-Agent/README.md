# Final Project — Cookie Recipe Adaptation Agent

## Full Project Repository

The full final project is stored in its own complete GitHub repository:

```text
https://github.com/2002nicole/NicoleMarcial_Solo_ITAI2376
```

This folder is a portfolio summary for the ITAI 2376 course portfolio. I kept the final project in a separate repository to avoid duplicating the same code, demo, data, and documentation across multiple repositories.

## Project Overview

The Cookie Recipe Adaptation Agent is my final project for **ITAI 2376: Deep Learning**. It is a single AI agent that helps users adapt cookie recipes through ingredient substitutions, batch size changes, dietary adjustments, and texture guidance.

The project is focused on cookies only so the agent stays realistic, manageable, and more reliable.

## Problem Statement

Baking is sensitive to small ingredient and ratio changes. Beginners often struggle when they need to halve a recipe, replace an ingredient, or adjust a recipe for dietary needs without ruining the texture, spread, flavor, or structure.

This project solves that problem by building a cookie-focused AI agent that gives practical adaptation guidance for beginner and intermediate home bakers.

## Target User

The target users are beginner or intermediate home bakers who want clearer support when changing cookie recipes.

## Source Code Location

The actual implementation is available in the full project repository:

```text
agent.ipynb
```

The notebook contains the complete agent workflow, including:

- Data preparation
- Baking knowledge base setup
- Recipe retrieval setup
- Embedding and vector store creation
- Custom tool definitions
- LangChain agent setup
- Real-world scenario testing
- Optional Gradio interface

## Approach and Methodology

The agent uses a single-agent architecture with retrieval and custom tools.

The main workflow is:

1. The user gives a cookie-related request.
2. The agent interprets the request.
3. The agent decides which custom tool is needed.
4. The tool returns recipe or baking guidance.
5. The agent uses the tool output to produce a beginner-friendly final response.

The project uses Retrieval-Augmented Generation so the agent can retrieve relevant cookie recipe and baking context instead of only relying on the language model’s general knowledge.

## Architecture Summary

The final implementation includes three main layers:

### 1. Recipe and Baking Knowledge Layer

The project uses a filtered cookie recipe dataset and a small cookie baking knowledge base. These text sources are converted into LangChain documents, split into chunks, embedded with a Hugging Face sentence-transformer model, and stored in a local Chroma vector database.

### 2. Custom Tool Layer

The agent has custom tools for the main cookie-adaptation tasks:

- Recipe retrieval
- Ingredient scaling
- Substitution guidance
- Full recipe adaptation

### 3. Agent Reasoning Layer

The LangChain agent uses an OpenAI language model as the reasoning engine. It interprets the user’s request, decides which tool to call, observes the returned result, and writes the final response.

## Main Technologies

The full project uses:

- Python
- LangChain
- OpenAI language model integration
- Hugging Face sentence-transformer embeddings
- Chroma vector database
- Pandas
- Gradio
- Google Colab

## Custom Tools

### Recipe Retrieval Tool

Retrieves relevant cookie recipe examples and baking guidance from the knowledge base.

### Ingredient Scaling Tool

Scales ingredient quantities when the user changes the batch size or number of servings.

### Substitution Guidance Tool

Suggests cookie-friendly replacements and explains likely effects on texture, spread, flavor, structure, or moisture.

### Recipe Adaptation Tool

Adapts a full cookie recipe based on requests such as egg-free, butter replacement, or dietary adjustments.

## Results and Evaluation

The agent was tested on real-world cookie adaptation scenarios, including:

- Butter substitution
- Egg-free cookie adaptation
- Scaling a recipe from 24 servings to 12 servings

The final project successfully demonstrated a working single-agent system with tool use, retrieval, custom recipe logic, and a user-facing Gradio demo.

One important testing issue involved ingredient formatting during batch scaling. For example, some scaled ingredient amounts were originally displayed in awkward units, so the code was adjusted to make ingredient amounts cleaner and easier to read.

## Demo

The full project repository includes the demo video:

```text
demo.mp4
```

The demo shows the agent handling multiple real-world cookie recipe adaptation scenarios.

## Requirements and Dependencies

The full dependency list is stored in the final project repository:

```text
requirements.txt
```

A summary is also included in this portfolio folder:

```text
REQUIREMENTS.md
```

## Data Access

The full project uses a filtered cookie recipe dataset and a small baking knowledge base. Clear data access and source information are included in:

```text
DATA_ACCESS.md
```

## Learning Outcomes

This project helped me practice:

- Building a focused single-agent system
- Using LangChain tools
- Connecting retrieval to an LLM agent
- Creating a small RAG pipeline
- Designing custom Python tools
- Testing real user scenarios
- Debugging a Gradio interface
- Writing GitHub documentation for a working AI project

## Deep Learning Connection

This project connects to several ITAI 2376 topics:

### NLP and Sequence Modeling

The agent works with recipe text and user instructions, so it depends on language understanding.

### Transformers and Attention

The LLM must understand context across ingredients, recipe instructions, and user constraints.

### Embeddings and RAG

Recipes and baking knowledge are converted into embeddings and retrieved through a vector database.

### AI Agents and Tool Use

The system uses a single-agent workflow where the agent interprets the request, chooses tools, observes results, and produces a final response.

## Known Limitations

The current version works best with self-contained prompts where the user includes the full recipe or request in one message. It is intentionally limited to cookie recipes only. Substitution guidance is practical but not perfect because real baking results can vary based on ingredient brands, oven behavior, dough temperature, and measuring accuracy.

## Reflection

The full final reflection is available in the project repository:

```text
REFLECTION.md
```

In the reflection, I explained what worked well, what I had to fix during testing, why I stayed with a single-agent design, and what I would build next if I had another semester.

## Notes About Repository Organization

This ITAI 2376 portfolio repository does not duplicate the full final project files because the final project already has its own complete public repository. This folder provides a clear summary and direct link to the full implementation.
