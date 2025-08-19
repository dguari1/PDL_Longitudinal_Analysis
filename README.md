# PDL Longitudinal Analysis

A longitudinal analysis repository for Parkinson's Disease (PDL) motor assessment data, focusing on finger tapping and hand movement tasks.

## Overview

This repository contains datasets and analysis tools for studying the progression of motor symptoms in Parkinson's Disease patients over time. The data includes detailed kinematic measurements from finger tapping (FT) and hand movement (HM) tasks, along with clinical assessments including UPDRS-III scores.

This respository includes code to reproduce the results included in our paper related to the changes in certain motor symptoms with time in Parkinson's disease. 

There are 4 measures per participant, including right and left hands, and at two time points about 24 months appart. 
The analysis was performed using Liner Mixed Effect models. 

## Dataset Description

The repository includes two main longitudinal datasets:

### 1. Finger Tapping Data (`Data_FT_longitudinal.csv`)
- **Task**: Finger tapping movements
- **Measurements**: Video derived kinematic features obtained from VisionMD (www.VisionMD.ai)
- **Clinical Data**: UPDRS-III scores, bradykinesia ratings, disease duration

### 2. Hand Movement Data (`Data_HM_longitudinal.csv`)
- **Task**: General hand movements
- **Measurements**: Similar kinematic parameters as finger tapping
- **Clinical Data**: Corresponding clinical assessments

### Data Features

Both datasets contain the following key variables:

#### Demographics & Clinical
- `Subject_ID`: Unique participant identifier
- `Age`: Participant age (years)
- `Sex`: Biological sex (0=Female, 1=Male)
- `Handedness`: Dominant hand (0=Left, 1=Right)
- `Visit`: Study visit number
- `Time`: Time from baseline (months)
- `UPDRS_III`: Unified Parkinson's Disease Rating Scale Part III score
- `Bradykinesia`: Bradykinesia subscore
- `Item_Score`: Specific item score
- `DiseaseDuration`: Current disease duration (months)
- `BaselineDiseaseDuration`: Disease duration at baseline (moths)
- `BaselineDiseaseSeverity`: Baseline UPDRS III score

#### Kinematic Measurements
These features are devired from VisionMD

https://www.nature.com/articles/s41531-025-00876-6
https://www.nature.com/articles/s41531-025-00999-w
https://www.nature.com/articles/s41531-025-01082-0


- **Amplitude**: `MeanAmplitude`, `StdAmplitude`, `CVAmplitude`
- **Speed**: `MeanSpeed`, `StdSpeed`, `CVSpeed`
- **Velocity**: `MeanRMSVelocity`, `StdRMSVelocity`, `CVRMSVelocity`
- **Opening/Closing**: Opening and closing speed metrics with statistics
- **Timing**: `MeanCycleDuration`, `StdCycleDuration`, `CVCycleDuration`
- **Frequency**: Movement frequency
- **Decay**: `AmplitudeDecay`, `VelocityDecay`
- **Movement Quality**: `NumberofPauses`, `numberofHesitations`


## Getting Started

### Prerequisites

To work with this data, you'll need:
- Python 3.7+
- Jupyter Notebook or JupyterLab
- Common data science libraries (pandas, numpy, matplotlib, seaborn, scipy)

### Installation

1. Clone this repository:
```bash
git clone https://github.com/dguari1/PDL_Longitudinal_Analysis.git
cd PDL_Longitudinal_Analysis
```

2. Install required dependencies:
```bash
pip install pandas numpy matplotlib seaborn scipy jupyter
```

3. Launch Jupyter Notebook:
```bash
jupyter notebook DataAnalysis.ipynb
```

## Usage

The `DataAnalysis.ipynb` notebook provides a framework for analyzing the longitudinal data. You can:

1. Load and explore the datasets
2. Perform descriptive statistics
3. Visualize temporal trends
4. Conduct longitudinal modeling
5. Compare finger tapping vs. hand movement metrics

## Data Format

The CSV files are structured with one row per subject per visit per hand, allowing for:
- Longitudinal tracking of individual subjects
- Bilateral comparison (left vs. right hand)
- Multi-visit progression analysis

## Research Applications

This dataset can be used for:
- **Longitudinal Analysis**: Tracking motor symptom progression over time
- **Digital Biomarkers**: Developing objective measures of motor function
- **Machine Learning**: Building predictive models for disease progression
- **Clinical Research**: Validating digital assessments against clinical scales

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Citation

If you use this dataset in your research, please cite:

```
@dataset{guarin2025pdl,
  author = {Diego L. Guarin},
  title = {PDL Longitudinal Analysis Dataset},
  year = {2025},
  url = {https://github.com/dguari1/PDL_Longitudinal_Analysis}
}
```

## Contact

For questions or collaborations, please contact:
- Diego L. Guarin - [@dguari1](https://github.com/dguari1)

## Acknowledgments

- Participants who contributed to this longitudinal study
- Clinical research teams involved in data collection
- Open source community for analysis tools and frameworks