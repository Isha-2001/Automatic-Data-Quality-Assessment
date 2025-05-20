# Automatic Data Quality Assessment Dashboard

This project presents an interactive dashboard for assessing and visualizing the quality of tabular datasets. Built using Plotly Dash, the application provides insights into various data quality dimensions, aiding users in identifying and addressing potential issues in their datasets.

## Features

- **Missing Value Analysis**: Visual representation of missing data across columns.
- **Duplicate Detection**: Identification and count of duplicate records.
- **Data Type Distribution**: Overview of data types present in the dataset.
- **Statistical Summaries**: Key statistics like mean, median, standard deviation for numerical columns.
- **Interactive Visualizations**: Dynamic plots for better understanding of data distributions and anomalies.

## Text Preprocessing

While the primary focus is on data quality assessment, the application includes preprocessing steps to ensure accurate analysis:

- **Handling Missing Values**: Detection and optional imputation strategies.
- **Data Type Conversion**: Ensuring correct data types for each column.
- **Outlier Detection**: Identifying anomalies in numerical data.
- **Normalization**: Scaling data for uniformity in analysis.

## Visualization

The dashboard offers a range of visual tools:

- **Heatmaps**: To display correlations and missing data patterns.
- **Bar Charts**: For categorical data distribution.
- **Histograms**: To show frequency distributions of numerical data.
- **Box Plots**: For visualizing data spread and detecting outliers.

## Dataset

The application is designed to work with user-uploaded CSV files. Users can upload their datasets through the dashboard interface, upon which the application performs the quality assessment and displays the results interactively.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgments

- [Plotly Dash](https://dash.plotly.com/) for the interactive web application framework.
- [Pandas](https://pandas.pydata.org/) for data manipulation and analysis.
- [NumPy](https://numpy.org/) for numerical operations.
- [Matplotlib](https://matplotlib.org/) and [Seaborn](https://seaborn.pydata.org/) for data visualization support.
