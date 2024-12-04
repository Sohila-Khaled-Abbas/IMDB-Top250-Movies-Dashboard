# DAX Formulas Used in IMDB Top 250 Movies Dashboard

This document provides an overview of the key DAX formulas used in the IMDB Top 250 Movies Dashboard. These formulas are designed to calculate various metrics, such as average ratings, movie counts, and dynamic color assignments based on rating ranges.

---

## 1. **Decade and Rating Group**

This formula combines the movie's decade with its rating range. The rating groups are divided into ranges such as 8-9 and 9-10 to provide a more granular view of the ratings.

```DAX
Decade and Rating Group = 
    VAR Decade = FLOOR([Year], 10)
    VAR RatingGroup = 
        SWITCH(
            TRUE(),
            [IMDB Rating] >= 9, "9-10",
            [IMDB Rating] >= 8, "8-9",
            "Below 8"
        )
    RETURN 
        Decade & " | " & RatingGroup
```

**Explanation**:
- **Decade**: Extracts the decade from the movie's release year.
- **RatingGroup**: Categorizes the movie's rating into specific ranges (8-9, 9-10, etc.).

---

## 2. **Average Rating**

This formula calculates the average IMDB rating across all movies in the dataset.

``` DAX
Average Rating = AVERAGE('Movies'[IMDB Rating])
```

**Explanation**:
- **AVERAGE**: Calculates the mean of the IMDB ratings for all movies.

---

## 3. **Avg Rating by Decade**

This formula computes the average rating per decade, allowing for insights into rating trends over time.

``` DAX
Avg Rating by Decade = 
    CALCULATE(
        AVERAGE('Movies'[IMDB Rating]),
        ALLEXCEPT('Movies', 'Movies'[Decade])
    )
```

**Explanation**:
- **CALCULATE**: Recalculates the average rating in the context of each decade.
- **ALLEXCEPT**: Keeps the decade context and removes any other filters.

---

## 4. **Count of Movies**

This formula counts the number of movies in the dataset.

``` DAX
Count of Movies = COUNTROWS('Movies')
```

**Explanation**:
- **COUNTROWS**: Returns the number of rows (movies) in the 'Movies' table.

---

## 5. **IMDB Rating Color**

This formula dynamically assigns a color based on the movie's average rating. Ratings above 9 are marked as green, between 8 and 9 as orange, and below 8 as red.

``` DAX
IMDB Rating Color = 
    SWITCH(
        TRUE(),
        [IMDB Rating] >= 9, "Green",
        [IMDB Rating] >= 8, "Orange",
        "Red"
    )
```

**Explanation**:
- **SWITCH**: Checks the IMDB rating and assigns a color accordingly.
- The colors (Green, Orange, Red) correspond to the rating thresholds.

---

# Summary of DAX Formulas
- **Decade and Rating Group**: Combines movie decade with its rating range.
- **Average Rating**: Calculates the overall average rating of movies.
- **Avg Rating by Decade**: Computes the average rating for movies per decade.
- **Count of Movies**: Counts the total number of movies in the dataset.
- **IMDB Rating Color**: Assigns a color based on the movie's IMDB rating.
These DAX formulas are central to providing dynamic insights in the dashboard, enabling users to view ratings, trends, and categorizations based on movie decades and ratings.

---

# Lessons Learned and Challenges
## Performance Optimization
- Large datasets can slow down the performance when calculating averages or aggregating data. We optimized the use of `CALCULATE` and `ALLEXCEPT` to filter only relevant columns.

## Dynamic Color Assignment
- The dynamic color formula was particularly useful for improving the visual appeal of the dashboard. However, testing different colors for contrast and clarity was important to ensure accessibility.
