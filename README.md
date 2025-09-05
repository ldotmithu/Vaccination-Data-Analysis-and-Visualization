# Vaccination Data Analysis and Visualization 🌍💉

Welcome to the **Vaccination Data Analysis and Visualization** project! This repository houses a Jupyter Notebook (`vaccine.ipynb`) that explores the impact of vaccines on disease cases, coverage, and incidence rates across countries like Aruba and Afghanistan. Using cleaned datasets from sources like the World Health Organization (WHO), we dive into vaccine effectiveness, coverage gaps, and regional disparities with 📊 stunning visualizations and 📈 robust statistical analyses.

Built with Python, Pandas, Matplotlib, Seaborn, and Scipy, this project answers 10 key questions to uncover insights about global vaccination efforts.

## 🎯 Objectives

The analysis tackles these questions:
1. Is there a correlation between vaccine introduction and reduced disease cases?
2. What are the trends in disease cases before and after vaccination campaigns?
3. Which diseases show the most significant case reductions due to vaccines?
4. What percentage of the target population is covered by each vaccine?
5. How do vaccination schedules (e.g., booster doses) affect coverage?
6. Are there disparities in vaccine introduction timelines across WHO regions?
7. How does vaccine coverage correlate with disease reduction?
8. Which regions have low coverage despite vaccine availability?
9. What are the coverage gaps for high-priority diseases (e.g., TB, Hepatitis B)?
10. Are certain diseases more prevalent in specific geographic areas?

## 📋 Datasets

The project uses five cleaned CSV datasets:

1. **cleaned_cases.csv**: Disease case counts by country and year.
   - Columns: `GROUP`, `CODE`, `NAME`, `YEAR`, `DISEASE`, `DISEASE_DESCRIPTION`, `CASES`
   - Example: Aruba, 2023, Invasive Meningococcal Disease, 1 case

2. **cleaned_coverage.csv**: Vaccination coverage by antigen and country.
   - Columns: `GROUP`, `CODE`, `NAME`, `YEAR`, `ANTIGEN`, `ANTIGEN_DESCRIPTION`, `COVERAGE_CATEGORY`, `COVERAGE_CATEGORY_DESCRIPTION`, `TARGET_NUMBER`, `DOSES`, `COVERAGE`
   - Example: Aruba, 2023, DTPCV3, 95.98% coverage

3. **cleaned_incidence.csv**: Disease incidence rates per population unit.
   - Columns: `GROUP`, `CODE`, `NAME`, `YEAR`, `DISEASE`, `DISEASE_DESCRIPTION`, `DENOMINATOR`, `INCIDENCE_RATE`
   - Example: Aruba, 2023, Invasive Meningococcal Disease, 9.3 per 1M

4. **cleaned_schedule.csv**: Vaccination schedules by country and target population.
   - Columns: `CODE`, `COUNTRYNAME`, `WHO_REGION`, `YEAR`, `VACCINECODE`, `VACCINE_DESCRIPTION`, `SCHEDULEROUNDS`, `TARGETPOP`, `TARGETPOP_DESCRIPTION`, `GEOAREA`, `AGEADMINISTERED`, `SOURCECOMMENT`
   - Example: Aruba, 2023, DTaP-IPV, Risk groups, 3 rounds

5. **cleaned_vaccine_intro.csv**: Vaccine introduction status by country and year.
   - Columns: `CODE`, `COUNTRYNAME`, `WHO_REGION`, `YEAR`, `VACCINE`, `INTRO`
   - Example: Afghanistan, 2023, Hepatitis B vaccine, Introduced (Yes)

**Note**: Place these datasets in the same directory as the notebook.

## 🛠️ Setup Instructions

### Prerequisites
- Python 3.10 or later
- Jupyter Notebook or JupyterLab
- Libraries: `pandas`, `matplotlib`, `seaborn`, `scipy`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/ldotmithu/Vaccination-Data-Analysis-and-Visualization.git
   cd Vaccination-Data-Analysis-and-Visualization
   ```

2. Create a virtual environment (recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install pandas matplotlib seaborn scipy jupyter
   ```

4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```


### Dataset Preparation
- Ensure the five CSV files are in the repository’s root directory.
- Verify the datasets match the column structure described above.

## 🚀 Usage

1. **Run the Notebook**:
   - Open `vaccine.ipynb` in Jupyter Notebook or JupyterLab.
   - Execute cells sequentially to load data, run analyses, and generate visualizations.
   - The notebook includes error handling for missing files or columns.

2. **Visualizations** 📊:
   - **Box Plots**: Compare disease cases before and after vaccine introduction.
   - **Line Plots**: Show case trends around introduction years.
   - **Bar Plots**: Display case reductions and coverage by vaccine/disease.
   - **Scatter Plots**: Correlate vaccine coverage with disease incidence.


## 🔍 Key Findings

- **Vaccine Impact**: Hepatitis B and Hib vaccines significantly reduce cases in high-coverage areas (e.g., Aruba, 95.98% for DTPCV3).
- **Coverage Trends**: Primary doses (e.g., DTPCV1, 97.99%) outperform boosters (e.g., DIPHCV5, 82.69%).
- **Regional Disparities**: EMR (e.g., Afghanistan) lags in vaccine introductions compared to AMRO (e.g., Aruba).
- **Disease Prevalence**: Invasive Meningococcal Disease (9.3 per 1M in Aruba) and Neonatal Tetanus are more prevalent in EMR regions.


## 🤝 Contributing

We welcome contributions! To get started:
1. Fork the repository.
2. Create a branch: `git checkout -b feature-branch`.
3. Commit changes: `git commit -m "Add feature"`.
4. Push to the branch: `git push origin feature-branch`.
5. Open a pull request.

Follow PEP 8 standards and include clear comments in your code.

## 📜 License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## 📬 Contact

For questions or feedback, open an issue on GitHub or contact the repository owner.

---

© 2025 ldotmithu | Made with 💉 & 📊