# Data Visualization Virtual Lab

An interactive Streamlit application that helps students explore datasets, build charts, learn when to use each visualization, and test their understanding through quiz-based practice.

This project combines data analysis, visual storytelling, and ed-tech design into one guided lab experience.

## Live Demo

Hosted on Streamlit:

https://vizellect.streamlit.app/

## Overview

The Virtual Data Visualization Lab is designed as a hands-on learning environment where users can:

- upload real datasets
- inspect data types and quality
- clean and transform records
- perform exploratory data analysis
- build visualizations in auto and manual mode
- learn chart concepts dynamically
- answer dataset-aware quiz questions
- generate simple and technical insights

The goal is to make data visualization both practical and educational, not just analytical.

## Key Features

### 1. File Upload Module

Supports:

- CSV
- Excel (`.xlsx`)
- JSON

After upload, the app displays:

- top-row preview
- dataset shape
- column names
- detected data types
- missing values summary

### 2. Automatic Data Type Detection

Columns are automatically classified into:

- Numerical
- Categorical
- Datetime

This helps the app recommend suitable charts and generate smarter quiz questions.

### 3. Data Cleaning Module

Users can clean the dataset with interactive controls:

- drop missing values
- fill missing values using mean, median, or mode
- remove duplicate rows
- convert column types
- compare before vs after cleaning

### 4. Exploratory Data Analysis

The app includes built-in EDA tools for:

- summary statistics
- distribution analysis
- correlation heatmaps

### 5. Visualization Engine

Built with Plotly for interactive charts.

#### Auto Mode

The app suggests appropriate charts based on dataset structure:

- Numerical -> Histogram, Boxplot
- Categorical -> Bar, Pie
- Numerical vs Numerical -> Scatter
- Categorical vs Numerical -> Boxplot

#### Manual Mode

Users can choose:

- X-axis
- Y-axis
- chart type

Supported chart types:

- Line
- Bar
- Scatter
- Histogram
- Boxplot
- Heatmap
- Pie

### 6. Learning Mode

Every chart is connected to an educational explanation.

For each selected visualization, the lab shows:

- when to use the chart
- what the chart shows
- a real-world use case

This makes the app useful for both self-study and classroom demonstrations.

### 7. Quiz Mode

The quiz system is designed to gamify learning.

Features include:

- multiple-choice questions
- immediate feedback
- answer explanations
- live score tracking
- difficulty levels: Easy, Medium, Hard
- dataset-aware question generation

### 8. Insight Generator

The app automatically detects patterns such as:

- missing value warnings
- duplicate rows
- skewed distributions
- strong correlations
- dominant categories

It also produces a short summary paragraph to help users interpret the dataset quickly.

### 9. Interactive Filters

Users can slice the active dataset view using:

- sliders for numerical ranges
- dropdown filters for categorical columns

### 10. Download Options

The lab supports:

- downloading cleaned datasets as CSV
- downloading cleaned datasets as Excel
- downloading generated plots as PNG

## Educational Value

This project is built as a "learn by doing" lab.

Students can:

- explore real data interactively
- understand why certain charts are appropriate
- practice chart selection through quizzes
- connect visual patterns to real-world decisions

It is well suited for:

- data visualization labs
- beginner data science classes
- statistics and analytics practice
- mini projects and demonstrations

## Tech Stack

- Python
- Streamlit
- Pandas
- Plotly
- OpenPyXL
- Kaleido

## Project Structure

The current implementation is organized in a modular way inside a single Streamlit app:

```text
app.py
requirements.txt
.gitignore
README.md
```

Main functional modules inside `app.py` include:

- `data_loader()`
- `cleaning_module()`
- `visualization_module()`
- `learning_module()`
- `quiz_module()`
- `insights_module()`

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/rushikesh-geek/Data-Visualization-Virtual-Lab.git
cd Data-Visualization-Virtual-Lab
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the app

```bash
streamlit run app.py
```

## How to Use

1. Open the app in your browser using Streamlit.
2. Upload a CSV, Excel, or JSON dataset.
3. Review the dataset overview and detected column types.
4. Clean the data if needed.
5. Explore the visualizations in auto or manual mode.
6. Read the concept explanations in Learning Mode.
7. Practice with the quiz.
8. Review auto-generated insights.
9. Download the cleaned dataset or plot outputs.

## Performance Notes

The app uses Streamlit caching with `st.cache_data` to improve performance for repeated data loading and question generation. It is also designed to handle larger datasets more efficiently through filtered views and guided chart selection.

## Team

Built by Team ADS, Computer Engineering:

- Rushikesh Shembade
- Aditya Upasani
- Raziq Sarwar Mukadam

## License

This project is intended for educational and academic use. 
