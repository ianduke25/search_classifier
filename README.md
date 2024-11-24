
# ACLU Police Search Transcript Classifier

This repository contains resources for the ACLU project aimed at classifying transcripts that contain police searches.

## Repository Contents

1. **embedding_and_training.ipynb**: A Jupyter notebook containing the code for embedding the transcripts and training the classification model.

## Data Requirements

The attached notebook requires a `search_labels.csv` file containing labeled data used for training the model. It should include two columns:
- `File`: The filename of the bodycam file
- `Search?`: A binary label indicating whether the transcript contains a police search (1) or not (0).
