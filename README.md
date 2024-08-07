# Analysis of Reduced Subgenual Cingulate-Dorsolateral Prefrontal Connectivity as an Electrophysiological Marker for Depression


![project overview GIF](https://s10.gifyu.com/images/SDxNl.gif)




This repository contains the code and analysis based on the research study [Reduced subgenual cingulate-dorsolateral prefrontal connectivity as an electrophysiological marker for depression](https://www.researchgate.net/publication/364247301_Reduced_subgenual_cingulate-dorsolateral_prefrontal_connectivity_as_an_electrophysiological_marker_for_depression).

**Note: This is a draft version of the code and analysis. It is currently a work in progress and will be updated in the future, although the script works fine, the preprocessing pipleine can be improved**

## Table of Contents

- [Analysis of Reduced Subgenual Cingulate-Dorsolateral Prefrontal Connectivity as an Electrophysiological Marker for Depression](#analysis-of-reduced-subgenual-cingulate-dorsolateral-prefrontal-connectivity-as-an-electrophysiological-marker-for-depression)
  - [Table of Contents](#table-of-contents)
  - [Introduction](#introduction)
  - [Installation](#installation)
  - [Usage](#usage)
  - [Data](#data)
  - [Analysis](#analysis)
    - [Detailed Analysis Steps](#detailed-analysis-steps)
  - [Results](#results)
    - [Example Outputs](#example-outputs)
  - [Contributing](#contributing)
  - [License](#license)
  - [Acknowledgments](#acknowledgments)

## Introduction

The goal of this project is to reproduce the analysis from the mentioned study, which investigates the electrophysiological connectivity between the subgenual cingulate and the dorsolateral prefrontal cortex as a potential marker for depression using opensource tools.

## Installation

To run the code in this repository, you need to set up a virtual environment using Conda and install the necessary libraries. Follow the steps below to set up your environment:

1. **Clone the repository:**

    ```bash
    git clone https://github.com/zavesone/AEC_sbACC_PFC.git
    cd AEC_sbACC_PFC
    ```

2. **Create and activate the Conda environment:**

    ```bash
    conda create --name eeg_analysis python=3.8
    conda activate eeg_analysis
    ```

3. **Install the required libraries:**

    ```bash
    pip install -r requirements.txt
    ```

4. **Install Jupyter Notebook:**

    ```bash
    conda install -c conda-forge notebook
    ```

## Usage

1. **Set up the file paths:**

    Ensure you have the correct file path for your MEG data file. Modify the `meg_file` variable in the notebook if necessary.

2. **Run the Jupyter Notebook:**

    ```bash
    jupyter notebook
    ```

3. **Open the notebook:**

    In the Jupyter interface, open the provided notebook file `AECsbACC-PFC.ipynb` and execute the cells to perform the analysis.

## Data

The data used in this analysis is obtained from [source of the data]. Ensure you have the appropriate permissions to use the data.

- `data/raw/`: Contains the raw data files.
- `data/processed/`: Contains the processed data files.

## Analysis

The analysis is performed in several steps:

1. **Preprocessing**: Data cleaning and preprocessing.
2. **Feature Extraction**: Extracting relevant features from the preprocessed data.
3. **Connectivity Analysis**: Analyzing the connectivity between brain regions.
4. **Statistical Analysis**: Performing statistical tests to validate findings.

### Detailed Analysis Steps

1. **Load MEG Data**: Load the MEG data from the provided file.
2. **Preprocess the Data**: Filter and downsample the data.
3. **Create Epochs**: Split the continuous data into 10-second epochs.
4. **Compute Noise Covariance Matrix**: Calculate the noise covariance matrix.
5. **Setup Source Space**: Define the source space for source localization.
6. **Compute Head -> MRI Transform**: Estimate the transformation from head space to MRI space.
7. **Compute Forward Solution**: Calculate the forward model.
8. **Compute Inverse Operator**: Generate the inverse operator for source estimation.
9. **Apply Inverse Operator**: Apply the inverse operator to the epochs to obtain source estimates.
10. **Extract Time Series from ROIs**: Extract time series data from specified regions of interest (sgACC and DLPFC).
11. **Compute AEC**: Calculate amplitude envelope correlation between the ROIs.
12. **Visualize Results**: Generate 2D and 3D plots to visualize the connectivity.

## Results

The results of the analysis are summarized in the `results/` directory. This includes:

- Connectivity matrices
- Statistical test results
- Plots and figures

### Example Outputs

- **2D Plot**: `sgACC_DLPFC_connectivity_timeseries.png`
- **3D Plot**: `sgACC_DLPFC_connectivity_3D.png`

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments
Special thanks to the authors of the original study for their inspiring work.
