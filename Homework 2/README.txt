PHYS 2550 — HOMEWORK 2

Files
PHYS_2550_Homework2.ipynb: executed notebook, organised by assignment question.
report/PHYS2550_Homework2_Report.pdf: report with the original Homework 1 formatting.
report/main.tex and report/figures/: editable LaTeX source and figures.
results/: measurements, predictions, splits, histories and hardware record.
checkpoints/: best-validation model weights from the completed GPU run.
requirements.txt: general dependencies.
requirements-review-lock.txt: exact package versions tested for CPU review.
GPU_RUN_INSTRUCTIONS.txt: how to reproduce the experiment.

Completed experiment
Nine baseline models and two scrambled models ran on the same Tesla T4 GPU.
The notebook includes shifted-crop and bonus B2 added-noise evaluations.
Its 39 code cells have been checked in CPU saved-result review mode.
The model measurements still come from the completed GPU experiment. Three seeds share a test set; their standard deviations
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
Review loads and checks the saved split, scaling, permutation, labels and
predictions. Regenerated plots and summaries go into a dated review_outputs/
folder; the original results and weights are not overwritten.
In Colab, select a GPU runtime and run all cells for a new experiment; retain
Colab's CUDA-compatible PyTorch installation. New runs use separate folders.
Colab notebook:
https://colab.research.google.com/drive/1IhZVrHby1eqb0qL0XkNx7c4TMkqqj1jG
The repository notebook is an alternative for viewing the saved outputs.

Report
Compile main.tex from report/ using pdfLaTeX, or upload report/ to Overleaf.
The source retains Homework 1's font, margins, title and caption styling.

Additional analysis
The border contamination estimate uses 25 flagged and 25 unflagged training
images, sampled with seed 2554. Decisions and notes are in
results/border_visual_review.csv; both labelled contact sheets are in the
notebook and report/figures/. Clear neighbours are visibly separate objects
overlapping the four-pixel border. Uncertain edge features are counted
separately. The weighted estimates are exploratory visual assessments,
not catalogue-confirmed source counts. Bootstrap sampling uncertainty is
conditional on those visual labels.

The aperture-intensity summary distinguishes brightness from SNR.
The FCNN weight-permutation check uses 128 training images and changes no
saved model weights.

Environment
The original training record identifies PyTorch 2.11.0+cu130 and NumPy 2.1.3
on a Tesla T4; a complete package freeze was not captured at that time.
The review requirements describe the tested CPU environment, not the
original GPU environment. Fresh runs now save execution_environment.json
and environment_freeze.txt in their own results directory.
Numerical summaries in the notebook are calculated from the loaded results.
The PDF describes the recorded experiment and must be revised after a new run.
