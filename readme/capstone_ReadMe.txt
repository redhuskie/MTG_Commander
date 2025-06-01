MTG Commander Data Analysis

This project explores data from Magic: The Gathering (MTG), specifically focusing on **Commander-legal cards**. Using card attribute data, we analyze what makes certain commanders more popular using metrics like `edhrecRank`, and apply machine learning tools such as SHAP for interpretability.

Project Goals

- Clean and prepare a dataset of MTG Commander-legal cards
- Impute missing `edhrecRank` values using a Random Forest regression model
- Perform exploratory data analysis on card features (color identity, mana value, keyword abilities, etc.)
- Use SHAP (SHapley Additive exPlanations) to identify which features most influence popularity
- Build an interpretable model to understand Commander deck-building trends

#Tech Stack

- **Python** 3.10
- **Pandas**, **NumPy** – data wrangling
- **Scikit-learn** – modeling & imputation
- **SHAP** – model interpretability
- **Matplotlib**, **Seaborn** – data visualization
- **Jupyter Notebook** – interactive development

Data Cleaning Highlights

- Converted text-based card features to structured boolean flags (e.g., `has_draw`, `has_lifelink`)
- Calculated derived metrics like `color_count` and `mana_complexity`
- Identified and filled missing `edhrecRank` values using a trained regression model

#Machine Learning

A **Random Forest Regressor** was trained using features like:
- `manaValue`
- `color_count`
- `has_draw`, `has_ramp`, `has_destroy`, etc.

Missing `edhrecRank` values were predicted and imputed for cards with complete feature sets.

SHAP Analysis

SHAP values were used to:
- Visualize which features contributed most to a commander's popularity
- Quantify the impact of mana cost, color identity, and mechanics on rank