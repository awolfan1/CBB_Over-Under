# College Basketball Total Points Prediction

This project uses machine learning models to predict the total points scored in NCAA college basketball games. The prediction models are trained on team statistics such as offensive rating, defensive rating, pace, average points scored, and average points allowed. The project utilizes regression techniques, including Ridge, Lasso, ElasticNet, and Random Forest.

## Features

- Predicts total points scored between two teams.
- Supports multiple regression models:
  - Ridge Regression
  - Lasso Regression
  - ElasticNet Regression
  - Random Forest Regressor
- Scales features using `StandardScaler` to normalize inputs.
- Implements cross-validation using Leave-One-Out (LOO) to estimate model performance.

## Installation

To run the project, make sure you have the following packages installed:

```bash
pip install pandas numpy scikit-learn
```

## Usage

1. Clone the repository:

   ```bash
   git clone https://github.com/yourusername/college-basketball-prediction.git
   cd college-basketball-prediction
   ```

2. Run the Jupyter Notebook:

   ```bash
   jupyter notebook basketball_totalpoints.ipynb
   ```

3. Adjust the team statistics in the code cells to predict outcomes for different matchups.

## Data

The data used for predictions is collected from [Basketball Reference](https://www.basketball-reference.com) and [KenPom](https://kenpom.com). The following features are used for each team:

- **Offensive Rating (`off_rtg`)**: Points scored per 100 possessions.
- **Defensive Rating (`def_rtg`)**: Points allowed per 100 possessions.
- **Pace**: Number of possessions per game.
- **Average Points Scored (`avg_scored`)**: Points scored per game.
- **Average Points Allowed (`avg_allowed`)**: Points allowed per game.

## Models and Evaluation

### Models Used:
- **Ridge Regression**: Uses L2 regularization to minimize overfitting.
- **Lasso Regression**: Uses L1 regularization for feature selection.
- **ElasticNet Regression**: Combines L1 and L2 regularization.
- **Random Forest Regressor**: An ensemble method to capture complex patterns.

### Performance Metrics:
- **Mean Squared Error (MSE)** is calculated for model evaluation.
- **Leave-One-Out Cross-Validation (LOO)** is used for model validation.

## Results

The project predicts total points for selected games using different models and prints the predicted values. In several cases, the model demonstrated value on the over compared to the Vegas over/under spread. For example:

- **Georgia Tech vs. Duke**: Predicted total points exceeded the Vegas over/under of **143.5**.
- **UNC Wilmington vs. Delaware**: Predicted total points exceeded the Vegas over/under of **147.5**.
- **St. Joe's vs. George Mason**: Predicted total points exceeded the Vegas over/under of **132.5**.

These predictions highlight potential opportunities to exploit discrepancies between model outputs and betting lines. The coefficients from each model and the predicted total points are displayed as output.

## Future Improvements

- Integrate advanced feature engineering using historical data.
- Implement model comparison metrics to choose the best-performing algorithm.
- Automate data collection from public NCAA stats databases.
- Experiment with additional regression models, such as XGBoost or neural networks.

## Contributing

Contributions are welcome! Please feel free to open issues or submit pull requests.

