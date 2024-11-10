# K-Nearest Neighbors (KNN) Implementation

This repository contains a custom implementation of the K-Nearest Neighbors (KNN) algorithm, written in Python. This code does not use the KNN model from `scikit-learn`, as it demonstrates building the model from scratch, but it uses other libraries for efficiency and convenience in handling arrays and distances.

## Features
- Calculates Euclidean distances manually
- Finds the `k` nearest neighbors and predicts labels based on majority voting
- Can be used with normalized data for consistent distance calculation

## Libraries Used

### NumPy
![NumPy Logo](https://upload.wikimedia.org/wikipedia/commons/3/31/NumPy_logo_2020.svg)
- **Purpose**: We use `numpy` for efficient array operations and mathematical calculations. 
- **Where Used**:
  - `np.array`: Converts lists to arrays for faster computations.
  - `np.partition`: Finds the smallest distances in `k` nearest neighbors selection.
  - `np.bincount`: Counts occurrences of labels to determine the most common label in the nearest neighbors.
  - `np.sqrt` and `np.sum`: Calculate Euclidean distances in the `calc_distance` function.

### Scikit-learn (Optional)
- **Purpose**: If desired, `scikit-learn` can be used to validate our custom KNN model by comparing its predictions to those of the library's KNN model.
- **Where Used**: This project doesn't use `scikit-learn`'s KNN, but if you'd like to compare or use other utilities, install `scikit-learn` as an optional dependency.

## Code Structure

- **`knn_predict`**: Main function that predicts the labels for the test data based on training data.
- **`calc_distance`**: Calculates Euclidean distance between two data points.
- **`nearest_labels`**: Finds indices of the `k` smallest distances.
- **`most_comman_label`**: Determines the most frequent label among `k` nearest neighbors.
- **`normalize`**: Normalizes data to a 0-1 range for more consistent distance calculations.

## Installation

To install the necessary dependencies:

```bash
pip install numpy
