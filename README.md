# Construction Noise Monitoring — Analysis Code

This is the code I used for the analysis or the sensor data and survey data.
## Anonymised data

Data in this repository is fully randomised according to my DMP. Numeric readings (dBA, sharpness) are random values within a plausible range, event labels and survey answers are randomly drawn from their respective category sets. You will need to extract the "Data" ZIP file before running files in this folder.

## Notebooks

Run in this order:

1. **`Final_Extraction_Code.ipynb`** — loads the (anonymised) CityAI, Munisense, and Survey data, cleans and merges it, and exports `CityAI_data.csv`, `CityAI_sources_data.csv`, `Munisense_data.csv`, `Survey_data.csv`, and `question_labels.json`.
2. **`Final_Analysis1.ipynb`** — data quality checks: missing values, exceedance statistics.
3. **`Final_Analysis2.ipynb`** — main analysis: temporal patterns (day of week, week of project, hour of day), noise event statistics (counts, loudness, sharpness), further investigation of specific anomalies, and survey response analysis.

You do not need to run the Randomiser. I only provided it for reference.

## Notes

- File paths in the notebooks point to a local Windows directory structure and will need updating to run elsewhere.
- Sensor 10 (CityAI) and sensor 48/M2 (Munisense) are excluded from analysis even with the anonymised data. You can choose to include them but will need to make some changes across the project.
