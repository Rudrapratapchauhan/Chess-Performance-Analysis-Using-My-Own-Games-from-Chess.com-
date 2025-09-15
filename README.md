# Chess Performance Analysis

This project analyzes personal chess game data from a PGN file to gain insights into performance trends, opening effectiveness, and results against different opponent ratings.

## Setup

1.  **Mount Google Drive:** The notebook starts by mounting Google Drive to access the PGN file stored there.
2.  **Install Libraries:** Necessary libraries (`chess` and `pandas`) are installed.
3.  **Import Libraries:** The required libraries are imported.

## Data Loading and Wrangling

1.  **Load PGN Data:** Chess game data is loaded from a PGN file using the `chess.pgn` library.
2.  **Extract Game Information:** Key information such as date, players, result, opening, time control, and player ratings (WhiteElo and BlackElo) is extracted from the PGN headers and stored in a list of dictionaries.
3.  **Create DataFrame:** The extracted game information is converted into a pandas DataFrame for easier manipulation and analysis.
4.  **Calculate Opponent Rating:** A column is added to the DataFrame to store the rating of the opponent for each game.
5.  **Calculate Your Rating:** A column is added to the DataFrame to track your rating progression over time.

## Analysis and Visualization

The notebook includes code to generate various visualizations to analyze chess performance:

1.  **White vs Black Performance:** Calculates the number of wins as White and Black.
2.  **Win % by Opening:** Determines the win rate for different chess openings played.
3.  **Performance vs Opponent Rating:** Analyzes results based on the opponent's rating.
4.  **Win Rate by Opening (Bar Chart):** Visualizes the win rate for each opening.
5.  **Rating Progression Over Time (Line Chart):** Shows how the player's rating has changed over time.
6.  **Heatmap: Results vs Opponent Rating:** Visualizes the average result (win rate) against different bins of opponent ratings.
7.  **Distribution of Results (Pie Chart):** Displays the overall proportion of wins, losses, and draws.
8.  **Accuracy by Opening (Boxplot - Requires Accuracy Data):** (Note: This visualization requires accuracy data which is not typically in standard PGN files. If available, this plot can show the distribution of move accuracy for different openings.)

## How to Use

1.  Upload your PGN file to your Google Drive.
2.  Update the file path in the data loading cell (`/content/drive/My Drive/your_chess_games.pgn`) to point to your PGN file.
3.  Replace `"Rudra_Pratap18"` with your actual username in the relevant cells for calculating your rating and opponent rating.
4.  Run the cells sequentially to perform the analysis and generate the visualizations.
