# DS-A5 — Time-Series Rolling Evaluation Lab

**Student:** Amsalu Tessema Adgeh  
**ID:** 2026A8000929002  

## Dataset
UCI Individual Household Electric Power Consumption, DOI [10.24432/C58K54]
(https://doi.org/10.24432/C58K54), CC BY 4.0. 
Dataset covers one household in Sceaux, France, Dec 2006–Nov 2010, with 2,075,259 one-minute records and missing measurements.

## Run
```bash
python -m venv .venv
# Windows: .venv\Scripts\activate
# macOS/Linux: source .venv/bin/activate
pip install -r requirements.txt
jupyter notebook https://github.com/amsalu2212/DS-Ass5/blob/main/Ass5.ipynb
```
Run every cell top-to-bottom. The notebook downloads `data/uci_household_power_consumption.zip`; 

## Experimental design
Forecast one-hour-ahead hourly mean global active power (kW). 
Six expanding rolling origins; each test block is 168 hours. 
Compare persistence, 24-hour seasonal naive, and a pipeline of median imputation, standardization, and histogram gradient boosting. 
Preprocessing is fitted separately at each origin. 
Predictors use only calendar-known information and target history ending no later than the previous completed hour. 
Leakage assertions check chronological separation.

## Outputs after a successful run
The notebook does not hard-code results. 
I derive the 216 word in(DS-Ass5.pdf) file summary from the 7 page reports from a successful run and verify the raw outputs.

## Provenance and limitations
Source attribution: Hebrail, G. & Berard, A. (2012). *Individual Household Electric Power Consumption*. 
UCI Machine Learning Repository. https://doi.org/10.24432/C58K54. License: CC BY 4.0. 