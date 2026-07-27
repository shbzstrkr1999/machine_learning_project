# 🌸 Iris Flower Classification

A machine learning project that classifies Iris flowers into one of three species — **Setosa**, **Versicolor**, and **Virginica** — based on their sepal and petal measurements.

## 📋 Overview

This project uses the classic [Iris dataset](https://archive.ics.uci.edu/dataset/53/iris) to build and evaluate a supervised classification model. It's a great beginner-friendly project for learning the end-to-end ML workflow: data loading, exploration, preprocessing, model training, and evaluation.

## 📊 Dataset

The Iris dataset contains 150 samples with the following features:

| Feature        | Description                  |
|-----------------|-------------------------------|
| Sepal Length    | Length of the sepal (cm)     |
| Sepal Width     | Width of the sepal (cm)      |
| Petal Length    | Length of the petal (cm)     |
| Petal Width     | Width of the petal (cm)      |
| Species (target)| Setosa, Versicolor, Virginica |

## 🛠️ Tech Stack

- Python 3.x
- pandas / numpy — data handling
- scikit-learn — model training & evaluation
- matplotlib / seaborn — data visualization
- Jupyter Notebook (optional, for exploration)

## 📁 Project Structure

```
iris-flower-classification/
├── data/
│   └── iris.csv
├── notebooks/
│   └── exploration.ipynb
├── src/
│   ├── train.py
│   ├── predict.py
│   └── utils.py
├── models/
│   └── model.pkl
├── requirements.txt
└── README.md
```

## 🚀 Getting Started

### 1. Clone the repository
```bash
git clone https://github.com/your-username/iris-flower-classification.git
cd iris-flower-classification
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Train the model
```bash
python src/train.py
```

### 4. Make predictions
```bash
python src/predict.py --sepal_length 5.1 --sepal_width 3.5 --petal_length 1.4 --petal_width 0.2
```

## 🤖 Model

The project experiments with several classification algorithms, including:

- Logistic Regression
- K-Nearest Neighbors (KNN)
- Decision Tree
- Support Vector Machine (SVM)
- Random Forest

Model performance is evaluated using accuracy, precision, recall, and a confusion matrix.

## 📈 Results

| Model               | Accuracy |
|---------------------|----------|
| Logistic Regression | ~97%     |
| KNN                  | ~96%     |
| SVM                  | ~97%     |
| Random Forest         | ~96%     |

*(Update this table with your actual results.)*

## 📄 License

This project is licensed under the MIT License.

## 🙌 Acknowledgments

- Iris dataset originally introduced by Ronald A. Fisher (1936)
- UCI Machine Learning Repository
