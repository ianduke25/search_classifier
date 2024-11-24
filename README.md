
# ACLU Police Search Transcript Classifier

This repository contains resources for the ACLU project aimed at classifying transcripts that contain police searches. The project includes a model training notebook, a pre-trained model (Test Set Accuracy: 88% | Precision: 45% | Recall: 83%), and labeled data used for training. 

## Presentation
Information about model training and performance was presented to ACLU attorneys in May, 2024. The presentation can be found here: [https://docs.google.com/presentation/d/1loyEmG-KriFtHOBHD2x-RyCTEJal65KX2RSz9zjXKR0/edit?usp=sharing](https://docs.google.com/presentation/d/1R0gg6ssnXQd461zMOuv7qex55wx8SIudQlDcGeh8zMw/edit?usp=sharing)

## Repository Contents

1. **embedding_and_training.ipynb**: This Jupyter notebook contains the code for embedding the transcripts and training the classification model.
2. **best_random_forest_model.pkl**: This file contains the pre-trained Random Forest model, which has been optimized for classifying police search-related transcripts.
3. **search_labels.csv**: This CSV file contains the labeled data used for training the model. Each transcript is labeled as either containing a police search or not.

## Setup Instructions

### Prerequisites

To run the notebook and use the model, you will need the following:
- Python 3.7+
- Jupyter Notebook
- Required Python packages (listed in `embedding_and_training.ipynb`)

### Installation

1. Clone this repository to your local machine:
   ```bash
   git clone https://github.com/ia/ACLU-police-search-classifier.git
   ```
2. Navigate to the project directory:
   ```bash
   cd ACLU-police-search-classifier
   ```
3. Install the required Python packages:
   ```bash
   pip install -r requirements.txt
   ```

### Running the Notebook

1. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
2. Open `embedding_and_training.ipynb` in Jupyter Notebook.
3. Follow the steps in the notebook to understand the data preprocessing, embedding, and model training processes.

### Using the Pre-Trained Model

The pre-trained model (`best_random_forest_model.pkl`) can be loaded and used to classify new transcripts. Here is an example of how to use the model:

```python
import pickle

# Load the pre-trained model
with open('best_random_forest_model.pkl', 'rb') as file:
    model = pickle.load(file)

# Load new transcripts and preprocess them as shown in the notebook
# ...

# Predict using the model
predictions = model.predict(new_transcripts)
```

## Data

The `search_labels.csv` file contains labeled data used for training the model. It includes two columns:
- `transcript`: The text of the transcript.
- `label`: The label indicating whether the transcript contains a police search (1) or not (0).
