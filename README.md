# Bird Recognition from Sound

A notebook-based audio-classification project for identifying bird species from
recordings. The project compares signal representations and neural network
architectures with an evaluation strategy designed for imbalanced classes.

## Audio representation

Each recording is transformed into three complementary feature families:

- Mel spectrograms for time-frequency energy;
- MFCC representations for compact spectral-envelope information; and
- engineered acoustic features for additional signal descriptors.

The final multi-input neural network processes these feature families in
parallel. Mel and MFCC tensors pass through separate 2D convolutional branches,
while engineered features pass through a 1D convolutional branch. Their learned
representations are concatenated before classification.

![Multi-input network architecture](https://github.com/Zeromeam/bird_recognition/assets/102630502/9b58d543-7e69-4dc7-b44e-b0e8fd87edad)

## Evaluation

The notebooks compare feed-forward, convolutional, recurrent, and multi-input
architectures using cross-validation. Because the dataset is imbalanced, model
comparison uses macro-averaged F1: the F1 score is calculated per species and
then averaged so that each class contributes equally.

Executed notebook outputs include feature views, training curves, and macro-F1
figures for the evaluated models.

![Macro-F1 across training](https://github.com/Zeromeam/bird_recognition/assets/102630502/adde2334-8189-4191-bf57-d0581c81dcc9)

## Repository structure

- `cv/cross_validation.ipynb` — feature analysis and model comparison
- `cv/final.ipynb` — final multi-branch experiment and recorded outputs

## Running the notebooks

1. Install the imported packages, including PyTorch, NumPy, pandas,
   scikit-learn, and Matplotlib.
2. Configure the dataset paths used by the notebooks.
3. Run feature preparation before the cross-validation and final-model sections.

Explore the synchronized feature atlas in the
[portfolio case study](https://medoali.at/work/bird-recognition).
