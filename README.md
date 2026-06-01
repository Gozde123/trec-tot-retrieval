# trec-tot-retrieval
IR project using TREC 2024 Tip-of-the-Tongue dataset. It includes EDA, preprocessing, and retrieval models with BM25, SBERT and MonoT5.

The dataset used in this project is the TREC 2024 Tip-of-the-Tongue dataset.

- For the final repository, large raw files are not stored directly.
- The corpus is NOT stored in this repository due to its large size (~3M documents).

Instead, the corpus is loaded using the `ir_datasets` library:


## Installation

Install dependencies:

```bash
pip install -r requirements.txt

```

Running the Project
- Open the notebook in the src/ folder and run all cells.
-On the first run:
* The corpus will be automatically downloaded via ir_datasets
* The train/dev/test splits will be automatically downloaded from Zenodo

Data Access
- This project uses the official TREC ToT 2024 dataset.

Corpus
-The full document corpus (~3M documents) is not stored in this repository due to its size.
-It is loaded automatically via:

```bash
import ir_datasets
dataset = ir_datasets.load("trec-tot/2024")
```

- Train / Validation / Test Splits
- The following files are automatically downloaded inside the notebook:
train-2024.zip
dev1-2024.zip (validation set)
dev2-2024.zip (test set)
Source (official release):
https://zenodo.org/records/13370657
- The repository does NOT contain any raw dataset files.


## Models
- BM25
- SBERT
- BGE-M3
- MonoT5
- BGE-Reranker

## Evaluation Metrics
- nDCG@10
- nDCG@100
- nDCG@1000
- Recall@10
- Recall@100
- Recall@500
- Recall@1000

## Additional Analyses
- Wilcoxon Statistical Significance Test
- Rank Shift Analysis
- Error Analysis
- Candidate Recall Analysis
- Win/Loss Analysis
- UMAP Visualization


* ## Report
The project proposal report is available in `reports/project_proposal_report.pdf`.

# W&B Reports

The complete experiment logs, hyperparameter sweeps, evaluation results, statistical analyses, and visualizations are available through the following Weights & Biases reports.

## Interim Reports

* **Interim Report 1**
  https://wandb.ai/gozdenur104-metu-middle-east-technical-university/trec-tot-hybrid-final/reports/Untitled-Report--VmlldzoxNjgyNTg4MQ?accessToken=85ivuatu4dzwikdqv8a70oleogsv67z1k5u31hakg7xh0wg87ladjc6cn3hbnn2r

* **Interim Report 2**
  https://wandb.ai/gozdenur104-metu-middle-east-technical-university/trec-tot-interim/reports/Interim-Report-2--VmlldzoxNjgyNTkxMg?accessToken=5beoinygj9k0qremz4p3ngn03qu8vb8h904bzon5wb9qxd0knr1ui7uwt1qo2vx6

## Final Reports

* **Final Tables Report**
  https://wandb.ai/e250231-odt-teknokent/trec-tot-final/reports/Final-Tables-Report--VmlldzoxNzA1NjAxMA?accessToken=8cy7yb1rcwqboa63wr4rnnajq0flxt834h5gjveqm79upvb47m23khpdrp8hf755

* **Final Plots Report**
  https://wandb.ai/e250231-odt-teknokent/trec-tot-hybrid-final/reports/-Final-Plots-Report--VmlldzoxNzA1NjI3NQ?accessToken=7pnb0v3mwcp6f0ptr45yuycy6dfcexwtmx9j7z8u853m2wb08432a1olihbnp5gv

These reports contain all experimental results, statistical significance tests, interpretability analyses, visualizations, and benchmark comparisons presented in this project.


## Reproducibility

To reproduce the experiments:

1. Install the required packages from `requirements.txt`.
2. Build the PyTerrier index.
3. Run the notebook cells sequentially.
4. Evaluate retrieval performance using nDCG and Recall metrics.
5. Compare systems using the Wilcoxon signed-rank test.
6. Review the W&B reports for the complete experimental history.

Random seeds were fixed to ensure reproducibility whenever possible.

## docstring

set_reproducibility(): Sets random seeds for reproducible experiments.
normalize_per_query(): Normalizes retrieval scores using min-max scaling.
build_dense_run(): Generates dense retrieval rankings from BM25 candidates.
build_cross_encoder_run(): Produces reranked results using cross-encoder models.
build_monot5_run(): Produces reranked results using the MonoT5 reranker.


