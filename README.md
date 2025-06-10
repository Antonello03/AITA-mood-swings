# r/AmITheAsshole Analysis Project

This repository contains the **AITA Subreddit Exploration & Web and Social Media Analysis** project by Antonello Di Rita, Alessandro Longato, and Emirhan Kayar for the Web and Social Networks course (B.Sc. in Artificial Intelligence, a.y. 2024/2025).

## Overview
The project analyzes the subreddit [r/AmITheAsshole](https://www.reddit.com/r/AmITheAsshole) to study user interaction patterns, sentiment trends, and temporal dynamics. The focus is on posts judged as “YTA” (You’re the Asshole) versus “NTA” (Not the Asshole).

## Data
- **Posts**: 500 top posts (250 YTA, 250 NTA) from 2019–2023, collected via the Reddit API, including submission ID, author, flair, score, title, body, and comment count.
- **Comments**: Up to three levels deep, with the year, depth, text, author, and parent post label. Reply relationships are excluded for sentiment analysis.
- **Reply Graphs**: Complete comment trees for 40 posts (20 YTA, 20 NTA) stored under `replyGraphs/`, preserving comment IDs and authors.
- **User Interaction Graph**: Interactions across all posts, aggregated by user pairs with comment scores and vote tendencies (Total YTA minus Total NTA).

Key CSVs include:
- `top450-aita-balanced.csv`
- `comments.csv`
- `comments_with_bert.csv`
- `User-Interaction_graph.csv`
- `user_interaction_graph-centrality_metrics.csv`
Reply graphs are located in the `replyGraphs/` directory.

## Repository Structure
- `data_collection.ipynb` – uses PRAW and pandas to gather posts and comments.
- `temporal_analysis.ipynb` – analyzes posting times with pandas, seaborn, and matplotlib.
- `sentiment_analysis.ipynb` – performs sentiment scoring with NLTK, Afinn, VADER, and other libraries.
- `topology_analysis.ipynb` – builds interaction networks using networkx and computes network metrics.

## Usage
1. Install Python (3.10+ recommended) and create a virtual environment.
2. Install the dependencies: `praw`, `pandas`, `requests`, `matplotlib`, `seaborn`, `networkx`, `nltk`, `afinn`, and other libraries referenced in the notebooks.
3. Open the notebooks in Jupyter or Google Colab. Each notebook can load the CSV files directly—many cells reference GitHub raw URLs for convenience. Execute the cells in sequence to reproduce the analyses.

## Authors
Antonello Di Rita  
Alessandro Longato  
Emirhan Kayar
