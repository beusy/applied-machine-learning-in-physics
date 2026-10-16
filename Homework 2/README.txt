PHYS 2550 — HOMEWORK 2

Files
PHYS_2550_Homework2.ipynb: executed notebook, organised by assignment question.
report/PHYS2550_Homework2_Report.pdf: final 16-page report.
report/main.tex and report/figures/: editable LaTeX source and figures.
results/: measurements, predictions, splits, histories and hardware record.
checkpoints/: best-validation model weights from the completed GPU run.
requirements.txt: dependencies for local review or a fresh CUDA environment.
GPU_RUN_INSTRUCTIONS.txt: how to reproduce the experiment.

Completed experiment
Nine baseline models and two scrambled models ran on the same Tesla T4 GPU.
The notebook includes shifted-crop and bonus B2 added-noise evaluations.
Its 38 remaining code cells preserve the completed outputs. The report uses
these GPU results. Three seeds share a test set; their standard deviations
measure training variability, not uncertainty from sampling new galaxies.

Dataset
The original Galaxy10 SDSS file is about 200 MB and is not stored in Git.
The notebook downloads it automatically, or download it from:
https://zenodo.org/records/10844811/files/Galaxy10.h5
Place Galaxy10.h5 alongside the notebook for local saved-result review.
Documentation: https://astronn.readthedocs.io/en/latest/galaxy10sdss.html
SHA-256: 969a6b1cefcc36e09fffa86febd2f699a4aa19b837ba0427f01b0bc6ded458af

Run or review
Open the notebook from this folder in Jupyter to review saved results on CPU.
In Colab, select a GPU runtime and run all cells for a new experiment; retain
Colab's CUDA-compatible PyTorch installation. New runs use separate folders.
Colab notebook:
https://colab.research.google.com/drive/1IhZVrHby1eqb0qL0XkNx7c4TMkqqj1jG
The repository notebook is an alternative for viewing the saved outputs.

Report
Compile main.tex from report/ using pdfLaTeX, or upload report/ to Overleaf.
The source retains Homework 1's font, margins, title and caption styling.
