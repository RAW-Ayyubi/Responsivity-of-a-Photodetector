# Model Card for Extra Trees Regressor Model for Predicting Photodetector Responsivity

## Model Summary
This model predicts the responsivity (A/W) of photodetectors based on a variety of input features including active layer properties, substrate bandgap, experimental conditions, and device architecture. The model is built using the Extra Trees Regressor (ETR), selected for its high accuracy and stability across different input dimensions.

## Model Details

### Model Description
The Extra Trees Regressor is an ensemble learning method based on a large number of randomized decision trees. It is used here to learn complex relationships between material, device, and experimental features and their corresponding responsivity values. The implementation uses the `ExtraTreesRegressor` class from the `scikit-learn` Python library (v1.2+), with the following key hyperparameters:

- **n_estimators:** 510 (number of trees in the forest)
- **max_depth:** 18 (maximum depth of each tree)
- **random_state:** 100 (for reproducibility)

- **Implemented by:** Abdul Wahab Ayyubi
- **Developed by:** Scikit-learn contributors (https://scikit-learn.org/)
- **Model type:** Tree-based ensemble regressor (Extra Trees Regressor)
- **License:** MIT License

### Model Sources
- **Repository:** https://github.com/ayyubi/Responsivity-of-a-Photodetector

## Uses

### Direct Use
The model can be used to predict photodetector responsivity from input features in device design and material screening workflows.

### Out-of-Scope Use
This model should not be used for photodetectors based on unknown or non-standard materials or conditions significantly different from those represented in the training data.

## Bias, Risks, and Limitations
The model is trained on data extracted from 29 experimental studies. Any inherent bias in the published data (e.g., preference for reporting high-performing devices) may be reflected in the model. The model may also underperform on device architectures or material systems not represented in the training data.

### Recommendations
Use caution when applying the model to extrapolate beyond the material systems, device types, or experimental conditions represented in the original dataset.

## How to Get Started with the Model
Clone the GitHub repository and run the notebook `Responsivity_Pred.ipynb` after updating the path to `InputData.csv`. Ensure you have the required Python libraries installed as listed in the environment setup.

## Training Details

### Training Data
The model was trained on a custom dataset of 1927 data points derived from 29 experimental studies, complemented by theoretical data from the Materials Project and NIST database.

### Preprocessing
Highly correlated features were removed using Pearson correlation analysis. No standardization or normalization was applied as Extra Trees is insensitive to scaling.

### Training Hyperparameters
The model was trained with the following parameters:
- `n_estimators=510`
- `max_depth=18`
- `random_state=100`

### Speeds, Sizes, Times
Model training and evaluation takes approximately 7–10 minutes on a local Intel i5 CPU with 8 GB RAM.

## Evaluation

### Testing Data
The dataset was split randomly into 70% training and 30% testing sets. No independent external dataset was used.

### Metrics
The model was evaluated using Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), and R-squared (R²).

### Results
Extra Trees Regressor outperformed other tested models (Random Forest, Decision Tree, XGBoost, LightGBM, CatBoost, SGBoost) based on all three metrics and testing plots.

On the test set, the Extra Trees Regressor achieved:
- **MAE:** 0.0728 A/W
- **RMSE:** 0.2726 A/W
- **R²:** 0.99995
These results demonstrate extremely high accuracy and reliability in predicting photodetector responsivity.

## Model Examination
Feature dependence and importance plots were generated to interpret the model's behavior and identify key influencing factors.

## Environmental Impact
- **Hardware Type:** Local machine (Intel i5-1135G7, 8 GB RAM)
- **Hours used:** ~0.2 hours
- **Cloud Provider:** None
- **Carbon Emitted:** Estimated to be negligible for local, short-duration runs

## Technical Specifications
- **Architecture:** Extra Trees Regressor
- **Software:** Python 3.9+, Jupyter Notebook, scikit-learn, pandas, matplotlib, seaborn

## Citation
**BibTeX:**
```
@misc{ayyubi2025responsivity,
  title={Responsivity-of-a-Photodetector},
  author={Abdul Wahab Ayyubi},
  year={2025},
  howpublished={\url{https://github.com/ayyubi/Responsivity-of-a-Photodetector}}
}
```

## Model Card Contact
For questions or support, please contact [abdulayyubi@gmail.com](mailto:abdulayyubi@gmail.com)

