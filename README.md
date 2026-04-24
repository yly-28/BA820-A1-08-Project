# Survival Strategy Analysis in *Alone*: Equipment Choices, Similarity, and Exit Patterns

## Project Overview

This project explores survival strategy patterns in the reality TV show *Alone* using unsupervised learning and exploratory data analysis. In the show, contestants are isolated in remote wilderness locations and must survive as long as possible using a limited set of selected gear items. Since each contestant is allowed to bring only a fixed number of items, their equipment choices provide a useful lens for understanding different survival strategies.

The main goal of this project is to examine whether contestants' gear loadouts reveal meaningful strategy groups, how stable these groups are under different analytical choices, and whether these equipment-based strategies are related to survival outcomes such as winning, medical evacuation, or voluntary withdrawal.

Rather than predicting outcomes directly, this project focuses on similarity, grouping, co-occurrence, and interpretation. The analysis is designed to help understand how contestants make strategic tradeoffs under resource constraints.

## Research Questions

This project is guided by the following questions:

1. Do contestants' gear selections form distinct survival strategy types?
2. Which gear items tend to appear together, and what do these co-occurrence patterns suggest about survival priorities?
3. Are equipment-based strategy groups associated with different exit outcomes, such as winning, medical evacuation, or withdrawal?
4. How stable are the identified strategy groups when different clustering methods, distance metrics, or feature representations are used?
5. Do the results suggest clearly separated survival archetypes, or is the strategy space more constrained and overlapping?

## Dataset

The project uses structured data related to contestants, gear loadouts, and episode-level information from *Alone*. The main datasets include:

- `survivalists.csv`: contestant-level information such as season, name, age, gender, result, and exit reason
- `loadouts.csv`: gear items selected by each contestant
- `episodes.csv`: episode-level information, including season and episode structure

The core analytical dataset is built by merging contestant-level information with a binary equipment matrix. Each row represents one contestant, and each gear column indicates whether that contestant selected a specific item.

The final equipment matrix contains:

- 94 contestants
- 27 binary gear item columns
- contestant-level metadata such as season, name, age, result, and exit category

## Project Structure

```text
.
├── data/
│   ├── raw/
│   │   ├── survivalists.csv
│   │   ├── loadouts.csv
│   │   └── episodes.csv
│   ├── processed/
│   │   └── unified_survivalist_loadout.csv
│
├── notebooks/
│   ├── 01_eda_preprocessing.ipynb
│   ├── 02_equipment_similarity_clustering.ipynb
│   ├── 03_cluster_exit_analysis.ipynb
│   └── 04_robustness_checks.ipynb
│
├── reports/
│   ├── proposal/
│   ├── milestone_2/
│   ├── milestone_3/
│   └── milestone_4/
│
├── figures/
│   ├── gear_frequency.png
│   ├── cooccurrence_heatmap.png
│   ├── dendrogram.png
│   ├── cluster_profiles.png
│   └── robustness_results.png
│
├── README.md
└── requirements.txt
