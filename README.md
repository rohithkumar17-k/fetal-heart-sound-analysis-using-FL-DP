# Heart Sound Analysis using Federated Learning and Differential Privacy

A research/learning project exploring heart sound classification with a deep-learning pipeline and a privacy-aware federated-learning workflow.

## Project overview

The downloadable project package contains two notebooks:

1. **`01_HeartSound_Project.ipynb`** — the initial heart-sound classification workflow.
2. **`02_HeartSound_FL_DP.ipynb`** — the federated-learning and differential-privacy workflow.

Download `Heart-Sound-FL-DP-GitHub-Ready.zip` from this repository and extract it to get the complete folder structure. The notebooks are the primary source of truth for the implemented methods. Before reporting performance or privacy claims, rerun the notebooks and record the resulting metrics and privacy accountant output.

## Workflow at a glance

- Load and prepare heart-sound recordings/features.
- Train/evaluate the baseline classification model.
- Partition training data across federated clients.
- Train local client models and aggregate model parameters using Federated Averaging (FedAvg).
- Explore differential privacy during training and evaluate the resulting model.

> **Important:** Federated learning and differential privacy do not automatically guarantee that a deployed system is clinically validated or that all privacy risks are eliminated. Treat this as an experimental project, not a medical diagnostic tool.

## Run in Google Colab

1. Download and extract the project ZIP, then upload/open a notebook in Google Colab.
2. Select **Runtime → Change runtime type** and choose a GPU if your experiment benefits from it.
3. Make the dataset available in the runtime. If using Google Drive, mount it and update the dataset paths in the notebook's setup/data-loading cells.
4. Install dependencies from `requirements.txt`, then add any notebook-specific package versions required by your runtime.
5. Run cells from top to bottom.
6. Save final metrics and privacy-accounting results in `results/` or in the notebook.

## Dataset

The dataset is **not included** in this repository. Add the dataset source, license/terms, and exact preparation instructions here before publishing the repository. Do not upload restricted, private, or very large raw recordings without checking the dataset's redistribution terms.

## Results

No performance numbers are hard-coded in this README. Run the notebooks and add measured results here, including test-set metrics, split protocol and class distribution, federated client count and communication rounds, and the differential-privacy configuration and computed privacy budget (epsilon and delta), if successfully calculated.

## Reproducibility and limitations

- Dataset paths and package versions may need to be adjusted for your environment.
- Results can vary with random seeds, dataset splits, hardware, and package versions.
- Privacy parameters such as clipping norm, noise multiplier, and delta should be reported alongside the computed privacy budget.
- This repository is an educational/research prototype and is not intended for clinical use.

## License

A license has not yet been selected. Add a license only after confirming that you have the right to license your own code and that the dataset's license is compatible with your intended use.
