# Vaccination Data Analysis and Visualization

## Overview

This repository contains a Jupyter Notebook (`vaccine_impact_analysis_updated.ipynb`) for analyzing and visualizing the impact of vaccine introductions on disease cases, coverage, and incidence rates across countries. The project uses cleaned datasets from sources like the World Health Organization (WHO) to address key questions about vaccine effectiveness, coverage disparities, and disease prevalence. The analysis focuses on diseases such as Hepatitis B, Diphtheria, and Invasive Meningococcal Disease, with data from countries like Aruba and Afghanistan.

The notebook leverages Python with Pandas, Matplotlib, Seaborn, and Scipy to perform statistical analyses and generate visualizations (e.g., box plots, line plots, bar plots, scatter plots). It addresses 10 key questions to understand vaccine impact and identify coverage gaps.

## Objectives

The analysis answers the following questions:
1. Is there a correlation between vaccine introduction and a decrease in disease cases?
2. What is the trend in disease cases before and after vaccination campaigns?
3. Which diseases have shown the most significant reduction in cases due to vaccination?
4. What percentage of the target population has been covered by each vaccine?
5. How does the vaccination schedule (e.g., booster doses) impact target population coverage?
6. Are there significant disparities in vaccine introduction timelines across WHO regions?
7. How does vaccine coverage correlate with disease reduction for specific antigens?
8. Are there specific regions or countries with low coverage despite high availability of vaccines?
9. What are the gaps in coverage for vaccines targeting high-priority diseases (e.g., TB, Hepatitis B)?
10. Are certain diseases more prevalent in specific geographic areas?

## Datasets

The project uses five cleaned datasets (in CSV format):

1. **cleaned_cases.csv**: Disease case counts by country, year, and disease.
   - Columns: `GROUP`, `CODE`, `NAME`, `YEAR`, `DISEASE`, `DISEASE_DESCRIPTION`, `CASES`
   - Example: Aruba, 2023, Invasive Meningococcal Disease, 1 case

2. **cleaned_coverage.csv**: Vaccination coverage data by antigen and country.
   - Columns: `GROUP`, `CODE`, `NAME`, `YEAR`, `ANTIGEN`, `ANTIGEN_DESCRIPTION`, `COVERAGE_CATEGORY`, `COVERAGE_CATEGORY_DESCRIPTION`, `TARGET_NUMBER`, `DOSES`, `COVERAGE`
   - Example: Aruba, 2023, DTPCV3, 95.98% coverage

3. **cleaned_incidence.csv**: Disease incidence rates per population unit.
   - Columns: `GROUP`, `CODE`, `NAME`, `YEAR`, `DISEASE`, `DISEASE_DESCRIPTION`, `DENOMINATOR`, `INCIDENCE_RATE`
   - Example: Aruba, 2023, Invasive Meningococcal Disease, 9.3 per 1M population

4. **cleaned_schedule.csv**: Vaccination schedules by country and target population.
   - Columns: `CODE`, `COUNTRYNAME`, `WHO_REGION`, `YEAR`, `VACCINECODE`, `VACCINE_DESCRIPTION`, `SCHEDULEROUNDS`, `TARGETPOP`, `TARGETPOP_DESCRIPTION`, `GEOAREA`, `AGEADMINISTERED`, `SOURCECOMMENT`
   - Example: Aruba, 2023, DTaP-IPV, Risk groups, 3 rounds

5. **cleaned_vaccine_intro.csv**: Vaccine introduction status by country and year.
   - Columns: `CODE`, `COUNTRYNAME`, `WHO_REGION`, `YEAR`, `VACCINE`, `INTRO`
   - Example: Afghanistan, 2023, Hepatitis B vaccine, Introduced (Yes)

**Note**: Ensure these datasets are placed in the same directory as the notebook.

## Setup Instructions

### Prerequisites
- Python 3.10 or later
- Jupyter Notebook or JupyterLab
- Required Python libraries:
  - `pandas`
  - `matplotlib`
  - `seaborn`
  - `scipy`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/ldotmithu/Vaccination-Data-Analysis-and-Visualization.git
   cd Vaccination-Data-Analysis-and-Visualization
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn scipy
   ```

4. Install Jupyter Notebook:
   ```bash
   pip install jupyter
   ```

5. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

### Dataset Preparation
- Place the five CSV files (`cleaned_cases.csv`, `cleaned_coverage.csv`, `cleaned_incidence.csv`, `cleaned_schedule.csv`, `cleaned_vaccine_intro.csv`) in the repository’s root directory.
- Ensure the datasets match the column structure described above.

## Usage

1. **Run the Notebook**:
   - Open `.ipynb` in Jupyter Notebook.
   - Execute cells sequentially to load data, perform analyses, and generate visualizations.
   - The notebook includes error handling for missing files or columns.

2. **Visualizations**:
   - Box plots: Compare disease cases before and after vaccine introduction.
   - Line plots: Show case trends around introduction years.
   - Bar plots: Display case reductions and coverage by vaccine/disease.
   - Scatter plots: Correlate vaccine coverage with disease incidence.


## Key Findings

- **Vaccine Impact**: Hepatitis B and Hib vaccines show significant case reductions where coverage is high (e.g., Aruba, 95.98% for DTPCV3).
- **Coverage Trends**: Primary doses (e.g., DTPCV1, 97.99%) have higher coverage than boosters (e.g., DIPHCV5, 82.69%).
- **Regional Disparities**: WHO’s EMR region (e.g., Afghanistan) shows later vaccine introductions and lower coverage compared to AMRO (e.g., Aruba).
- **Disease Prevalence**: Invasive Meningococcal Disease (9.3 per 1M in Aruba) varies by region, with EMR showing higher rates for some diseases.


## Contributing

Contributions are welcome! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature-branch`).
3. Make changes and commit (`git commit -m "Add feature"`).
4. Push to the branch (`git push origin feature-branch`).
5. Open a pull request.

Please ensure code follows PEP 8 standards and includes clear comments.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or suggestions, contact the repository owner via GitHub issues or email (if provided).

---

© 2025 ldotmithu