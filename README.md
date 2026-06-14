# MDA5013 Deep Learning for Data Science — Assessment 2.2

This repository contains the codebase, evaluation assets, and the final compiled research report for **Assessment 2.2: Evaluating the Efficacy of RNN, LSTM, and GRU Models for Time Series Prediction** under the `MDA5013` module.

The project models sequential bike rental counts (the target variable `cnt` in `DATA/day.csv`) based on historical environmental covariates, seasons, and social calendar markers using three deep recurrent architectures implemented in TensorFlow (Keras): **SimpleRNN**, **LSTM**, and **GRU**.

---

## 📂 File Structure

```text
.
├── DATA/
│   ├── day.csv             # Daily bike rental dataset (731 records)
│   └── hour.csv            # Hourly bike rental dataset (unused in current sequence)
├── RESOURCES/
│   ├── mda5013-assessment2-2-brief.md  # Official assessment brief & rubric
├── assessment_2-2.ipynb    # Primary Jupyter Notebook containing EDA, preprocessing, models, and visualizations
├── comparison_full_line_plot.png    # Line plot comparing predictions vs actual on the full test set (102 days)
├── comparison_zoom_line_plot.png    # Zoomed temporal view of tracking (first 30 test days)
├── comparison_scatter_plots.png     # Scatter plots with regression lines and lines of perfect agreement (y=x)
├── comparison_metrics_bar.png       # Side-by-side benchmarking bar charts of error scales (RMSE, MAE) and R² coefficients
├── pyproject.toml          # Declarative package dependencies list
├── uv.lock                 # Standard lockfile for hermetic environment reproduction
└── README.md               # Repository documentation and setup instructions (this file)
```

---

## 🛠️ Requirements & Installation

This project has been configured and lock-managed for Python `>=3.12`. It requires TensorFlow, Scikit-Learn, Pandas, NumPy, Matplotlib, Seaborn, and python-docx.

### Option A: Using `uv` (Recommended & Deterministic)
If you have [uv](https://github.com/astral-sh/uv) installed, you can initialize the isolated environment and run the notebook with perfect reproducibility:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/izzaziii/mda5013-assessment2-2-08052342.git
   cd mda5013-assessment2-2-08052342
   ```

2. **Initialize and sync the virtual environment:**
   This reads `uv.lock` and sets up everything automatically:
   ```bash
   uv sync
   ```

3. **Launch the Jupyter Notebook server:**
   ```bash
   uv run jupyter notebook
   ```

---

### Option B: Using Standard `pip` and `venv`
If you do not use `uv`, you can spin up a standard Python virtual environment:

1. **Clone the repository:**
   ```bash
   git clone https://github.com/izzaziii/mda5013-assessment2-2-08052342.git
   cd mda5013-assessment2-2-08052342
   ```

2. **Create a virtual environment:**
   ```bash
   python3 -m venv .venv
   source .venv/bin/activate
   ```

3. **Install dependencies:**
   ```bash
   pip install --upgrade pip
   pip install ipykernel tensorflow scikit-learn pandas seaborn matplotlib python-docx
   ```

4. **Launch the Jupyter Notebook server:**
   ```bash
   jupyter notebook
   ```
