 
# Explainable Credit Scoring Project

## Overview
This project uses machine learning to predict and analyze loan risks. By employing interpertable techniques, we extract insights from loan data and implement segment analysis to identify loan segments with a high proportion of bad loans. The goal is to aid financial institutions in better understanding and managing loan risk.

## Features
- **Loan Risk Prediction**: Predicts the risk associated with loans using a decision tree classifier.
- **Segment Analysis**: Analyzes different segments of loan data to find the proportion of bad loans, helping pinpoint higher-risk categories.
- **Visualization**: Provides visualization of the decision tree for a better understanding of the model's decision paths.

## Getting Started

### Prerequisites
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Graphviz for visualization

### Installation
1. **Clone the repository**
   ```bash
   git clone https://github.com/zgcharaf/XAI-CREDIT-SCORING
   cd loan-risk-analysis
   ```

2. **Set up a Python virtual environment (optional)**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install the required packages**
   ```bash
   pip install -r requirements.txt
   ```

### Usage
1. **Prepare your dataset**: Ensure your dataset is in a CSV format and follows the expected schema, make sure to modify the configuration.pql file accordingly. 

2. **Run the analysis**: Execute the main script to train the model and perform segment analysis.
   ```bash
   python main.py
   ```

3. **View the results**: Check the output files or terminal output for the analysis results and visualizations.

## Documentation
Please refer to the folder Documentation.

## Contact
- **Project Link**: [https://github.com/zgcharaf/XAI-CREDIT-SCORING/)
- **Maintainer**: zgcharaf@gmail.com





