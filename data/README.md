# Data

The raw TREC 2024 Tip-of-the-Tongue dataset is not stored in this repository due to its large size.

The document corpus is automatically loaded through `ir_datasets`:

```python
import ir_datasets
dataset = ir_datasets.load("trec-tot/2024")
```
The train, validation, and test split files are automatically downloaded from the official Zenodo release during notebook execution.

Source:
https://zenodo.org/records/13370657
