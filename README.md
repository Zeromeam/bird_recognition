# Bird Recognition from Sound

A notebook-based audio-classification project for identifying bird species from
recordings. The work focuses on representation and evaluation: different views
of the same signal expose different information, and class imbalance makes plain
accuracy a poor summary.

## Representation

Each recording is transformed into three complementary feature families:

- Mel spectrograms for time-frequency energy
- MFCC views for compact spectral-envelope information
- engineered acoustic features for additional signal descriptors

The final multi-input neural network processes these families in parallel. Mel
and MFCC tensors enter separate 2D convolutional branches; engineered features
enter a 1D convolutional branch. The branch representations are concatenated and
passed to the final classifier.

![Multi-input network architecture](https://github.com/Zeromeam/bird_recognition/assets/102630502/9b58d543-7e69-4dc7-b44e-b0e8fd87edad)

## Evaluation

The dataset is imbalanced, so model comparison uses macro-averaged F1: F1 is
computed independently for each species and every species contributes equally to
the final average. This makes failure on a less common class visible instead of
allowing common classes to dominate the score.

The notebooks compare feed-forward, convolutional, recurrent, and multi-input
architectures using cross-validation. Executed outputs preserve the feature
views, training curves, and macro-F1 figures.

![Macro-F1 across training](https://github.com/Zeromeam/bird_recognition/assets/102630502/adde2334-8189-4191-bf57-d0581c81dcc9)

## Repository map

- cv/cross_validation.ipynb — exploratory feature analysis and model comparison
- cv/final.ipynb — final multi-branch experiment and recorded outputs

## Reproduction

The original audio/features are not bundled. Reproduction requires restoring the
dataset paths expected by the notebooks and installing their imported Python
packages, including PyTorch, NumPy, pandas, scikit-learn, and Matplotlib. Run the
feature preparation before the cross-validation and final-model cells.

## Limitations

- No trustworthy raw-audio sample or deployable trained model is retained in the
  repository, so there is no live species predictor.
- Notebook outputs document the experiment, but a clean environment lockfile and
  one-command pipeline were not preserved.
- Macro-F1 exposes imbalance better than accuracy, but a full deployment review
  would also inspect per-class precision/recall, confusion patterns, calibration,
  and performance on recordings from new conditions.

Explore the synchronized feature atlas in the
[portfolio case study](https://medoali.at/work/bird-recognition).
