# trec-tot-retrieval
IR project using TREC 2024 Tip-of-the-Tongue dataset. It includes EDA, preprocessing, and retrieval models with BM25, SBERT and MonoT5.

The dataset used in this project is the TREC 2024 Tip-of-the-Tongue dataset.

- Queries and qrels are loaded from local files.
- The corpus is NOT stored in this repository due to its large size (~3M documents).

Instead, the corpus is loaded using the `ir_datasets` library:

```python
import ir_datasets
dataset = ir_datasets.load("trec-tot/2024")
