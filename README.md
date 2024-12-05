# Chess Games Analysis  
**COMP3125 Individual Project**  

**Dylan Patel**  

---

## Table of Contents  
1. [Introduction](#introduction)  
2. [Datasets](#datasets)  
    - [Source of Dataset](#source-of-dataset)  
    - [Character of the Dataset](#character-of-the-dataset)  
3. [Methodology](#methodology)  
    - [Question 1: Popular Openings by Rating Range](#question-1-popular-openings-by-rating-range)  
    - [Question 2: Game Termination by Rating Range](#question-2-game-termination-by-rating-range)  
    - [Question 3: Rating Difference Distribution](#question-3-rating-difference-distribution)  
4. [Results](#results)  
    - [Popular Openings by Rating Range](#popular-openings-by-rating-range)  
    - [Game Termination by Rating Range](#game-termination-by-rating-range)  
    - [Rating Difference Distribution](#rating-difference-distribution)  
5. [Discussion](#discussion)  
6. [Conclusion](#conclusion)  
7. [Acknowledgment](#acknowledgment)  
8. [References](#references)  

---

## Introduction  
Chess is a timeless game of strategy and intellect, with millions of games played daily worldwide. Analyzing large datasets of chess games can reveal patterns in player behavior, popular strategies, and the impact of rating differences on game outcomes.  

This project utilizes the Lichess dataset from 2013 to explore three key questions:  
1. **Which openings are most commonly played in different rating ranges?**  
2. **How often do players win via checkmate versus timeouts at various rating levels?**  
3. **What is the average rating difference between opponents in the dataset?**  

Understanding these patterns provides valuable insights into chess strategy and skill development across different player levels.  

---

## Datasets  

### Source of Dataset  
The dataset is sourced from [Lichess.org](https://lichess.org), a popular online chess platform. The PGN (Portable Game Notation) file contains games played from late 2012 through January 2013.  

### Character of the Dataset  
The dataset includes metadata such as:  
- **Format:** PGN (Portable Game Notation).  
- **Game Metadata:**  
    - Event: Game type (e.g., "Rated Classical game").  
    - Site: URL of the game.  
    - Result: Game outcome (e.g., "1-0").  
    - Player Ratings: Ratings of both players and their rating changes.  
    - Opening: Name and ECO (Encyclopaedia of Chess Openings) code.  
    - Time Control: Time settings (e.g., "480+2").  
    - Termination: How the game ended (e.g., "Normal").  
    - Moves: Complete list of moves.  

#### Preprocessing and Cleaning  
- Extracted key metadata using Python.  
- Grouped games into rating ranges.  
- Excluded incomplete or corrupt entries for consistency.  

---

## Methodology  

### Question 1: Popular Openings by Rating Range  
- **Approach:**  
    - Group games into rating ranges:  
        - `<1200`, `1200–1400`, `1400–1600`, `1600–1800`, `>1800`.  
    - Count occurrences of each opening.  
- **Analysis:**  
    - Identify top 10 openings per range and visualize using bar plots.  

### Question 2: Game Termination by Rating Range  
- **Approach:**  
    - Extract termination metadata (checkmate vs. timeouts).  
- **Analysis:**  
    - Calculate percentages for each termination type and visualize with grouped bar charts.  

### Question 3: Rating Difference Distribution  
- **Approach:**  
    - Compute absolute differences between player ratings.  
- **Analysis:**  
    - Calculate average and median differences.  
    - Visualize with a histogram and overlay averages.  

---

## Results  

### Popular Openings by Rating Range  
- **Findings:**  
    - **<1200:** Van Kruijs Opening  
    - **1200–1400:** Van Kruijs Opening  
    - **1400–1600:** Van Kruijs Opening  
    - **1600–1800:** Owen Defense  
    - **>1800:** Caro-Kann Defense  
- Bar plots revealed distinct opening preferences at each skill level.  

### Game Termination by Rating Range  
- **Findings:**  
    - Checkmate dominated (70%) across all levels.  
    - Timeouts accounted for 30%.  
- Grouped bar charts visualized termination trends.  

### Rating Difference Distribution  
- **Findings:**  
    - **Average Difference:** 154.17  
    - **Median Difference:** 121.00  
- Histogram showed most games had small rating differences, ensuring fairness.  

---

## Discussion  
### Observations  
1. Dataset covers only games from 2013, limiting relevance to current trends.  
2. Exclusion of noisy data reduced dataset size but ensured accuracy.  

### Future Enhancements  
- Use recent datasets to analyze evolving trends.  
- Include additional metrics like move accuracy.  
- Apply machine learning to predict outcomes based on metadata.  

---

## Conclusion  
This analysis of the 2013 Lichess dataset uncovered trends in opening preferences, termination types, and rating differences. These insights enhance our understanding of chess strategy across skill levels, paving the way for future research in player training and AI development.  

---

## Acknowledgment  
- Thanks to [Lichess.org](https://lichess.org) for providing the dataset and supporting open research.  

---

## References  
- **Lichess.org PGN Dataset, 2013**.  
