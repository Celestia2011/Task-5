# Task-5
# Mushroom Classification with AdaBoost

This project focuses on classifying mushrooms as edible or poisonous using decision stumps and the AdaBoost algorithm. We explore the performance of these models with varying numbers of weak learners.

## Dataset

We use a mushroom dataset with the following attributes:

- cap-diameter
- cap-shape
- gill-attachment
- gill-color
- stem-height
- stem-width
- stem-color
- season
- class (target variable: edible or poisonous)

## Project Structure

```
mushroom-classification/
│
├── data/
│   └── mushrooms.csv
│
├── src/
│   └── mushroom_classification.py
│
├── requirements.txt
│
└── README.md
```

## Requirements

- Python 3.7+
- pandas
- numpy
- scikit-learn

Install the required packages using:

```bash
pip install -r requirements.txt
```

## Methodology

We implement the following steps:

1. Apply a decision stump model (a tree with a single attribute)
2. Apply AdaBoost with 1 weak learner (decision stump)
3. Apply AdaBoost with 2 weak learners
4. Apply AdaBoost with 3 weak learners
5. Apply AdaBoost with 10 weak learners

## Usage

Run the main script:

```bash
python src/mushroom_classification.py
```

## Results

| Model           | Weak Learners | Accuracy |
|-----------------|---------------|----------|
| Decision Stump  | 1             | 0.609050 |
| AdaBoost        | 1             | 0.609050 |
| AdaBoost        | 2             | 0.622837 |
| AdaBoost        | 3             | 0.622837 |
| AdaBoost        | 10            | 0.673637 |

## Key Observations

- The decision stump (baseline) achieved an accuracy of about 60.9%.
- AdaBoost with a single weak learner performed identically to the decision stump.
- Increasing the number of weak learners in AdaBoost improved accuracy.
- The highest accuracy of 67.4% was achieved with 10 weak learners.
- The improvement was most significant when moving from 1 to 2 weak learners.

## Conclusion

AdaBoost with multiple weak learners outperformed a single decision stump in this mushroom classification task. The best performance was achieved with 10 weak learners, demonstrating the advantage of the ensemble method over the base classifier.

## Future Work

- Implement feature engineering or selection techniques
- Experiment with more complex base classifiers
- Try other ensemble methods or advanced algorithms (e.g., Random Forests, Gradient Boosting)
- Collect more data or address potential class imbalance issues

