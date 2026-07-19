# Model Training

This folder contains the deep learning experimentation for the vehicle damage
classifier.

- `damage_prediction.ipynb` - loads the dataset, tries four model architectures
  (a custom CNN, a regularized CNN, EfficientNet-B0 transfer learning, and ResNet50
  transfer learning), evaluates each with a confusion matrix, and saves the
  best-performing model.
- `hyperparameter_tunning.ipynb` - uses Optuna to search for the best learning rate
  and dropout rate for the winning ResNet50 architecture.
- `saved_model.pth` - the final trained weights (ResNet50, ~80% validation accuracy).

### Dataset
Not included in this repo (too large). Expected structure locally:
dataset/F_Breakage, F_Crushed, F_Normal, R_Breakage, R_Crushed, R_Normal
