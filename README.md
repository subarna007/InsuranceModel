# Medical Insurance Cost Prediction

Predicts yearly medical insurance charges from age, sex, BMI, number of children, smoking status
and region, using the insurance dataset (1,338 people).

## What the notebook does

1. Explores the data: smokers pay far more, and charges grow with age and BMI.
2. Encodes sex and smoker as 0/1 and one-hot encodes region.
3. Splits the data 80/20 and compares two models on the held-out test set.

## Result

| Model | Train R² | Test R² | Test MAE |
|---|---|---|---|
| Linear regression | 0.752 | 0.745 | 4,280 |
| Polynomial regression (degree 2) | 0.845 | **0.852** | **2,834** |

The degree-2 model does better because it can capture interactions such as smoking × BMI.

## Run it

```bash
pip install pandas numpy matplotlib seaborn scikit-learn jupyter
jupyter notebook "Insurance Regression Model.ipynb"
```
