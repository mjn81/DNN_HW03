# Self-Organizing Maps (SOM) for Dimensionality Reduction and Clustering

This repository contains an implementation of **Self-Organizing Maps (SOMs)** using Python, based on the **Human Activity Recognition Using Smartphones** dataset. The project is designed to explore dimensionality reduction and clustering techniques using neural networks.

## 📌 Project Overview

This project is part of an **Artificial Intelligence and Deep Learning** course and aims to:

- Reduce the dimensionality of high-dimensional data using **Self-Organizing Maps (SOMs)**.
- Cluster data points and visualize them in a lower-dimensional space.
- Evaluate the performance of the SOM network in terms of clustering accuracy and neuron activation.

The implementation follows the steps outlined in the coursework instructions.

## 📂 Repository Structure

```
├── Q1.ipynb                 # Jupyter Notebook containing the implementation
├── dataset/                 # Directory for the dataset (downloaded automatically)
├── README.md                # This README file
run the project
```

## 📊 Dataset: Human Activity Recognition (HAR)

We use the **UCI Human Activity Recognition Using Smartphones** dataset, which contains sensor measurements from smartphones collected while subjects performed activities like walking, sitting, and running. The dataset consists of:

- **Features:** Accelerometer and gyroscope measurements with high-dimensional input space.
- **Labels:** Activity categories such as walking, standing, sitting, etc.

### 📥 Dataset Download

The dataset is automatically downloaded and extracted when the notebook is executed. The script follows these steps:

1. Download the dataset from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones).
2. Extract the data.
3. Load training and test sets for processing.

## 🚀 Implementation Details

### 🧩 Step 1: Data Preprocessing
- Load and extract the dataset.
- Merge the training and test data.
- Display dataset statistics.

### 🧩 Step 2: Self-Organizing Maps (SOM) Implementation
We implement a **2D Self-Organizing Map (SOM)** using NumPy, following these steps:

1. **Initialize the SOM** with random weight vectors.
2. **Find the Best Matching Unit (BMU)** for each input vector.
3. **Update the weights** of the BMU and its neighbors using:
   - Learning rate decay
   - Neighborhood function (linear, Gaussian)
4. **Repeat for multiple epochs** to optimize the network.

### 🧩 Step 3: Experiments and Analysis

We conduct several experiments to analyze different parameters affecting the SOM network:

1. **Effect of Network Size:** We compare SOM grids of different sizes, e.g., `5×5`, `10×10`.
2. **Effect of Neighborhood Function:** We experiment with linear and Gaussian neighborhood functions.
3. **Impact of Learning Rate and Radius Decay:** We analyze the effect of decreasing these parameters over training iterations.
4. **Visualization of Clustered Data:** We project the high-dimensional data into a 2D representation.

## 📈 Results & Analysis

- The **reduced representation of high-dimensional data** is plotted for better understanding.
- The number of **dead neurons** (neurons that never activate) is visualized over training epochs.
- **Clustering results** are visualized using different colors to distinguish groups.

## 🔧 Installation & Usage

### Prerequisites
Ensure you have Python installed. You can set up the required dependencies using:

```bash
pip install numpy pandas matplotlib scikit-learn
```

### Running the Notebook
1. Open the Jupyter Notebook:

   ```bash
   jupyter notebook Q1.ipynb
   ```

2. Execute the cells step by step.

## 🏆 Contributors

- **Instructor:** Dr. Safabakhsh
- **Student:** Mohammad Javad Najafi
- **Institution:** Amirkabir University of Technology
