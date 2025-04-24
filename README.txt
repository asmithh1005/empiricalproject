Empirical Project: Nutritional Disparities in UK Fast Food: A Comparative Macronutrient Analysis

This project explores the nutritional quality of fast food items across major US chains, with a focus on protein density (grams of protein per 100 calories). The aim is to uncover trends, outliers and nutritional strategies that chains use to market their products, especially those that appear to be "healthier" but may not deliver nutritionally.

Project Structure:

empiricalproject/
│
├── blog/                   # Final blog post which is in PDF format
├── data/                   # Raw and cleaned CSV files aswell as source link
├── notebooks/              # Python notebooks for scraping, cleaning and analysis
│   ├── cleaning_data.ipynb     # Run this first to prepare the cleaned dataset
│   └── analysis.ipynb          # Main analysis and visualizations
├── outputs/                # Saved plots and visual outputs
├── venv/                   # Python virtual environment 
├── README.md               # Project overview and setup instructions
└── requirements.txt        # Python dependencies for easy replication

## How to Run

1. Clone the repository:
   git clone https://github.com/asmithh1005/empiricalproject
   cd empiricalproject

2. Set up your virtual environment:
   python -m venv venv  
   (On Mac/Linux: source venv/bin/activate)  
   (On Windows: venv\Scripts\activate)

3. Install dependencies:
   pip install -r requirements.txt

4. **Important: Edit File Paths**  
   Before running the notebooks, make sure to **edit any hard-coded file paths** in `notebooks/cleaning_data.ipynb` and `notebooks/analysis.ipynb`.  
   These paths point to local directories (e.g., for loading/saving data and plots) and must be updated to reflect your own machine’s structure (e.g., C:/Users/yourname/Desktop/fast_food_nutrition/data/).

5. Run the notebooks in this order:
   - First run `notebooks/cleaning_data.ipynb` to generate and clean the dataset.
   - Then run `notebooks/analysis.ipynb` to conduct the full analysis and generate visuals.

Key Features:

- Web Scraping: Selenium + BeautifulSoup used to extract fast food nutritional data from Nutritionix.com.
- Data Cleaning: Removed inconsistent entries, standardized column names, dropped irrelevant or incomplete rows.
- Protein Density Analysis: Core focus on "protein per 100 calories" as a metric for evaluating food quality.
- Visual Exploration: Graphs and plots include:
  - Protein density comparison by chain
  - Top 20 protein-dense items
  - Outliers in calorie estimates
  - Fat-to-protein ratio distributions
- Regression Modelling: Used to identify key predictors of high protein density.

Blog Post:

The full blog post is located in the `blog` folder.

Tools & Libraries Used

beautifulsoup4==4.13.3
certifi==2025.1.31
charset-normalizer==3.4.1
idna==3.10
numpy==2.2.4
pandas==2.2.3
python-dateutil==2.9.0.post0
pytz==2025.2
requests==2.32.3
six==1.17.0
soupsieve==2.6
typing_extensions==4.13.1
tzdata==2025.2
urllib3==2.3.0
matplotlib
seaborn
statsmodels
scipy
scikit-learn


Author

**Adam Smith**  
GitHub: https://github.com/asmithh1005/empiricalproject
