# IPL Match Winner Prediction

A data analysis and prediction project built using IPL ball-by-ball delivery data from 2008 to 2024. The project analyzes team and player performance, then predicts the likely winner of any IPL match based on historical strength scores.

---

## About the Project

This project digs into 16 years of IPL data to find patterns in team batting, bowling, and overall performance. Using those patterns, it builds a strength score for each team and uses it to predict which team is more likely to win when two teams face each other.

---

## Dataset

- File: deliveries.csv
- Total Records: 260,920 ball-by-ball deliveries
- Features: 17 columns including match_id, batting_team, bowling_team, batter, bowler, batsman_runs, total_runs, is_wicket, dismissal_kind, and more
- Coverage: IPL seasons 2008 to 2024

---

## What This Project Does

1. Loads and explores the full IPL deliveries dataset
2. Analyzes total runs scored by every team across all seasons
3. Analyzes total wickets taken by every team across all seasons
4. Identifies the top 10 batsmen by career runs
5. Identifies the top 10 bowlers by career wickets
6. Builds a normalized strength score for each team based on batting and bowling performance
7. Predicts the winner and win probability for any two teams

---

## Key Results

### Top Run-Scoring Teams
| Team | Total Runs |
|------|-----------|
| Mumbai Indians | 42,176 |
| Kolkata Knight Riders | 39,331 |
| Chennai Super Kings | 38,629 |

### Top Wicket-Taking Teams
| Team | Total Wickets |
|------|--------------|
| Mumbai Indians | 1,591 |
Chennai Super Kings | 1,481 |
| Kolkata Knight Riders | 1,464 |

### Top 3 Batsmen (Career Runs)
| Player | Runs |
|--------|------|
| V Kohli | 8,014 |
| S Dhawan | 6,769 |
| RG Sharma | 6,630 |

### Top 3 Bowlers (Career Wickets)
| Player | Wickets |
|--------|---------|
| YS Chahal | 213 |
| DJ Bravo | 207 |
| PP Chawla | 201 |

---

## Sample Predictions

**Mumbai Indians vs Chennai Super Kings**
- Mumbai Indians: 51.1% win probability
- Chennai Super Kings: 48.9% win probability
- Predicted Winner: Mumbai Indians

**Royal Challengers Bangalore vs Kolkata Knight Riders**
- Royal Challengers Bangalore: 49.4% win probability
- Kolkata Knight Riders: 50.6% win probability
- Predicted Winner: Kolkata Knight Riders

---

## How the Prediction Works

1. Calculate average runs per delivery for each team — this is the batting score
2. Count total wickets taken by each team — this is the bowling score
3. Normalize both scores between 0 and 1
4. Average the two scores to get an overall team strength score
5. When two teams are compared, divide their strength scores to calculate win probability percentage

---

## Technologies Used

- Python
- Pandas and NumPy
- Matplotlib and Seaborn
- Google Colab

---

## How to Run

1. Open the notebook in Google Colab
2. Upload deliveries.csv to the Colab session
3. Run all cells from top to bottom
4. Use the predict_winner function in the last cell to predict any match

Example:
```python
predict_winner("Mumbai Indians", "Chennai Super Kings")
predict_winner("Royal Challengers Bangalore", "Kolkata Knight Riders")
```

---

## Visualizations Generated

- Total runs scored by each IPL team (bar chart)
- Total wickets taken by each IPL team (bar chart)
- Top 10 batsmen by career runs (bar chart)
- Top 10 bowlers by career wickets (bar chart)
- Overall team strength score comparison (bar chart)

---

## Author

Sanivarapu Deekshitha
3rd Year B.Tech CSE — Vignan University, Guntur
GitHub: github.com/deekshitha875
Email: vu.241fa04797@gmail.com
