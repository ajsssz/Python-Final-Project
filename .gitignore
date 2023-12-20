# Import necessary libraries
import requests
import re
import numpy as np
import pandas as pd
import matplotlib.pyplot as plt
import os
import subprocess

# Function to fetch trending repositories from GitHub API
def fetch_trending_repositories(language='python', since='weekly'):
    url = f'https://api.github.com/search/repositories?q=language:{language}&sort=stars&order=desc&since={since}'
    response = requests.get(url)
    
    if response.status_code == 200:
        return response.json()['items']
    else:
        print(f"Failed to fetch data. Status code: {response.status_code}")
        return []

# Function to analyze repository data
def analyze_repositories(repositories):
    if not repositories:
        print("No data to analyze.")
        return

    # Extract relevant information
    repo_names = [repo['name'] for repo in repositories]
    stars = [repo['stargazers_count'] for repo in repositories]

    # Basic analysis using Pandas/Numpy
    df = pd.DataFrame({'Repository': repo_names, 'Stars': stars})
    mean_stars = np.mean(df['Stars'])
    max_stars_repo = df.loc[df['Stars'].idxmax()]['Repository']

    print(f"Average stars: {mean_stars}")
    print(f"Repository with the most stars: {max_stars_repo}")

    # Plotting using Matplotlib
    plt.figure(figsize=(10, 6))
    plt.barh(repo_names, stars, color='skyblue')
    plt.xlabel('Stars')
    plt.title('Trending GitHub Repositories')
    plt.show()

# Function to perform advanced string operations
def advanced_string_operations(repo_names):
    # Example: Find repositories with names containing 'python'
    python_repos = [repo for repo in repo_names if re.search(r'python', repo, re.I)]
    print(f"Repositories with 'python' in their name: {python_repos}")

# Function to initialize Git repository and make initial commit
def initialize_git_repository():
    if not os.path.exists('.git'):
        subprocess.run(['git', 'init'])
        subprocess.run(['git', 'add', '.'])
        subprocess.run(['git', 'commit', '-m', 'Initial commit'])

# Main function
def main():
    # Step 1: Fetch trending repositories
    repositories = fetch_trending_repositories()

    # Step 2: Perform analysis
    analyze_repositories(repositories)

    # Step 3: Perform advanced string operations
    repo_names = [repo['name'] for repo in repositories]
    advanced_string_operations(repo_names)

    # Step 4: Initialize Git repository and make initial commit
    initialize_git_repository()

if __name__ == "__main__":
    main()
