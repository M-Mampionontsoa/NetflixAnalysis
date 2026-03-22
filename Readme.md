# Netflix Analysis

A comprehensive data analysis project exploring Netflix's content catalog across multiple dimensions including content types, production countries, age classifications, and genres.

## Table of Contents

- [Overview](#overview)
- [Project Structure](#projetct-structure)
- [Dataset](#dataset)
- [Data Cleaning](#data-cleaning)
- [Visualizations](#visualizations)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Future Improvements](#future-improvements)
- [Contributing](#contributing)
- [License](#license)

## Overview

This project provides an in-depth analysis of Netflix's streaming catalog, examining the distribution of content based on multiple criteria:

- **Content Types**: Movies vs. TV Shows
- **Production Countries**: Geographic distribution of content
- **Age Classification**: Rating distribution (PG, PG-13, R, TV-MA, etc.)
- **Genres**: Most popular categories and their evolution

## Project Structure

netflix-analysis/
│
├── data/
│ ├── netflix_original.csv # Raw dataset
│ ├── netflix_cleaned.csv # Processed dataset
│
│
├── notebooks/
│ ├── description.ipynb
│ ├── exploration.ipynb
│ └── cleaning.ipynb
| └── analysis.ipynb

│
├── requirements.txt # Project dependencies
├── README.md # Project documentation

## Dataset

### Original Dataset

- **Total entries**: 7,787 records
- **Total columns**: 12 attributes
- **Memory usage**: 730.2 KB

### Dataset Columns

| Column         | Description                                         |
| -------------- | --------------------------------------------------- |
| `show_id`      | Unique identifier for each title                    |
| `type`         | Movie or TV Show                                    |
| `title`        | Name of the content                                 |
| `director`     | Director(s) of the content                          |
| `cast`         | Main actors/actresses                               |
| `country`      | Country of production                               |
| `date_added`   | Date added to Netflix                               |
| `release_year` | Original release year                               |
| `rating`       | Age classification (PG, R, TV-MA, etc.)             |
| `duration`     | Duration (minutes for movies, seasons for TV shows) |
| `listed_in`    | Genres/categories                                   |
| `description`  | Brief synopsis                                      |

## Data Cleaning

1. **Removed duplicates**: Eliminated duplicate entries
2. **Handled missing values**:
   - Filled missing countries with 'Nan'
   - Handled missing ratings with appropriate defaults
   - Processed missing directors and cast information
3. **Standardized formats**:
   - Normalized date formats
   - Standardized country names
   - Categorized age ratings into meaningful groups
4. **Data type corrections**:
   - Converted date_added to datetime format
   - Extracted numeric values from duration

## Visualizations

### 1. Content Type Distribution

- **Pie Chart**: Visual representation of Movies vs. TV Shows ratio
- **Bar Chart**: Comparative analysis with percentages
- Custom styling with professional color palettes

### 2. Production Countries Analysis

- **Top 10 Countries**: Bar chart showing content production leaders
- **Geographic Distribution**: Visualization of content origin diversity
- **Trend Analysis**: Evolution of production countries over years

### 3. Age Classification Analysis

- **Rating Distribution**: Breakdown of content by age appropriateness
- **Content Type vs. Rating**: Comparative analysis between movies and TV shows
- **Rating Trends**: Evolution of age classifications over time

### 4. Genre Analysis

- **Most Popular Genres**: Top 15 genres by content count
- **Genre Distribution**: Pie chart of genre proportions
- **Genre Evolution**: How genre popularity has changed over the years

### 5. Temporal Analysis

- **Content Addition Trends**: Year-by-year addition of content to Netflix
- **Release Years Distribution**: Historical analysis of content release dates
- **Seasonal Patterns**: Monthly content addition patterns

## Technologies Used 🛠️

| Library              | Purpose                                            |
| -------------------- | -------------------------------------------------- |
| **Python 3.8+**      | Core programming language                          |
| **Pandas**           | Data manipulation and analysis                     |
| **NumPy**            | Numerical computations                             |
| **Matplotlib**       | Custom visualizations and styling                  |
| **Seaborn**          | Statistical visualizations and enhanced aesthetics |
| **Jupyter Notebook** | Interactive development environment                |

## Installation

### Prerequisites

- Python 3.8 or higher
- pip package manager

### Setup

```bash
# Clone the repository
git clone https://github.com/yourusername/netflix-analysis.git
cd netflix-analysis

# Create virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install dependencies
pip install -r requirements.txt
```
