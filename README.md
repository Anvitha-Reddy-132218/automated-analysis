CSV Data Analysis Automation

This project automates the process of analyzing multiple datasets stored in CSV format. It generates detailed summaries, visualizations, and insights for each dataset.

Features

Data Ingestion: Reads multiple CSV files with robust handling of encoding issues.

Statistical Summaries: Generates descriptive statistics for all columns, including numeric and categorical data.

Missing Data Identification: Highlights columns with missing values.

AI-Generated Reports: Utilizes OpenAI's GPT-4 model to provide insightful textual summaries for each dataset.

Visualizations:

Bar plots for top genres by average ratings (if applicable).

Correlation heatmaps for numeric columns.

Prerequisites

Python 3.7 or higher

Required Libraries:

pandas

matplotlib

seaborn

openai

Install dependencies using:

pip install pandas matplotlib seaborn openai

Setup

Set Up OpenAI API Key:

Obtain an API key from OpenAI.

Set it as an environment variable:

export OPENAI_API_KEY='your-api-key-here'

Configure API Proxy (if required):

Update the script to include your API proxy and endpoint:

openai.api_base = "https://your-proxy-url/openai/v1"

Usage

Place the target CSV files in the project directory.

Update the CSV_FILES list in the script with the names of your CSV files:

CSV_FILES = ["goodreads.csv", "happiness.csv", "media.csv"]

Run the script:

python analyze_csv.py

Results for each dataset will be saved as:

Summary Report: goodreads_README.md, happiness_README.md, etc.

Visualizations: goodreads_top_genres.png, happiness_heatmap.png, etc.

Example Outputs

Summary Report

goodreads_README.md

# Data Analysis Report for Goodreads.csv
## Summary
- **Key Statistics**: Overview of key metrics such as mean, median, and standard deviation.
- **Trends and Insights**: Identifies top correlations and trends in the dataset.
- **Recommendations**: Suggested steps for further exploration.

Visualizations

Top 5 Genres by Average Rating


Correlation Heatmap


Error Handling

Encoding Issues: If a file cannot be read due to encoding, the script will skip the file and log the error.

Missing Columns: Visualizations requiring specific columns (e.g., Genre or Rating) will be skipped if those columns are not present.

Future Improvements

Enhanced Visualization: Add support for interactive visualizations using Plotly or Dash.

Additional File Formats: Extend support to include Excel, JSON, and database connections.

Dashboard Integration: Automate uploading res
