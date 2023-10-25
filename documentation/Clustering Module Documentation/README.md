# Clustering Module Documentation

The Clusterizare module employs the K-Means clustering algorithm to group data points into clusters based on certain attributes. It showcases a part of a Windows Form Application allowing users to load data, execute clustering, and view the results in a structured table with color-coded clusters.

## Features

1. **Data Loading:**
   - Load data from specified CSV files into a DataTable, which is then displayed on a DataGridView.

2. **Clustering:**
   - Utilize the K-Means algorithm (from external libraries) to categorize data points into clusters.
   - Visualize clustering results by color-coding rows in the DataGridView based on cluster membership.

3. **Sorting:**
   - Determine the bounds (min and max values) of the clusters in the data, potentially for further graphical visualization or analysis.

4. **Closing:**
   - Ability to close the form through the GUI.

## Key Methods and Functionalities

- `readCSVToolStripMenuItem_Click`: Handles data loading from CSV files and populates the DataTable and DataGridView.
- `clusterToolStripMenuItem_Click`: Initiates the clustering process, updates the DataGridView with clustering results, and color-codes rows based on cluster membership.
- `sort`: Finds the minimum and maximum values of the data points, presumably to determine the bounds of clusters.
- `exitToolStripMenuItem_Click`: Provides the ability to close the form through the GUI.

## External Dependencies

- `ComponentLearning_1`, `ComponentLearning_2`, and `ComponentLearningAnalizaMultidim`: Libraries containing the K-Means algorithm and other utilities required for clustering.

## Usage

1. **Loading Data:**
   - Trigger the `readCSVToolStripMenuItem_Click` method, typically through a button click or other UI interaction, to load data from the specified CSV files.
   
2. **Performing Clustering:**
   - Trigger the `clusterToolStripMenuItem_Click` method, typically through a button click or other UI interaction, to perform clustering and view the results in the DataGridView.

3. **Closing the Form:**
   - Trigger the `exitToolStripMenuItem_Click` method, typically through a button click or other UI interaction, to close the form.

