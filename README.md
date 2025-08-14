# Iris Species Classification with K-Nearest Neighbors (KNN)

This project implements a K-Nearest Neighbors (KNN) classifier to predict the species of an iris flower based on its sepal and petal measurements. It serves as a practical example of implementing a distance-based machine learning algorithm, including the critical steps of feature scaling and hyperparameter tuning.

---

## The Dataset

The project uses the classic **Iris dataset**, which contains measurements for 150 iris flowers from three different species:
- Iris-setosa
- Iris-versicolor
- Iris-virginica

The features included are `SepalLengthCm`, `SepalWidthCm`, `PetalLengthCm`, and `PetalWidthCm`.

---

## Project Workflow

### 1. Data Preprocessing
- **Data Loading**: The `Iris.csv` dataset was loaded and the unnecessary 'Id' column was removed.
- **Encoding**: The categorical target variable 'Species' was converted into a numerical format using `LabelEncoder`.
- **Feature Scaling**: As KNN is a distance-based algorithm, all features were normalized using `StandardScaler`. This ensures that each feature contributes equally to the distance calculations.

### 2. Hyperparameter Tuning (Finding the Best K)
A key part of the KNN algorithm is choosing the number of neighbors (K).
- **Experimentation**: The model was trained and evaluated for K values ranging from 1 to 25.
- **Optimal K**: By plotting the accuracy against each K value, we determined that **K=9** provided the best performance on our test set, achieving an accuracy of approximately **96%**.

### 3. Model Evaluation
The final model (with K=9) was evaluated using a confusion matrix, which confirmed its high accuracy and showed only two minor misclassifications on the test data.

### 4. Decision Boundary Visualization
To better understand how the model makes its decisions, we visualized its decision boundaries in 2D space.
- **Comparison**: We plotted the boundaries for both a **K=1** model (which showed high variance and overfitting) and our optimal **K=9** model (which showed a much smoother, more generalized boundary). This visually demonstrates the importance of choosing a good K value.

---

## How to Run the Code
1. Ensure you have Python and Jupyter Notebook installed.
2. Clone this repository to your local machine.
3. Install the required libraries:
   ```bash
   pip install pandas numpy scikit-learn matplotlib seaborn
