# Style Over Substance 📚

This is the GitHub repository for the **Style Over Substance** project. We aim to uncover content bias in LLM-based AES (Automated Essay Scoring) systems.

This is related to how stylistic attributes such as stance, sentiment, and formality affect scores given by these systems. This repository includes tagged datasets (PERSUADE 2.0 - English and CAES - Spanish), counterfactual essays, evaluation results, and fine‑tuning experiments for both corpora. Everything is implemented in Python using Jupyter Notebooks for each task/module.

## Features ✨
- **Dataset Tagging** – Annotate essays with stance, formality, and sentiment labels for both corpora.
- **Counterfactual Generation** – Create style‑flipped essays using classifiers to ensure attribute validity.
- **Evaluation** – Score original and counterfactual texts against rubric metrics and store results under counterfactuals_scored/
- **Data Analysis** – Examine raw and scored data in notebooks.
- **Fine‑tuning Experiments** – Local and Colab notebooks for model fine‑tuning and QWK comparison of baseline vs. tuned models.

## Directory Structure 📁

```
caes/ & persuade/         Cleaned and tagged corpus CSVs
counterfactuals/          Generated counterfactual essays
counterfactuals_scored/   Counterfactuals scored by multiple LLMs
checkpoints/              Finetuned model checkpoints and evaluation summaries
plots/                    Figures produced during analysis
*.ipynb                   Jupyter notebooks for tagging, generation, evaluation, analysis, and fine-tuning
requirements.txt          Python dependencies
```

## Getting Started 🚀
1. Install Dependencies. Tested on Python 3.13.

```
pip install -r requirements.txt
```

Required libraries include datasets, torch, transformers, peft, and common data‑science packages

2. Explore Notebooks
   
Launch Jupyter, VS Code or PyCharm and open the notebooks in the project root. The first markdown cell in each notebook describes its purpose and expected data locations. The notebooks are separated by dataset, as indicated in their name ('persuade' or 'caes).

## Data 📊
- *caes/* and *persuade/* contain cleaned_*.csv and tagged_*.csv files.
- *counterfactuals/* provides style‑flipped essays for each attribute direction (e.g., formality_informal_to_formal.csv).
- *counterfactuals_scored/* stores LLM‑scored versions for DeepSeek R1 (8B), Gemma 3 (12B), LLaMA 3 (8B), and Qwen 3 (8B).

## License 📄
This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

<p align="center">This project was made with academical purposes. J.A Ibarra. 2025</p>
