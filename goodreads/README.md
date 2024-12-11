# Dataset Analysis Report

## Insights from LLM

# README.md

## Dataset Overview
This dataset contains information about books, including their IDs, authors, publication years, ratings, and other relevant features. The dataset comprises 10,000 records, reflecting the characteristics of various books and reader interactions, such as ratings and reviews.

## Summary Statistics
The following are key summary statistics for the dataset:

- **Number of Records**: 10,000
- **Key Columns**:
  - `book_id`: Unique identifier for each book
  - `goodreads_book_id`: Goodreads-specific book identifier
  - `authors`: Authors of the book
  - `average_rating`: Average rating score from users
  - `ratings_count`: Total number of ratings received by the book
  - `ratings_x`: Count of ratings in incremental categories (1 to 5)
  - `Cluster`: Designation of cluster group (used for clustering analysis)

| Statistic       | book_id       | goodreads_book_id        | average_rating | ratings_count | ratings_1 | ratings_2 | ratings_3 | ratings_4 | ratings_5 | Cluster |
|------------------|---------------|---------------------------|----------------|----------------|-----------|-----------|-----------|-----------|-----------|---------|
| Count            | 10,000        | 10,000                    | 10,000         | 10,000         | 10,000    | 10,000    | 10,000    | 10,000    | 10,000    | 9,397    |
| Mean             | 5000.5        | 5,264,697                 | 3.85           | 5305.4         | 1,900.5   | 2,271.5   | 3,084.1   | 19,965.7  | 23,789.8  | 0.379    |
| Standard Deviation | 2886.9      | 7,575,462                 | 0.87           | 5,780.4        | 147.8     | 187.2     | 295.8     | 5,144.7   | 7,976.9   | 0.741    |
| Minimum          | 1             | 1                         | 0.0            | 738            | 0         | 0         | 0         | 750        | 754       | 0       |
| 25th Percentile  | 2,500.75      | 46,275                    | 3.5            | 1,300.4        | 0         | 1         | 1         | 54.07      | 59.5      | 0       |
| Median           | 5,000.5       | 394,965                   | 4.0            | 5,242          | 1         | 2         | 3         | 8,269.5   | 8,836     | 0       |
| 75th Percentile  | 7,500.25      | 9,382,225                 | 4.5            | 19,965         | 7         | 8         | 10        | 16,023.5  | 17,304.5  | 1       |
| Maximum          | 10,000        | 33,288,640                | 5.0            | 1,481,305      | 3,011,543  | 3,011,543 | 3,011,543 | 1,481,305 | 3,011,543 | 3       |

## Missing Values
The dataset contains missing values in some columns as follows:

- `isbn`: 700 missing values
- `isbn13`: 585 missing values
- `original_publication_year`: 21 missing values
- `original_title`: 585 missing values
- `language_code`: 1,084 missing values

Handling these missing values will be essential for ensuring the integrity of analysis and resulting models.

## Visualizations
To derive insights from the dataset, two primary visualizations have been created:

1. **Correlation Heatmap**:
   - Displays the correlation between various numerical features within the dataset.
   - Saved as: [correlation_heatmap.png](./correlation_heatmap.png)

2. **KMeans Clustering**:
   - Visualizes the clustering of books based on features such as average ratings and total rating counts.
   - Clustered data saved as: [clustered_data.csv](./clustered_data.csv)

## Analysis Steps
1. **Data Cleaning**: Assess and handle missing values to ensure the dataset is complete for analysis.
2. **Exploratory Data Analysis (EDA)**: Generate summary statistics and visualizations to uncover relationships and patterns in the data.
3. **Clustering Analysis**: Apply KMeans clustering to group books into categories based on ratings and interactions, followed by visualization.
4. **Correlation Analysis**: Utilize a correlation heatmap to identify relationships among numerical features.

## Key Findings
- The average book rating across the dataset appears to be approximately 3.85, indicating a generally favorable response from readers.
- Significant variability exists in the count of ratings per book, with some books receiving a disproportionately high number of ratings compared to others.
- Various clusters emerge from KMeans clustering, potentially indicating different reader preferences or book genres based on ratings.

This README provides an overview and analysis of the dataset, outlining its characteristics, visual insights, and the methodological approach used for analysis. Further exploration and modeling can build on this groundwork to derive more specific insights and predictions.

## Correlation Heatmap
![Correlation Heatmap](.\correlation_heatmap.png)

## KMeans Clustering
Clustered data saved as [clustered_data.csv](.\clustered_data.csv)