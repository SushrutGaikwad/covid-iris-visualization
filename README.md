# COVID and Iris Dataset Visualization

This project explores interactive data visualization using the `plotly` and `ggplot2` libraries in R. It contains two parts:

1. Visual exploration of the famous **Iris flower dataset**.
2. Analysis and visualization of **COVID-19 case trends** across US states using the NYTimes dataset.

The focus is on using **interactive visualizations**, **long-format transformations**, and **animated maps** to derive insights and support analysis.

---

## 🧑‍💻 Author

**Sushrut Gaikwad**  
ID: 50604159  
Date: February 16, 2025

---

## 📁 Project Structure

```{r}
covid-iris-visualization/
├── data/
│   ├── iris.csv                    # Iris dataset (from UCI / course)
│   └── us-states.csv               # COVID data from NYTimes GitHub
├── scripts/
│   └── analysis.Rmd                # R Markdown with full analysis and plots
├── output/
│   └── analysis.html               # Rendered HTML notebook
├── README.md                       # This file
├── LICENSE                         # Project license (MIT)
├── .gitignore                      # Files/folders to ignore in Git
└── covid-iris-visualization.Rproj  # RStudio project file
```

---

## 📦 Requirements

- **R**
- **RStudio**
- Required Packages:
  - `tidyverse`
  - `plotly`
  - `maps`
  - `knitr`

---

## 🌸 Part 1: Iris Dataset Visualization (26 points)

### 🔹 Dataset Overview

The Iris dataset includes measurements for three species of iris flowers: Setosa, Versicolor, and Virginica.

### 🔹 What I Did

- Loaded `iris.csv` and set factor types for species.
- Displayed head of the dataset to inspect structure.
- Created:
  - An interactive **histogram** using `plotly` grouped by species.
  - The same plot using `ggplot2` and converted it to `plotly` via `ggplotly()`.
- Transformed the data into long format using `pivot_longer()` to generate:
  - A **2x2 grid of histograms** for each metric (`Sepal.Length`, `Sepal.Width`, etc.)
  - A **2x2 grid of box plots** for the same metrics
- From these visualizations, determined that:
  - `Petal.Length` and `Petal.Width` are best at separating species.
- Plotted:
  - A **2D scatter plot** (`Petal.Length` vs `Petal.Width`) colored by species.
  - A **3D scatter plot** with three top metrics.
- Provided detailed observations on how well species can be separated based on these features.

---

## 🦠 Part 2: US COVID-19 Case Analysis (34 points)

### 🔹 Dataset Overview

The dataset (`us-states.csv`) contains daily cumulative COVID-19 cases and deaths by US state. Sourced from the [New York Times GitHub repository](https://github.com/nytimes/covid-19-data).

### 🔹 What I Did

- Loaded the dataset and ensured correct data types (`date`, `state`, `cases`, `deaths`).
- Created a new variable: **monthly new cases**, calculated by grouping by state and month and differencing cumulative counts.
- Generated:
  - A **multi-line interactive plot** showing monthly new cases across all US states using `plotly`.
    - Included an interactive dropdown to isolate states.
  - A **line plot just for New York** to explore state-specific trends.
  - Identified the **month with peak cases in NY**, and visualized that month's data:
    - Using a **US choropleth map**, colored by new cases per state.
- Built an **animated choropleth map** that:
  - Shows how case counts change month-by-month across all states.
  - Can be played, paused, and explored over time.
- Compared the different visualization types (static line plots vs interactive map) and explained when each is more useful.

---

## 📈 Visual Outputs

- Interactive histograms, box plots, scatter plots for Iris dataset
- 2D and 3D scatter plots showing separation between species
- Multi-line plot for state-wise COVID trends
- Choropleth and animated maps for spatial COVID analysis
- Scree plots and PCA biplots (in future extension)

---

## 🚀 How to Run

1. Clone or download this repository
2. Open `covid-iris-visualization.Rproj` in RStudio
3. Open `scripts/analysis.Rmd`
4. Click **Knit** to render as HTML or PDF

---

## 🎯 Learning Outcomes

- Mastered the use of `plotly` for building interactive plots
- Transformed wide-form data to long-form for faceted visualizations
- Learned how to:
  - Integrate multiple interactive visualizations in a single report
  - Animate data across time in a choropleth map
  - Perform basic exploratory analysis using visuals
- Practiced clean, reproducible R coding using tidyverse principles

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 💬 Feedback

Questions or suggestions? Feel free to fork the repo, raise issues, or contact me.
