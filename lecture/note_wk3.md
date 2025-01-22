# Week 3 Notebook from Lecture

## 1 AI Approach
### 1.1 okenization
Tool: **NLTK**

### 1.2 Context-Free-Grammar (CFG)
Only check the grammar not the meaning inside it.

### 1.3 WordNet 
Dictionary

**lesk** - a algorithm

## 2 ML Approach
### 2.1 Bag of Words (BoW)
using kind of an array. In the example, the array shows the number of the words showing in the sentence.

*Matrix Representation*<br>
"basketball is a team sport where we shoot a basketball",<br>
"football is a team sport where we score goals"

|   | basketball | football | goals |  is  | score | shoot | sport | team |  we  | where |
|:-:|:---------:|:--------:|:-----:|:----:|:-----:|:-----:|:-----:|:----:|:----:|:-----:|
| 0 |     2     |     0    |   0   |   1  |   0   |   1   |   1   |   1  |   1  |   1   |
| 1 |     0     |     1    |   1   |   1  |   1   |   0   |   1   |   1  |   1  |   1   |

### 2.2 Extract unique words
### 2.3 Removing Stopwords
### 2.4 Stemming and Lemmatization
#### Comparison Table: Stemming vs. Lemmatization

| Feature       | Stemming  | Lemmatization  |
|--------------|:----------:|:---------------:|
| **Method**   | Heuristic rules (removes suffixes) | Dictionary-based (uses linguistic rules) |
| **Speed**    | Faster | Slower |
| **Accuracy** | Lower (may produce non-words) | Higher (always a valid word) |
| **Context**  | Ignores word meaning | Considers word meaning |
| **Example**  | "Happily" → "happili" | "Happily" → "happy" |
| **Example**  | "Better" → "better" | "Better" → "good" |

### 2.5 Bow Extension (N-Grams)
### 2.6 TF-IDF (Term Frequency - Inverse Document Frequency)
#### 1. Introduction
**TF-IDF** is a statistical measure used in **Natural Language Processing (NLP)** and **Information Retrieval** to evaluate how **important** a word is in a document relative to a collection of documents (corpus).

---

#### 2. TF-IDF Formula
The TF-IDF score is calculated as:

$\text{TF-IDF}(t, d) = \text{TF}(t, d) \times \text{IDF}(t)$

Where:
- **TF (Term Frequency)**: Measures how frequently a term `t` appears in a document `d`.

$
\text{TF}(t, d) = \frac{\text{Number of times } t \text{ appears in } d}{\text{Total words in } d}
$

- **IDF (Inverse Document Frequency)**: Measures how important a term is across all documents.

$
\text{IDF}(t) = \log \left( \frac{N}{\text{DF}(t)} \right)
$

  Where:
  - `N` = Total number of documents
  - `DF(t)` = Number of documents that contain term `t`

---


