# Python-Final-Project
# Trending GitHub Repositories Analyzer

## Overview
# This Python program utilizes GitHub's API to fetch and analyze trending repositories based on specified criteria. 
# The program covers the following functionalities:

1. **Fetching Trending Repositories:**
   - The program sends a request to GitHub's API to retrieve trending repositories written in the Python programming language, based on weekly metrics.

2. **Data Analysis:**
   - The fetched repository data is then analyzed using Pandas and Numpy to calculate basic statistics, including the average number of stars and identifying the repository with the highest number of stars.

3. **Visualization:**
   - The program generates a horizontal bar chart using Matplotlib to visually represent the stars received by each trending repository.

4. **Advanced String Operations:**
   - Utilizing regular expressions, the program identifies repositories whose names contain a specified keyword, in this case, repositories with 'python' in their name.

5. **Git Initialization:**
   - If not already initialized, the program initializes a Git repository in the project directory and makes an initial commit.

## How to Use the Program

### Prerequisites
# Before running the program, make sure you have Python installed on your machine.
# Install the required libraries using the following command:
# `pip install requests numpy pandas matplotlib`

### Running the Program
# 1. Download the program source code.
# 2. Open a terminal or command prompt in the directory containing the program.

# 3. Run the program using the following command:
#    `python program_name.py`
#    Replace "program_name.py" with the actual name of your Python file.

# 4. Follow the on-screen instructions and review the output to understand the trending repositories, 
#    their statistics, and the visual representation.

# Note: The program does not require any command-line arguments. Simply execute the script,
# and it will fetch and analyze trending repositories automatically.

