# Digit Recognition with Multilayer Perceptron (MLP)

This project trains a Multilayer Perceptron (MLP) model to recognize handwritten digits from the MNIST dataset. The dataset contains grayscale images of digits (0-9) represented as 28x28 pixel matrices. The model processes these images to classify the digits accurately.

## Dataset

The dataset used in this project is sourced from Kaggle and can be found at the following link: [Kaggle](https://www.kaggle.com/datasets/oddrationale/mnist-in-csv).

The dataset contains two CSV files:
- **mnist_train.csv**: Training data with 60,000 rows and 785 columns.
- **mnist_test.csv**: Test data with 10,000 rows and 785 columns.

### Dataset Description

- **Label**: The digit depicted in the image (0-9).
- **Pixel Columns (Pixel0 to Pixel783)**: Each column represents the intensity of a pixel, with values ranging from 0 (black) to 255 (white). These columns flatten the 28x28 matrix into a 784-dimensional feature vector.

### Dataset Location

- **Data/**: Contains the dataset files downloaded and unzipped from Kaggle.
- **Notebook/**: Contains Jupyter notebooks for data preprocessing and model training. **Currently, we are working within the Notebook directory.**

## Project Structure

The project is organized as follows:

```plaintext
Digit-Recognition/
├── Data/
│   ├── mnist_train.csv
│   └── mnist_test.csv
├── Notebook/
│   └── [Jupyter notebooks for analysis and training]
└── README.md
```

## Data Preprocessing

- **Data Visualization**: Sample images are visualized to understand pixel intensity patterns.
- **Feature Scaling**: Features are standardized using `StandardScaler` for optimal model performance.
- **Train-Test Split**: Training and testing sets are prepared for supervised learning.

## Model Training

An MLP model from the scikit-learn library is trained with the following architecture:
- **Hidden Layers**: Two layers with 100 and 50 neurons, respectively.
- **Activation Function**: ReLU.
- **Maximum Iterations**: 300.
- **Early Stopping**: Enabled for better generalization.

## Model Performance

The MLP model achieved the following F1-scores:
- **Training Set**: 0.9977
- **Test Set**: 0.9742

## Requirements

To run this project, ensure the following Python libraries are installed:
- `pandas`
- `matplotlib`
- `scikit-learn`
- `kaggle`
