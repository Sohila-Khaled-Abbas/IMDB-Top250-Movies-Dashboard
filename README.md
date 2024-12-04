# IMDB Top 250 Movies Dashboard

## Project Overview  
This Power BI project showcases an interactive dashboard that visualizes insights from the IMDB Top 250 Movies List. The dashboard provides an in-depth look at trends in movie ratings across different decades, highlights top-rated movies, and breaks down movie distributions based on rating ranges. By using dynamic measures and engaging visuals, this project aims to provide data-driven insights into the world of cinema.

## Features

### **Visualizations**  
- **Average Rating by Decade**: Displays the average ratings of movies per decade.
- **Movie Distribution by Decade and Rating Range**: Shows the distribution of movies within different rating ranges across decades.
- **Top 5 Movies by Rating**: Highlights the top-rated movies in the IMDB Top 250 list.

### **Measures**  
- **Decade and Rating Group**: Combines decade with rating ranges (8-9, 9-10).
- **Average Rating**: The average of IMDB ratings.
- **Avg Rating by Decade**: Uses DAX to calculate the average ratings per decade.
- **Count of Movies**: Counts the number of movies.
- **IMDB Rating Color**: Dynamically assigns colors based on average ratings (green, orange, red).
---

## Screenshots

### Welcome Page
![Welcome Page](images/welcome_page.png)

### Top 250 Movies Dashboard
![Top 250 Movies Dashboard](images/top_250_movies_dashboard.png)

### Details Page
![Details Page](images/details_page.png)

---
## Data Source
The data for this project is sourced from the [IMDB Top 250 Movies List](https://www.imdb.com/chart/top/?ref_=nv_mv_250&sort=rank%2Casc).

## Additional Materials  
- **Color Palette**: [IMDb Top 250 Movies Dashboard Color Theme](https://color.adobe.com/IMDb-Top-250-Movies-Dashboard-color-theme-ce09f718-0758-4029-b509-2821099fed74/)
- **IMDB Logo**: [IMDB Logo](https://en.m.wikipedia.org/wiki/File:IMDB_Logo_2016.svg)
- **Welcome Page Background**: [IMDB Top 250 Movie Poster](https://images-wixmp-ed30a86b8c4ca887773594c2.wixmp.com/f/901370a7-ec10-4044-901c-82a189cc8036/d38rnod-2f6cb815-011d-47a8-bb9f-448c20f994c9.jpg/v1/fill/w_1172,h_682,q_70,strp/imdb_top_250_movie_poster_by_saxon1964_d38rnod-pre.jpg?token=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJ1cm46YXBwOjdlMGQxODg5ODIyNjQzNzNhNWYwZDQxNWVhMGQyNmUwIiwiaXNzIjoidXJuOmFwcDo3ZTBkMTg4OTgyMjY0MzczYTVmMGQ0MTVlYTBkMjZlMCIsIm9iaiI6W1t7ImhlaWdodCI6Ijw9MzIwMCIsInBhdGgiOiJcL2ZcLzkwMTM3MGE3LWVjMTAtNDA0NC05MDFjLTgyYTE4OWNjODAzNlwvZDM4cm5vZC0yZjZjYjgxNS0wMTFkLTQ3YTgtYmI5Zi00NDhjMjBmOTk0YzkuanBnIiwid2lkdGgiOiI8PTU1MDAifV1dLCJhdWQiOlsidXJuOnNlcnZpY2U6aW1hZ2Uub3BlcmF0aW9ucyJdfQ.FcSQpnBlme8MsgOfMBtOUgWTDydsuIy1mPsgznkqdOw)

---

## Local Setup Guide  

1. Clone the repository:  
   ```bash
   git clone https://github.com/your-username/IMDB-Top250-Movies-Dashboard.git
   cd IMDB-Top250-Movies-Dashboard
    ```
2. Download and install [Power BI Desktop](https://www.microsoft.com/en-us/power-platform/products/power-bi/desktop).
3. Open `src/IMDB_Top250.pbix` in Power BI Desktop.
---

## GitHub Pages Showcase  

Use GitHub Pages to create a visually appealing project showcase.  

#### Suggested Design:  
- Include dashboard screenshots and interactive GIFs.  
- Highlight key metrics and trends derived from the dashboard.  
- Use a clean, professional theme like **Cayman** or **Minimal**.  

---

## Lessons Learned  

### **Challenge**: Creating dynamic color-coded measures for ratings.  
- **Solution**: Used SWITCH and logical conditions in DAX.  

### **Reflection**: Strengthened DAX skills and improved dashboard performance.  

---

## Collaboration Opportunities  

We welcome contributions! If you'd like to collaborate:  
- Familiarity with Power BI and DAX is required.  
- Ensure code adheres to repository standards.  

#### **Contributing Guidelines**  
1. Fork the repository.  
2. Create a feature branch:  
   ```bash
   git checkout -b feature-name
    ```
3. Submit a pull request with a detailed description.
---

## License  
This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.
