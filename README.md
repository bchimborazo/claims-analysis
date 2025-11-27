# claims-analysis
- Name: Blanca Chimborazo-Reyes
- Project Description: This project analyzes healthcare claims data to identify billing patterns, common diagnoses, procedures, and payer relationships.
- Data Source:
    - Source: Stony Brook University
    - Files: 
        - HEADER: contains claim information (billing providers, service dates etc.)
        - LINE: contains service line/procedure details
        - CODE: contains diagnosis codes (ICD-10) and claim ID's
    - Additional Source: https://www.icd10data.com/ICD10CM/Codes (this site was used to search individual codes and the condition they correspond to)

- How to run this notebook: 
- Option 1: Google Colab
1. Click this link to open in Colab: https://colab.research.google.com/drive/1Ik4GoGQc5NuLwDalUXOnucVgEj2VSZqQ?usp=sharing
2. Load the required csv files (Note: storage of files is temporary, save files in local repository or store on device).
3. Run all cells

- Option 2: VS Code
1. Clone this repository
2. Open the folder in VS Code
3. Install the Python and Jupyter extensions if not already installed
4. Install required packages: `pip install -r requirements.txt`
5. Download the required data files and place them in the `data/` folder 
6. Open `notebooks/claims_analysis.ipynb`
7. Run all cells

Summary of key findings (3-5 bullet points):
- Top Provider: SB Internists is the highest-volume billing provider with 152 claims.
- Payer Mix: Medicare is the top payer with 62.37% of claims, followed by Healthfirst FFS at 11.86%.
- Common Procedures: Critical care (CPT 99291) is the most frequently billed procedure, often associated with acute respiratory failure (J96.01).
- Case Complexity: New York Spine and Brain Surgery handles the most complex cases, averaging 9.23 diagnosis codes per claim.
- Charges: Medicare accounts for the highest total charges ($131,008). 

Required libraries:
- To complete this colab project, I imported pandas as pd and matplotlib.pyplot as plt. 
- The instructions for this assignment calls for installing these libraries in the requirements.txt: 
    - pandas>=1.3.0
    - matplotlib>=3.4.0
    - seaborn>=0.11.0
