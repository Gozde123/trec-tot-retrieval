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

* ## Report
The project proposal report is available in `reports/project_proposal_report.pdf`.

## W§B for Project:

https://wandb.ai/gozdenur104-metu-middle-east-technical-university/trec-tot-hybrid-final/reports/Untitled-Report--VmlldzoxNjgyNTg4MQ?accessToken=85ivuatu4dzwikdqv8a70oleogsv67z1k5u31hakg7xh0wg87ladjc6cn3hbnn2r


https://wandb.ai/gozdenur104-metu-middle-east-technical-university/trec-tot-interim/reports/Interim-Report-2--VmlldzoxNjgyNTkxMg?accessToken=5beoinygj9k0qremz4p3ngn03qu8vb8h904bzon5wb9qxd0knr1ui7uwt1qo2vx6
