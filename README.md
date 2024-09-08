
# OKC Thunder Player Rest Regular-Season Schedule Generator

This Shiny app generates a rest schedule for players of the Oklahoma City Thunder during the 2024-2025 regular season, based on NBA rest rules, player injuries, and other constraints. Users can customize the rest schedule by specifying injured players and a minimum number of rest days between games for star players. The app allows users to regenerate the schedule dynamically and outputs a table showing rest days for each game.

## Features

- **Rest Schedule Generation**: Automatically generates a rest schedule for the 2024-2025 season, applying NBA rest rules for star players.
- **Injury Consideration**: Users can select injured players, and the app will incorporate their injury periods into the schedule.
- **Customizable Rest Period**: Users can specify a minimum number of days between rest days for star players.
- **Dynamic Schedule Regeneration**: A "Generate Rest Schedule" button allows users to regenerate the rest schedule based on their inputs.

## Key Logic

1. **Player Rest Rules**: The app first ensures that star players adhere to the NBA’s rest guidelines (i.e., avoiding rest during nationally televised games and maintaining a minimum number of rest days between games).
2. **Injury Consideration**: Injured players (both star and non-star) are automatically included in the rest schedule for the duration of their injury period.
3. **Duplicate Player Prevention**: The app ensures that a player can only be rested once on any given game day, even if they are marked as injured and scheduled for rest due to other reasons.

## Usage Instructions

1. **Select Injured Player**: Use the dropdown to select any injured player from the list.
2. **Specify Injury Dates**: Select the start and end dates for the injury period.
3. **Set Rest Days**: Adjust the minimum number of rest days between games for star players.
4. **Generate Rest Schedule**: Click the "Generate Rest Schedule" button to create or update the rest schedule.

## Requirements

The app requires the following R packages:
- `shiny`
- `dplyr`
- `lubridate`

## How to Run
To run the app on the internet, copy and paste https://lucasqiu.shinyapps.io/okc4/ into your browser.

To run the app locally, clone this repository and open the R project in RStudio. Ensure that the required R packages are installed, then run the following command in your R console:

```R
shiny::runApp()
```

This will start the Shiny app in your default browser.

