# AtliQo Bank Credit Card Hypothesis Testing Project

## Description
This project conducts an A/B testing analysis for AtliQo Bank to evaluate the impact of a specific intervention (e.g., a new product, promotion, or UI change) on customer transaction behavior. Built using Python, the project employs statistical techniques to compare average transaction amounts between a test group and a control group, utilizing z-tests and confidence intervals to determine statistical significance. Visualizations with Seaborn and Matplotlib provide insights into transaction patterns. The project aligns with data science practices for hypothesis testing, suitable for informing business decisions in the banking sector.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Features](#features)
- [Analysis Details](#analysis-details)
- [Contributing](#contributing)
- [Contact](#contact)

## Installation
Follow these steps to set up the project locally:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/atliqo-bank-hypothesis-testing.git
   ```
2. **Navigate to the Project Directory**:
   ```bash
   cd atliqo-bank-hypothesis-testing
   ```
3. **Create a Virtual Environment**:
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```
4. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```
   Required packages:
   - pandas
   - numpy
   - seaborn
   - matplotlib
   - scipy

5. **Ensure Dataset Availability**:
   Place the dataset (e.g., `transactions.csv`) in the `data/` folder. The dataset should include columns like `test_group_avg_tran` and `control_group_avg_tran`.

## Usage
To explore the hypothesis testing analysis:

1. **Run the Jupyter Notebook**:
   - Open `AtliQo Bank Project Phase 1 & 2.ipynb` in Jupyter Notebook to review data loading, statistical analysis, and visualizations.
   - Execute the notebook to perform the z-test and calculate confidence intervals for the test group’s transaction amounts.
   - Example output: 95% confidence interval for the test group’s mean transaction amount is approximately (226.86, 245.11).

2. **Visualize Results**:
   - The notebook generates plots (e.g., histograms, boxplots) to compare transaction distributions between test and control groups.

### Example
```python
# Example z-test in the notebook
from scipy import stats as st
z_statistic, p_value = st.ztest(df['test_group_avg_tran'], df['control_group_avg_tran'], alternative='larger')
print(z_statistic, p_value)
```

Output:
- Z-statistic and p-value to determine if the test group’s mean transaction amount is significantly higher than the control group’s.
- Confidence interval: `(226.86, 245.11)` for the test group’s mean transaction amount.

## Project Structure
```
atliqo-bank-hypothesis-testing/
├── data/                                       # Input dataset
│   ├── transactions.csv
├── notebooks/                                  # Jupyter Notebooks for analysis
│   ├── AtliQo Bank Project Phase 1 & 2.ipynb
├── requirements.txt                            # Project dependencies
└── README.md                                   # Project documentation
```

## Features
- **Data Analysis**: Loads and processes transaction data to compare test and control groups.
- **Statistical Testing**: Performs a z-test to evaluate if the test group’s average transaction amount is significantly higher than the control group’s.
- **Confidence Intervals**: Calculates 95% confidence intervals for the test group’s mean transaction amount.
- **Visualizations**: Uses Seaborn and Matplotlib to visualize transaction distributions and patterns.
- **Scalability**: Analysis can be extended to other banking metrics or interventions.

## Analysis Details
- **Methodology**: A/B testing with a z-test to compare mean transaction amounts (`test_group_avg_tran` vs. `control_group_avg_tran`).
- **Features Used**:
  - `test_group_avg_tran`: Average transaction amount for the test group.
  - `control_group_avg_tran`: Average transaction amount for the control group.
- **Statistical Test**:
  - Z-test with alternative hypothesis: Test group mean > control group mean.
  - 95% confidence interval calculated for the test group’s mean, e.g., (226.86, 245.11).
- **Tools**:
  - Python with Pandas for data manipulation, NumPy for numerical operations, Scipy for statistical testing, and Seaborn/Matplotlib for visualizations.
- **Outcome**: Provides statistical evidence to inform AtliQo Bank’s decision on the intervention’s effectiveness.

## Contributing
Contributions are welcome! To contribute:

1. Fork the repository.
2. Create a feature branch:
   ```bash
   git checkout -b feature/your-feature-name
   ```
3. Commit your changes:
   ```bash
   git commit -m "Add your feature description"
   ```
4. Push to the branch:
   ```bash
   git push origin feature/your-feature-name
   ```
5. Open a pull request.

Please follow PEP 8 standards and include tests for new features.

## Contact
For questions or feedback, reach out to:
- Mail ID: kavineshdhanush@gmail.com
