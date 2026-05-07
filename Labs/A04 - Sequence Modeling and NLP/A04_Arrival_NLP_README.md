# A04 — Analyzing *Arrival* Through the Lens of NLP

## Overview

This folder contains a written analysis paper for **ITAI 2376: Deep Learning**. The paper connects the film *Arrival* to Natural Language Processing concepts, especially translation, ambiguity, preprocessing, contextual meaning, and the risks of misinterpretation.

This is a written paper, not a coding lab or software project.

## File Included

```text
A04_Group8_NicoleMarcial_ITAI2376.pdf
```

## Assignment Topic

The paper analyzes how *Arrival* represents language understanding and communication challenges. The film follows Dr. Louise Banks as she works to interpret an alien language and prevent global conflict caused by mistranslation.

The main example discussed in the paper is the alien phrase translated as:

```text
offer weapon
```

The paper explains how this phrase creates panic because it is ambiguous and lacks enough context. This connects directly to NLP problems where literal translation is not enough to determine meaning.

## Main NLP Concepts Discussed

### Machine Translation

The paper connects the alien language translation problem to machine translation. It explains that translation systems can struggle when vocabulary, tone, and meaning shift across specialized domains such as military intelligence or healthcare.

### Text Preprocessing

The paper compares Dr. Louise’s process of identifying repeated alien symbols to preprocessing steps used in NLP, such as:

- text cleaning
- tokenization
- normalization
- lemmatization
- structuring raw language data

### Tokenization and Feature Engineering

Dr. Louise separates repeated alien symbols into identifiable units and looks for shared patterns. This is compared to tokenization and feature engineering, where text is broken into smaller pieces and meaningful patterns are extracted.

### Corpus Building

As more alien messages are collected, Dr. Louise builds something similar to a corpus. In NLP, a corpus is a collection of text used for analysis or model training.

### TF-IDF

The paper connects Dr. Louise’s pattern tracking to TF-IDF. TF-IDF helps identify which words or symbols are important because of how often they appear in specific contexts compared with general usage.

### Ambiguity and Word Sense Disambiguation

The phrase “offer weapon” is used as an example of ambiguity. The paper explains that the word “weapon” could mean a literal weapon or a tool, depending on context. This connects to word sense disambiguation and contextual modeling.

### Contextual Embeddings

The paper explains why modern NLP models need contextual understanding rather than isolated word counts. Contextual embeddings help models represent meaning based on surrounding words and usage.

### Part-of-Speech Tagging and Dependency Parsing

The phrase “offer weapon” is structurally unclear. The paper connects this problem to part-of-speech tagging and syntactic dependency parsing, which help determine how words function and relate to each other in a sentence.

### Sentiment Analysis

The paper explains that a sentiment analyzer might classify “offer weapon” as negative, even if the aliens’ intent is not hostile. This shows how sentiment analysis can fail when it lacks context or domain adaptation.

### Named Entity Recognition

The paper connects Dr. Louise writing “HUMAN” and pointing to herself to Named Entity Recognition. This is treated as a kind of entity mapping between a label and a real-world referent.

### Multi-Class Classification

The international response to the alien message is compared to multi-class classification. Different countries classify the same message differently, such as threat, warning, cooperation, or uncertainty.

## Key Takeaway

The main takeaway of the paper is that language understanding requires more than translating words directly. Accurate interpretation depends on structure, intent, context, domain knowledge, and careful analysis.

The paper shows that NLP systems, like humans in the film, can make serious mistakes when they do not have enough context.

## Course Connection

This paper connects to the language-focused parts of ITAI 2376, especially:

- Module 04: NLP and sequence modeling
- Module 05: Transformers and attention
- Later agent topics involving language understanding, reasoning, and user intent

Although this paper was not a coding assignment, it helped connect course concepts to a real-world communication problem shown through film.

## Notes About Authorship

This was a group written assignment by:

```text
Nicole Marcial
Aima Ayaz
```

The paper was submitted for ITAI 2376 with Professor Patricia McManus.

## Sources Referenced in the Paper

- ITAI 2373 Modules 1–13 PowerPoints by Professor Anna Rachapudi
- *Arrival*. Directed by Denis Villeneuve. Paramount Pictures, 2016.
