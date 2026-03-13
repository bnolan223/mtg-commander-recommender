# MTG Commander Recommender System

This project explores the development of a recommendation system for Magic: The Gathering Commander decks. The goal is to analyze a user's decklist and suggest potential improvements, such as card upgrades within the 99 or possible commander alternatives that better align with the deck’s strategy.

The project focuses on intermediate Commander players who understand the basics of deck construction but may benefit from data-driven insights when refining their decks.

## Data

Card data for this project comes from the MTGJSON AllPrintings dataset:
https://mtgjson.com/downloads/all-files/#allprintings

The dataset includes information on card identity, mana value, colors, card types, rarity, and rules text, which are used to analyze deck composition and support the recommendation pipeline.

## Project Structure

notebooks/ – Exploratory data analysis and modeling notebooks 

reports/ - Contains report files

## How to Run the Project

At the current stage of development, the repository contains exploratory data analysis notebooks used to understand the MTG card dataset.

To reproduce the analysis:

1. Download the **AllPrintings.json** dataset from MTGJSON:
https://mtgjson.com/downloads/all-files/#allprintings

2. Place the dataset locally (the raw dataset is not stored in the repository due to its size).

3. Open the Jupyter notebooks located in the `notebooks/` directory.

4. Run the notebooks sequentially to reproduce the exploratory data analysis and summary statistics.

Future versions of this project will include the recommendation pipeline and a user facing interface for submitting decklists.

## Current Progress

- Data acquisition and preprocessing pipeline established
- Basic metrics exploratory data analysis completed
- GitHub repository created to support collaborative development
- EDA Report completed
- Status Presentation completed

## Team Members

Group 1 – ManaCurve Analytics

- Bennett Nolan
- Jason Weinstein
- Dominic Durning
- Darryl Fields
- Nate Moore
