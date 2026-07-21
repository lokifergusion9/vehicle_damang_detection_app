# Vehicle Damage Detection App

A Proof-of-Concept deep learning system that classifies car photos into 6 damage
categories: Front Normal, Front Breakage, Front Crushed, Rear Normal, Rear Breakage,
Rear Crushed. Built for VROOM Cars

More details added as each part of the project is committed over the next few days.
See `Model_training_CNN/`, `Fast_API_server/`, and `Streamlit_app/`.

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
