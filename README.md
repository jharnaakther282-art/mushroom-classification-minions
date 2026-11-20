# Mushroom Edibility Classification

Team Minions (Team 14), CSE 12th Batch, CCN University of Science and Technology

This project classifies mushrooms as edible or poisonous using three
classifiers: Naive Bayes, Decision Tree, and Random Forest.

## Team Members
- Sameya Karim (111223082)
- Khadija Akter Akhi (111223044)
- Aysha Akter Sathi (111223072)

## Dataset
- Name: Mushroom Dataset (UCI Machine Learning Repository)
- Link: https://archive.ics.uci.edu/dataset/73/mushroom
- DOI: https://doi.org/10.24432/C5959T
- Size: 8,124 records, 22 categorical features (21 used after removing `veil-type`)
- Target: edible (e) or poisonous (p)

## Files
- `Mushroom_2.ipynb`: the notebook with all code and outputs
- `Minions_Mushroom_Classification_Paper.pdf`: the project paper

## Method (summary)
- Checked duplicates (none) and missing values (`stalk-root`, kept as a separate category)
- One-hot encoding (116 binary columns); encoder fitted on the training data only
- Stratified 80:20 train-test split, `random_state = 42`
- Metrics: accuracy, precision, recall, F1-score, confusion matrix, 5-fold stratified cross-validation

## Results (test set, 1,625 samples)
| Model | Test accuracy |
|---|---|
| Naive Bayes | 93.29% |
| Decision Tree | 100% |
| Random Forest | 100% |

Naive Bayes predicted 96 poisonous mushrooms as edible.

## How to run
1. Open the notebook in Google Colab.
2. Choose Runtime > Restart session and run all.
3. The dataset is downloaded automatically with the `ucimlrepo` package.

## Note
This is a classroom project. The models must not be used to decide
whether a wild mushroom is safe to eat.
