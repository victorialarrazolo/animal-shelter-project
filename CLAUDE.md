# Animal Shelter Project

## Project Overview
This is a data analytics portfolio project analyzing animal shelter intake and outcome data across multiple US cities. The goal is to understand whether sterilization rates correlate with stray animal intake, and to visualize seasonal patterns and shelter outcomes.

## Personal Context
This project is built by Victoria Larrazolo, a data analyst with 5+ years of experience in Power BI, SQL, and Snowflake. The project connects to her personal experience volunteering with a spay/neuter organization in Mexico and rescuing a street dog through that organization.

## Project Structure
- notebooks/01_data_exploration.ipynb - Austin-only analysis (complete)
- notebooks/02_multi_city_analysis.ipynb - Multi-city comparison (in progress)
- data/ - Raw CSV files from Austin, Sonoma County CA, and Norfolk VA
- tableau/ - Cleaned CSV exports for Tableau Public dashboards
- website/ - GitHub Pages case study site (not yet started)

## Data Sources
- Austin Animal Center (Austin TX): intakes and outcomes 2013-2025, ~173K rows each
- Sonoma County Animal Shelter (CA): combined intake/outcome file
- Norfolk Animal Care Center (Norfolk VA): intake and outcome files

## Key Findings from Austin Analysis
- Pre-COVID correlation between sterilization rate and stray intake: r = -0.818
- Sterilized animals returned to owners at 2.6x the rate of intact animals
- Cat stray intake spikes 3x in May (kitten season), dogs stay flat year-round
- COVID created a structural break in 2020 that disrupted both sterilization rates and intake patterns

## Current Task
Building notebook 02_multi_city_analysis.ipynb to:
1. Load Austin, Sonoma, and Norfolk datasets
2. Standardize column names and category labels across all three cities
3. Add a city column to each dataset
4. Merge into one combined dataframe
5. Export clean summary CSVs for Tableau with city as a filter dimension

## Tech Stack
- Python 3.13 with pandas, numpy, matplotlib, seaborn, duckdb
- Tableau Public for visualization
- GitHub Pages for case study website
- Anthropic Claude API for AI-powered narrative summaries on the website

## Column Standardization Target
Final merged dataframe should have:
- city (Austin / Sonoma County / Norfolk)
- animal_type (Dog / Cat)
- intake_type (Stray / Owner Surrender / Public Assist / Other)
- sterilized (Sterilized / Intact / Unknown)
- outcome_category (Adopted / Returned to Owner / Transferred / Euthanized / Other)
- intake_year
- intake_month
- length_of_stay (days)