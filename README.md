# Netflix Movies & TV Shows Analysis \| Power BI

An interactive Power BI project exploring Netflix movies and TV shows
through IMDb ratings, vote counts, release-year trends, runtime, and age
certification. The project uses Power Query for data preparation and
Power BI visuals to investigate seven business questions.

## Project Overview

This project analyzes a Netflix movies-and-TV-shows dataset to identify
patterns in content popularity, release-year distribution, IMDb ratings,
audience voting, runtime, and age certification. The report is organized
into **two Power BI pages** and includes slicers that let viewers
explore the data by release year and content type.

**Project type:** Exploratory data analysis and business intelligence\
**Primary tools:** Microsoft Power BI Desktop, Power Query, Microsoft
Excel\
**Dataset:** `Netflix TV Shows and Movies.xlsx`\
**Report file:** `Netflix Power BI Project.pbix`

## Business Questions

The project was designed around these questions:

1.  **Which movie and TV show performed best overall across the last 50
    years?**\
    Compare titles using the report's `Rating Votes` visual metric to
    surface popular titles.
2.  **How many movies and shows are represented across recent years, and
    is the dataset skewed toward the last 20 years?**\
    Examine the number of titles by release year and the concentration
    of recent releases.
3.  **How has the average IMDb score changed over time?**\
    Explore whether ratings appear to improve, decline, or fluctuate
    across release years.
4.  **Have more people started voting for movies and shows over the last
    50 years?**\
    Track IMDb vote counts across release years.
5.  **How has runtime changed over time?**\
    Compare runtime trends across release years.
6.  **How does age certification relate to movie ratings?**
7.  **How does age certification relate to TV show ratings?**

## Tools & Skills Demonstrated

-   **Power Query:** data inspection, column type preparation, and
    missing-value handling
-   **Power BI:** report design, visual selection, slicers, and
    interactive exploration
-   **Data analysis:** trend analysis, category comparisons, and
    popularity/rating exploration
-   **Data quality:** identifying missing values and choosing a
    documented treatment
-   **Business communication:** translating questions into charts and
    observations

## Dataset

The supplied Excel workbook contains **5,283 rows and 11 columns**. The
fields include:

  Column                Description
  --------------------- ---------------------------------------
  `index`               Row/index field in the source dataset
  `id`                  Content identifier
  `title`               Movie or TV show title
  `type`                Content type (`MOVIE` or `SHOW`)
  `description`         Text description of the content
  `release_year`        Release year
  `age_certification`   Age/content certification
  `runtime`             Runtime value recorded in the dataset
  `imdb_id`             IMDb identifier
  `imdb_score`          IMDb score
  `imdb_votes`          IMDb vote count

The supplied dataset spans release years **1953--2022**. It contains
**3,407 movies** and **1,876 shows**.

## Data Cleaning & Preparation

The project documentation shows the following Power Query preparation
steps:

1.  Imported the Excel workbook and selected the
    `Netflix TV Shows and Movies` table.
2.  Promoted the first row to column headers.
3.  Reviewed column quality and data types in Power Query Editor.
4.  Handled missing values in selected fields:
    -   Replaced missing `age_certification` values with `NA` so they
        could be treated as an explicit category.
    -   Replaced missing `imdb_votes` values with **2,279**, the median
        noted in the project material.
5.  Used the prepared data as the source for the Power BI report.

**Data-quality note:** The source workbook contains 2,285 missing values
in `age_certification` and 16 missing values in `imdb_votes`. The
cleaning choices above are those documented in the supplied project
material; they should not be interpreted as a universal rule for every
dataset. The source workbook also contains a small number of missing
descriptions, and the supplied material does not document a specific
treatment for those rows.

## Dashboard & Visualizations

The Power BI report contains two pages. Across the report, the visuals
support the following analyses:

-   **Most popular titles:** a column chart comparing titles using the
    report's `Rating Votes` field.
-   **Title count by release year:** an area chart showing how the
    number of records changes over time.
-   **IMDb votes by release year:** a time-trend visual for audience
    voting activity.
-   **IMDb score and votes over time:** a combination chart for
    comparing vote volume with the rating trend.
-   **Runtime by release year:** a line chart for exploring changes in
    runtime.
-   **Age certification and IMDb score:** a chart for comparing rating
    patterns across certification categories.
-   **Interactive filters:** release-year range and content type
    (`MOVIE` / `SHOW`) slicers.

Use the slicers to narrow the release-year range or focus on one content
type and observe how the visuals respond.

### Dashboard Preview

### Page 1
![Netflix Dashboard Page 1](Dashboard%20Page%201.png)

### Page 2
![Netflix Dashboard Page 2](Dashboard%20Page%202.png)

## Key Observations from the Supplied Dataset

The following are descriptive observations calculated from the supplied
Excel workbook, not claims about Netflix's complete catalogue:

-   **2019 has the most records** in the supplied dataset, with 749
    titles; 2018 follows with 733.
-   The dataset contains more movies (3,407) than shows (1,876).
-   The average IMDb score in the supplied data is approximately **6.27
    for movies** and **7.02 for shows**.
-   The average recorded runtime is approximately **101.5 minutes for
    movies** and **38.6 for shows**. Interpret this comparison in the
    context of how runtime is represented in the source data.
-   The source dataset has substantial missingness in
    `age_certification`; the project treats missing certification as
    `NA` rather than assigning a guessed certification.

These are dataset-level summaries. Ratings and vote counts are not proof
of quality or causation, and the dataset should not be treated as a
complete or current inventory of Netflix content.

## Repository Structure

Keep the following files together in the GitHub repository:

``` text
netflix-powerbi-analysis/
├── README.md
├── Netflix Power BI Project.pbix
├── Netflix TV Shows and Movies.xlsx
└── images/
    └── dashboard-preview.png
```

The `images/dashboard-preview.png` file is included in the companion
bundle for this README. Upload it to the `images/` folder in your
repository so the preview renders on GitHub.

## How to Explore the Project

1.  Download or clone this repository.
2.  Open `Netflix Power BI Project.pbix` in **Power BI Desktop**.
3.  If Power BI prompts you to locate the source workbook, point it to
    `Netflix TV Shows and Movies.xlsx` and refresh the data.
4.  Navigate between the two report pages.
5.  Use the release-year and content-type slicers to explore the
    visuals.
6.  Review the Power Query steps in **Transform data** to understand the
    documented data preparation.

## Limitations

-   The analysis is limited to the records and fields in the supplied
    dataset.
-   Missing values and the selected imputation method can affect
    summaries and visual interpretation.
-   The latest years may be incomplete in the source data, so lower
    counts for the most recent year should be interpreted cautiously.
-   IMDb scores and vote counts reflect the dataset's recorded values
    and can change over time.

## Conclusion

This project demonstrates an end-to-end introductory BI workflow:
inspecting a dataset, preparing data in Power Query, translating
business questions into visuals, and building an interactive two-page
Power BI report. It provides practice in data cleaning, trend analysis,
categorical comparison, and communicating data-backed observations.

------------------------------------------------------------------------

**Author:** Add your name here\
**Tools:** Power BI Desktop · Power Query · Excel
