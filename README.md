# Penguin Gender Predictor 🐧

This repository contains a machine learning model that predicts the gender of a penguin based on its physical characteristics and geographical location. 

## Dataset
The model is trained on the `penguins_size.csv` dataset, which includes the following features:
* **Species:** Adelie, Chinstrap, or Gentoo
* **Island:** Torgersen, Biscoe, or Dream
* **Physical Measurements:** Culmen length (mm), culmen depth (mm), flipper length (mm), and body mass (g)

## Tech Stack
* **Language:** Python
* **Libraries:** `pandas` (data manipulation), `scikit-learn` (machine learning)
* **Environment:** Google Colab / Jupyter Notebook

## Model Details
The project uses a **Logistic Regression** classifier. To ensure high accuracy and stable training, the data pipeline includes:
* **Data Cleaning:** Removal of null values and invalid stray characters.
* **Feature Engineering:** One-hot encoding to convert categorical text variables (species, islands) into numerical binary columns.
* **Feature Scaling:** `StandardScaler` to normalize the wide variance between large variables (body mass) and small variables (millimeter-scale measurements) so the model converges successfully.

## Performance
The trained model achieves an overall accuracy of **~91%** on the test data, demonstrating highly balanced precision and recall (F1-scores of 0.90+) for both male and female classes.

## How to Run
1. Clone this repository to your local machine:
   `git clone <your-repository-url>`
2. Ensure you have the required dependencies installed:
   `pip install pandas scikit-learn`
3. Keep the `penguins_size.csv` dataset in the same directory as your notebook.
4. Run the notebook cells sequentially to load the data, train the scaler and model, and test its accuracy.
