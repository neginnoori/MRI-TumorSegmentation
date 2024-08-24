# Brain Tumor Segmentation using Graph Cut 
## Overview

This project focuses on the segmentation of brain tumors from MRI images using advanced machine learning techniques, specifically the Graph Cut algorithm combined with a Genetic Algorithm for optimization. The primary objective is to accurately segment brain tumors in MRI scans, which is crucial for treatment planning and diagnosis in medical applications.

## Dataset

The dataset used for this project is the "LGG Segmentation Dataset" available on Kaggle, which consists of MRI images of lower-grade glioma (LGG) brain tumors. The dataset contains MRI scans in various modalities along with the corresponding tumor masks.

- **Kaggle Dataset:** [LGG MRI Segmentation](https://www.kaggle.com/datasets/mateuszbuda/lgg-mri-segmentation)
- **Download Command:**  
  ```bash
  kaggle datasets download -d mateuszbuda/lgg-mri-segmentation
  ```
  
## Installation

To set up the project, please follow the steps below:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/brain-tumor-segmentation.git
   cd brain-tumor-segmentation
   ```

2. **Install Required Dependencies**
   Ensure you have Python installed (preferably Python 3.8 or above). Install the necessary Python packages using pip:

   ```bash
   pip install -r requirements.txt
   ```

   The `requirements.txt` file should include the following libraries:
   - numpy
   - pandas
   - scikit-learn
   - scikit-image
   - matplotlib
   - tensorflow or pytorch (depending on your choice for neural network frameworks)
   - opencv-python
   - kaggle (to download datasets directly from Kaggle)

3. **Download the Dataset**
   Download the dataset from Kaggle and extract it into the `data/` directory.

   ```bash
   kaggle datasets download -d mateuszbuda/lgg-mri-segmentation -p data/
   unzip data/lgg-mri-segmentation.zip -d data/
   ```

## Usage

To run the tumor segmentation process, execute the Jupyter Notebook provided in the repository:

1. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook brain_genetic_programming.ipynb
   ```

2. **Run the Notebook Cells**
   Follow the notebook instructions to preprocess the data, train the model, and visualize the results. The notebook will guide you through:

   - Data Preprocessing: Loading and normalizing MRI images.
   - Tumor Segmentation: Using the Graph Cut algorithm to perform initial segmentation.
   - Optimization: Applying a Genetic Algorithm to optimize the segmentation mask.

3. **Evaluate the Model**
   Use the provided evaluation metrics in the notebook to assess the performance of the segmentation.

## Project Structure

```
brain-tumor-segmentation/
│
├── data/                               # Folder to store the dataset
│   └── lgg-mri-segmentation/           # Extracted MRI images and masks
│
├── brain_genetic_programming.ipynb     # Jupyter Notebook for segmentation and optimization
├── requirements.txt                    # Python dependencies
├── README.md                           # Project README file
└── LICENSE                             # License file (optional)
```

## Algorithms

### 1. Graph Cut Algorithm

Graph Cut is an optimization-based segmentation algorithm used in image processing. It models the segmentation task as a graph problem where each pixel is represented as a node, and edges represent the similarity between adjacent pixels. The algorithm finds the minimum cut that separates the graph into two disjoint sets, ideally corresponding to the object and background.

### 2. Genetic Algorithm

The Genetic Algorithm (GA) is a search heuristic that mimics the process of natural selection to find optimal or near-optimal solutions to complex problems. In this project, GA is used to optimize the parameters of the segmentation model, improving the accuracy of the tumor segmentation results.

## Results

The performance of the segmentation model is evaluated using standard metrics such as Dice coefficient, Jaccard index, and pixel-wise accuracy. The results indicate a significant improvement in segmentation quality using the combination of Graph Cut and Genetic Algorithm over traditional methods.

## Contributing

Contributions to the project are welcome! If you have any suggestions, bug reports, or feature requests, please open an issue or submit a pull request. 

