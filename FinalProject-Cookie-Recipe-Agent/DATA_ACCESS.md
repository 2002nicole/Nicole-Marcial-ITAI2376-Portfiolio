# Data Access — Final Project Cookie Recipe Adaptation Agent

## Full Project Repository

The complete final project repository is available here:

```text
https://github.com/2002nicole/NicoleMarcial_Solo_ITAI2376
```

This file explains the data sources used by the Cookie Recipe Adaptation Agent and how someone can reproduce the data setup.

## Data Sources Used

The project uses two main types of data:

1. A filtered cookie recipe dataset
2. A small baking knowledge base

## 1. Recipe Dataset

### Main Dataset

The project uses the Food.com recipe dataset from Kaggle.

Dataset source:

```text
Food.com Recipes with Ingredients and Tags
https://www.kaggle.com/datasets/realalexanderwei/food-com-recipes-with-ingredients-and-tags
```

### How It Was Used

The full Food.com dataset was filtered to focus on cookie recipes. The filtered recipe data was used to retrieve cookie examples and ingredient patterns.

Relevant recipe information included:

- Recipe name
- Ingredients
- Ingredient quantities
- Recipe steps
- Servings
- Tags

### Should the Full Raw Dataset Be Uploaded to GitHub?

No. The full raw dataset should not be uploaded to GitHub because it is large and comes from Kaggle.

Instead, the repository should include:

- A small sample or cleaned subset if needed
- Clear instructions for accessing the full raw dataset
- Notes explaining how the data was filtered

## 2. Baking Knowledge Base

The project also uses a small cookie baking knowledge base. This knowledge base was manually summarized and paraphrased from baking references.

Main references included:

```text
King Arthur Baking — Cookie chemistry
King Arthur Baking — Egg substitute guidance
King Arthur Baking — Chilling cookie dough
King Arthur Baking — Why cookies spread
```

Reference links:

```text
https://www.kingarthurbaking.com/blog/2016/03/14/cookie-chemistry-2
https://www.kingarthurbaking.com/blog/2021/01/21/guide-for-substituting-eggs-best-egg-replacers
https://www.kingarthurbaking.com/blog/2015/05/17/chilling-cookie-dough
https://www.kingarthurbaking.com/blog/2023/12/19/why-are-my-cookies-spreading
```

### How It Was Used

The baking knowledge base supports substitution and texture explanations.

For example, it helps the agent explain:

- What happens when butter is replaced
- Why egg replacements can change structure
- Why chilling cookie dough affects spread
- Why sugar, fat, flour, and moisture affect cookie texture

## Data Processing Summary

The recipe and baking knowledge data were prepared for retrieval by:

1. Loading recipe and knowledge text
2. Filtering recipe data to cookie-related examples
3. Converting records into LangChain documents
4. Splitting documents into smaller text chunks
5. Creating embeddings with a Hugging Face sentence-transformer model
6. Storing embeddings in Chroma
7. Using a retriever to provide relevant context to the agent

## Embedding Model

The project uses:

```text
sentence-transformers/all-MiniLM-L6-v2
```

This model converts recipe and baking text into embedding vectors so similar recipe questions and guidance can be retrieved.

## Vector Store

The project uses:

```text
Chroma
```

Chroma stores the embedded recipe and baking knowledge chunks locally for retrieval.

## Files to Check in the Full Repository

In the full project repository, check:

```text
data/
agent.ipynb
README.md
```

The `data/` folder contains sample or supporting data files used by the project. The notebook contains the full data loading, filtering, and retrieval setup.

## Reproducibility Instructions

To reproduce the data setup:

1. Download the Food.com recipe dataset from Kaggle.
2. Place the dataset where the notebook expects it, or update the file path.
3. Run the data loading cells in `agent.ipynb`.
4. Filter the dataset to cookie recipes.
5. Build or load the cookie baking knowledge base.
6. Run the document creation and chunking cells.
7. Generate embeddings with the Hugging Face sentence-transformer model.
8. Store the embeddings in Chroma.
9. Run the retrieval tests before using the agent.

## Important Notes

The final project is intentionally limited to cookie recipes. This helps keep the knowledge base focused and makes the agent more reliable than a broad general baking assistant.

Real baking outcomes may still vary based on ingredient brands, measuring accuracy, dough temperature, humidity, oven calibration, and baking time.
