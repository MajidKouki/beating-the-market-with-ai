# Beating the Market with AI

Analysis of various machine learning models across two stocks to identify the best feature sets and models for real-world usage in finance. The goal of the project is to identify which model is best able to train and test on one stock while maintaining performance when tested on another stock.

---

## Technologies

This project leverages python with the following packages:

* [Pandas](https://github.com/pandas-dev/pandas) - For dataframes and date offsetting.

* [NumPy](https://github.com/numpy/numpy) - For mathematical functions.

* [Matplotlib](https://github.com/matplotlib/matplotlib) - For plotting and plot configuration.

* [Scikit-learn](https://github.com/scikit-learn/scikit-learn) - For preprocessing and various models.

* [TA Lib](https://github.com/mrjbq7/ta-lib) - For technical indicators.

---

## Installation Guide

Before first running the application install the following dependencies:

```python
    pip install pandas
    pip install numpy
    pip install matplotlib
    pip install scikit-learn
    pip install ta-lib
```

Jupyter may be required to view the .ipynb file.

```python
    pip install jupyter
```

---

## Usage

This project is primarily intended for analysis in order to identify ideal machine learning models for algorithmic trading purposes. The code can be modified to work with other data if needed. The ideal usage of this project would be using the final results and analysis to determine the ideal model for other projects and real-world applications. To use this project, ensure all packages are installed and run all to view the results and analysis.

---

## Analysis

The result of testing multiple models with the initial data as well as the box plot of the results can be seen below:

* GaussianNB: 0.900 (0.011)

* SVM: 0.925 (0.016)

* LinearDiscriminantAnalysis: 0.888 (0.020)

* LogisticRegression: 0.929 (0.013)

* DecisionTreeRegressor: 0.935 (0.013)

* KNeighborsClassifier: 0.936 (0.008)

* DecisionTreeClassifier: 0.942 (0.015)

* RandomForestClassifier: 0.954 (0.012)

* ExtraTreesClassifier: 0.960 (0.011)

* AdaBoostClassifier: 0.940 (0.017)

* GradientBoostingClassifier: 0.955 (0.015)

* MLPClassifier: 0.982 (0.007)

<img src="./imgs/Models.jpeg" alt="Models Data Comparison" width="600" height="700">

The top three models chosen were the MLP Classifier, Extra Trees Classifier, and Gradient Boosting Classifier. The three models were trained and tested on Apple stocks with the following results and returns:

Baseline returns - 6.47x

MLP model - 7.36x

<img src="./imgs/aapl-mlp.png" alt="MLP Model - Apple" width="700" height="350">

ETC model - 5.74x

<img src="./imgs/aapl-etc.png" alt="ETC Model - Apple" width="700" height="350">

GBC model - 3.89x

<img src="./imgs/aapl-gbc.png" alt="GBC Model - Apple" width="700" height="350">

The models were then tested on Microsoft without retraining to identify whether the trained model can be used on other stocks and help identify patterns and possible overfitting. The results are as follows:

Baseline returns - 8.1x

MLP model - 2.01x

<img src="./imgs/msft-mlp.png" alt="MLP Model - Microsoft" width="700" height="350">

ETC model - 1.14x

<img src="./imgs/msft-etc.png" alt="ETC Model - Microsoft" width="700" height="350">

GBC model - 1.37x

<img src="./imgs/msft-gbc.png" alt="GBC Model - Microsoft" width="700" height="350">

Various other configurations were tested and it was found that the most likely cause of performance issues was the initial algorithm or indicators used to train the models as there was similarly poor performance with Microsoft prior to using the models. In the future, further testing and optimization of the algorithm used to create signals as well as the indicators used will likely result in a more positive outcome.

---

## Contributors

Brought to you by:
* [Jason](https://github.com/jasonbucks)
* [Justin](https://github.com/jlesieur0)
* [Majid](https://github.com/MajidKouki)
* [Ragini](https://github.com/ragininegi)
* [Souk](https://github.com/SoukP1)

---

## License

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)