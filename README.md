# EXXA Notebooks

Notebook repository for equivariant vision experiments in EXXA.

It includes two main workflows:

- `exxa_general_image.ipynb`: training and evaluation on general image data.
- `exxa_sequential.ipynb`: sequential workflow with support for real and synthetic data.

## Repository Contents

```text
.
├── exxa_general_image.ipynb
├── exxa_sequential.ipynb
├── requirements.txt
├── continuum_data_subset/
│   └── continuum_data_subset/*.fits
├── outputs_general_image/
│   ├── models/
│   └── plots/
└── outputs_sequential_image/
	 ├── models/
	 └── plots/
```

## Requirements

- Python 3.10+ recommended.
- Linux/macOS (on Windows, use PowerShell or WSL).

Quick setup:

```bash
python -m venv .venv
source .venv/bin/activate
python -m pip install --upgrade pip
pip install -r requirements.txt
```

## Data

The repository already includes a FITS subset:

- `continuum_data_subset/continuum_data_subset/*.fits`

With this subset, you can run the notebooks without downloading additional datasets.

## How To Run

1. Activate the virtual environment:

	```bash
	source .venv/bin/activate
	```

2. Start Jupyter:

	```bash
	jupyter notebook
	```

3. Run cells from top to bottom in one of these notebooks:

	- `exxa_general_image.ipynb`
	- `exxa_sequential.ipynb`

## Outputs

Each notebook writes results to dedicated folders:

- General workflow: `outputs_general_image/models/` and `outputs_general_image/plots/`
- Sequential workflow: `outputs_sequential_image/models/` and `outputs_sequential_image/plots/`

Versioning note:

- `.gitignore` is configured to ignore generated outputs, checkpoints, and large model artifacts.
- It is recommended to version only code/notebooks and, if needed, a small curated sample of final figures.

## Main Dependencies

Dependencies listed in `requirements.txt` include:

- `torch`
- `astropy`
- `lightkurve`
- `scikit-learn`
- `pytorch-msssim`
- Scientific stack (`numpy`, `scipy`, `pandas`, `matplotlib`)

## Quick Troubleshooting

- If Jupyter does not detect your environment, reinstall the kernel:

  ```bash
  pip install ipykernel
  python -m ipykernel install --user --name exxa-notebooks
  ```

- If `lightkurve` fails due to connectivity, the sequential notebook can continue in synthetic mode.

## Reproducibility

For consistent results:

- Keep dependency versions fixed via `requirements.txt`.
- Run each notebook in order without skipping cells.
- Clear old outputs if you want to compare runs from a clean state.
