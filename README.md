# Linear Regression From Scratch (Gradient Descent)

Multivariate linear regression trained with **batch gradient descent**, implemented from scratch in NumPy. It predicts **item-outlet sales** on a retail dataset.

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?logo=jupyter&logoColor=white)

## What's inside

- **Data cleaning and EDA:** histograms, category distributions, and missing-value imputation.
- **Custom `gradient_descent` class:** `fit`, `pred` and `compute_cost` (MSE cost), with a configurable learning rate and iteration count.
- **Feature scaling study:** min-max vs. z-score vs. no normalisation.
- **Evaluation:** MAE, MSE, RMSE and R².

## Results

| Scaling   | MAE   | RMSE   | R²    |
|-----------|-------|--------|-------|
| Min-max   | 863.9 | 1157.6 | 0.560 |
| Z-score   | 863.6 | 1158.5 | 0.559 |
| None      | diverges (cost → ∞) | – | – |

**Takeaway:** without feature scaling, gradient descent diverges on this data. Either scaling method makes it converge to roughly the same solution.

## Run it

```bash
pip install -r requirements.txt
jupyter notebook "Linear Regression.ipynb"
```

> The notebook expects the dataset as `dataset.csv` in the repo root (a BigMart-style retail sales dataset). The original file isn't redistributed here, but every cell's output is saved in the notebook.

## License

[MIT](LICENSE)
