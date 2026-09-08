# Decision-Trees
# Renewable Energy Adoption Prediction 🌱

 A machine learning project that uses a **Decision Tree Classifier** to predict whether renewable energy will be adopted based on factors such as carbon emissions, energy output, renewability, and cost efficiency.

 ## 📌 Project Overview

 This project applies supervised machine learning to predict **renewable energy adoption**.

 The model uses the following features:

 - `carbon_emissions`
- `energy_output`
- `renewability_index`
- `cost_efficiency`

 The target variable is:

 - `adoption` — whether renewable energy is adopted or not.

 A **Decision Tree Classifier** with a maximum depth of 3 is trained and evaluated using a train-test split.

 ## 🛠️ Technologies Used

 - Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Joblib
- Google Colab

 ## 📂 Project Structure

```
Renewable-Energy-Adoption/
│
├── Renewable_Energy_Adoption.csv
├── Renewable_Energy_Adoption_model.pkl
├── dt1.png
├── renewable_energy_adoption.ipynb
└── README.md
```

 ## 📊 Dataset

 The dataset is stored in:

```
Renewable_Energy_Adoption.csv
```

 The model uses four input features:

 | Feature | Description |
| --- | --- |
| `carbon_emissions` | Carbon emission level |
| `energy_output` | Energy produced/output |
| `renewability_index` | Measure of renewable characteristics |
| `cost_efficiency` | Cost efficiency of the energy source |
| `adoption` | Target variable indicating adoption |

 ## 🤖 Machine Learning Model

 A **Decision Tree Classifier** is used:

```
model = DecisionTreeClassifier(
    max_depth=3,
    random_state=42
)
```

 The dataset is divided into:

 - **80% training data**
- **20% testing data**

```
X_train, X_test, y_train, y_test = train_test_split(
    X,
    y,
    test_size=0.2,
    random_state=42
)
```

 ### Decision Tree

  Learn more  ## 📈 Model Evaluation

 The model is evaluated using:

 ### Accuracy

```
accuracy = accuracy_score(y_test, y_pred)
print("Accuracy:", accuracy)
```

 ### Confusion Matrix

 A confusion matrix is generated to compare the actual and predicted adoption classes.

```
conf_matrix = confusion_matrix(y_test, y_pred)
```

 The resulting visualization is saved as:

```
dt1.png
```

 ### Classification Report

 The classification report provides:

 - Precision
- Recall
- F1-score
- Support

```
print(
    classification_report(
        y_test,
        y_pred,
        target_names=['Non-Adoption', 'Adoption']
    )
)
```

 ## 🌳 Decision Tree Visualization

 The trained decision tree is visualized using:

```
plot_tree(
    model,
    feature_names=X.columns,
    class_names=['Non-Adoption', 'Adoption'],
    filled=True,
    rounded=True
)
```

 The visualization is saved as:

```
dt1.png
```

 ## 💾 Saved Model

 The trained model is saved using Joblib:

```
joblib.dump(
    model,
    '/content/Renewable_Energy_Adoption_model.pkl'
)
```

 The saved `.pkl` file can later be loaded without retraining the model:

```
import joblib

model = joblib.load(
    'Renewable_Energy_Adoption_model.pkl'
)
```

 ## 🚀 How to Run

 ### 1\. Clone the repository

```
git clone https://github.com/your-username/Renewable-Energy-Adoption.git
```

 ### 2\. Navigate to the project

```
cd Renewable-Energy-Adoption
```

 ### 3\. Install dependencies

```
pip install pandas numpy scikit-learn matplotlib seaborn joblib
```

 ### 4\. Run the notebook

 Open:

```
renewable_energy_adoption.ipynb
```

 You can run the project using **Google Colab** or **Jupyter Notebook**.

 ## 🔮 Future Improvements

 - Compare Decision Tree with Random Forest, Logistic Regression, and SVM.
- Perform hyperparameter tuning.
- Use cross-validation for more reliable evaluation.
- Add feature importance analysis.
- Handle missing values and outliers.
- Deploy the model as a web application.
- Add an interactive interface for renewable energy adoption predictions.

 ## 📌 Results

 After running the notebook, the following outputs are generated:

 - Predicted adoption values
- Accuracy score
- Confusion matrix
- Classification report
- Decision tree visualization
- Trained `.pkl` model

 > **Note:** The actual accuracy and classification results depend on the contents of `Renewable_Energy_Adoption.csv`.

 ## 👨‍💻 Author

 **Your Name**

 If you are uploading this to GitHub, replace `Your Name` with your name and update the repository URL in the installation section.

 ## 📄 License

 This project is intended for educational and research purposes.
