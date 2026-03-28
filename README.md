# trec-tot-retrieval
IR project using TREC 2024 Tip-of-the-Tongue dataset. It includes EDA, preprocessing, and retrieval models with BM25, SBERT and MonoT5.

The dataset used in this project is the TREC 2024 Tip-of-the-Tongue dataset.

- During development, query and qrel files were loaded from local zip files.
- For the final repository, large raw files are not stored directly.
- The corpus is NOT stored in this repository due to its large size (~3M documents).

Instead, the corpus is loaded using the `ir_datasets` library:

```python
import ir_datasets
dataset = ir_datasets.load("trec-tot/2024")
