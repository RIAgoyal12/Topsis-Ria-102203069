# TOPSIS Python Tool

## Overview

TOPSIS (Technique for Order of Preference by Similarity to Ideal Solution) is a widely used method in multi-criteria decision analysis (MCDA). It helps in ranking alternatives based on several criteria, each of which might have a different level of importance (weight) and impact (positive or negative).

This Python tool implements the TOPSIS algorithm to rank alternatives based on input data, weights, and impacts. It provides results including rankings, distances from both the ideal and worst solutions, and the corresponding TOPSIS score for each option.

## Features

- **Ranking**: Automatically ranks alternatives based on selected criteria.
- **Customizable Inputs**: Allows users to specify custom weights and impacts for each criterion.
- **Ideal Solution Calculation**: Computes the Euclidean distance from both the ideal best and worst solutions.
- **CSV Support**: Read data from CSV files and output the results into CSV format.

## Installation

To install the tool, use the following pip command:

```bash
pip install Topsis-Ria-102203069==1.0.0
```


## Usage
Running from Command Line
Once the package is installed, you can run the TOPSIS method directly from the command line by following this structure:

python -m topsis.topsis input_data.csv "1,1,2,2,1" "+,+,-,-,-" result.csv

 ### Parameters
The command-line interface expects the following arguments:

input_data.csv (Required):
The path to the input CSV file containing the data. The first column should list the alternatives (e.g., Option1, Option2, etc.), and the remaining columns should represent the criteria values for each alternative.

- **"1,1,2,2,1"** (Required):
A string of comma-separated values representing the weights assigned to each criterion. Higher values indicate more important criteria.

- **"+,+,-,-,-" **(Required):
A string of comma-separated values indicating the impact type for each criterion. + means a higher value is better for that criterion, and - means a lower value is better for that criterion.

- **result.csv** (Required):
The path to the output CSV file where the results will be stored. The resulting file will contain columns for each option, including:

## Option name
Distance from the Ideal Best
Distance from the Ideal Worst
TOPSIS Score
Rank

## Explanation of Results
- ** Distance from Ideal Best:** The Euclidean distance between each alternative and the ideal best solution. The ideal best is the alternative with the highest value in all positively impactful criteria and the -lowest in all negatively impactful ones.
- **Distance from Ideal Worst:** The Euclidean distance between each alternative and the ideal worst solution. The ideal worst is the alternative with the lowest value in positively impactful criteria and the highest in negatively impactful ones.
- **TOPSIS Score:** A score that reflects how close each alternative is to the ideal solution. A higher score means the alternative is closer to the ideal best.
- **Rank:** The ranking of each alternative based on the TOPSIS score, with 1 being the best.
## License
© 2025 Ria Goyal

This project is licensed under the MIT license. See LICENSE for more details.


## Package 

![image](https://github.com/user-attachments/assets/57825cfd-7d26-4003-93dc-c87203b94590)


## Additional Information
This tool requires Python version 3.6 or higher.
Make sure your input data is clean and only includes numerical values in the criteria columns.
The input CSV file must have the alternatives listed in the first column, followed by the numerical values for each criterion.
