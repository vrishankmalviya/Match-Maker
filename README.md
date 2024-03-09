# Matchmaker

Matchmaker is a Python project that recommends matches between male and female profiles based on various criteria such as shared interests, age difference, swiping history, and relationship type preferences.

## Overview

The project consists of several Python scripts and functions designed to perform the following tasks:

- `rel_score`: Function to calculate the match score between two profiles based on shared interests, age difference, swiping history, and relationship type preferences.
- `recommend`: Function to recommend matches between male and female profiles by iterating through each male profile and finding the best match among female profiles.
- Example usage scripts to demonstrate how to use the functions and generate recommendations.

## Dependencies

- Python 3.x
- pandas (for data manipulation)

## Usage

To use the Matchmaker, follow these steps:

1. Clone the repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Modify the example scripts or integrate the functions into your own project as needed.
4. Run the example scripts or incorporate the functions into your code to generate recommendations between male and female profiles.

## Example

```python
# Import necessary functions and modules
from matchmaker import calculate_match_score, recommend_profiles

# Load male and female profiles
# ...

# Generate recommendations
recommendation = recommend_profiles(male_profiles, female_profiles)

# Sort recommendations by match score in descending order
recommendations.sort(key=lambda x: x[2], reverse=True)

# Display the top recommendations
for idx, (male_profile, female_profile, match_score) in enumerate(recommendations[:10]):
    print(f"Recommendation {idx + 1}:")
    print(f"Male Profile (User {male_profile['User ID']}): Age {male_profile['Age']}, Interests {male_profile['Interests']}")
    print(f"Female Profile (User {female_profile['User ID']}): Age {female_profile['Age']}, Interests {female_profile['Interests']}")
    print(f"Match Score: {match_score}")
    print()
