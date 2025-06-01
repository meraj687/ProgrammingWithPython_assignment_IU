# ProgrammingWithPython_assignment_IU


# Data Analysis and Visualization Project

This project performs data analysis and visualization on two different datasets. The code is presented here as a single Python script designed to be run in a Google Colab or Jupyter Notebook environment.

## Project Description

This project encompasses two main data analysis and visualization tasks:

1.  **Dataset 1: Ideal and Training Data Analysis**
    *   This task involves loading and processing training, ideal, and test datasets provided in CSV format.
    *   The core functionality includes identifying the best-fit ideal functions from a set of candidates that match the training data, using the Least Squares deviation method to minimize the difference between the training data points and the ideal function values.
    *   Subsequently, test data points are validated by checking if they fall within a specific tolerance (defined as the maximum deviation from the training data multiplied by the square root of 2) of their corresponding best-fit ideal function at the same 'x' value.
    *   Unit tests are included to ensure the integrity of the loaded datasets, checking for missing values, correct data types, and expected ranges for 'x' values.
    *   Visualizations using the Bokeh library are generated to display the ideal functions, the training data, and the relationship between the training data and their best-fit ideal functions.

2.  **Dataset 2: Nanofluid Heat Transfer Dataset Analysis**
    *   This task focuses on loading and analyzing a dataset related to nanofluid heat transfer properties.
    *   Initial processing involves selecting only the numeric columns for analysis.
    *   Unit tests are implemented to verify successful data loading, the presence of numeric columns after preprocessing, and the absence of missing values in the dataset.
    *   A variety of visualizations are created using different libraries to explore the dataset:
        *   A heatmap using Seaborn to visualize the correlation matrix of the numeric features.
        *   An interactive scatter plot using Bokeh to show the relationship between 'Flow Velocity' and 'Heat Transfer Coefficient'.
        *   A histogram using Seaborn and Matplotlib to show the distribution of 'Thermal Conductivity'.
        *   A bar plot using Seaborn and Matplotlib to compare 'Heat Transfer Coefficient' across different 'Nanoparticle Types'.
        *   A box plot using Seaborn and Matplotlib to visualize the distribution of 'Viscosity' for each 'Nanoparticle Type'.
        *   A 3D interactive scatter plot using Plotly to explore the relationship between 'Flow Velocity', 'Heat Transfer Coefficient', and 'Viscosity'.

## Setup and Execution

To run this project, follow these steps:

1.  **Environment:** The code is designed to be executed in a Google Colab environment or a Jupyter Notebook. These environments provide the necessary Python interpreter and libraries.
2.  **Mount Google Drive:** The script accesses dataset files stored in Google Drive. You will need to mount your Google Drive within the Colab/Jupyter environment. This is automatically handled by the code block that imports `google.colab.drive` and calls `drive.mount('/content/drive')`. When this line is executed, follow the on-screen instructions to authenticate and connect your Google Drive.
3.  **Dataset Files:** Ensure you have the following four CSV files uploaded to your Google Drive in a location accessible to the notebook:
    *   `ideal.csv`
    *   `train.csv`
    *   `test.csv`
    *   `nanofluid_heat_transfer_dataset.csv`
4.  **Dataset Paths:** You need to update the file paths in the script to accurately point to the location of these dataset files within your mounted Google Drive. Look for the variables holding file paths and modify them accordingly. Examples include:
    *   `ideal_path = "/content/drive/MyDrive/Aryaan_project_AI_MSc/Programming_with_Python_Assignment/ideal.csv"`
    *   `train_path = "/content/drive/MyDrive/Aryaan_project_AI_MSc/Programming_with_Python_Assignment/train.csv"`
    *   `test_path = "/content/drive/MyDrive/Aryaan_project_AI_MSc/Programming_with_Python_Assignment/test.csv"`
    *   `file_path_task2 = r"/content/drive/MyDrive/Aryaan_project_AI_MSc/Programming_with_Python_Assignment/nanofluid_heat_transfer_dataset.csv"`
5.  **Install Libraries:** The necessary libraries are typically pre-installed in a Google Colab environment. However, if you are running this in a local Jupyter Notebook or encounter `ModuleNotFoundError`s, you will need to install the required packages using pip. Open a terminal or the notebook's terminal and run the following command:
6.  Note: `unittest` is a standard Python library and does not require a separate pip installation. `google.colab` is specific to Google Colab and is not installed this way in standard Python.
7.  **Execution:** Execute the code cells within your Google Colab or Jupyter Notebook environment in the order they appear in the script. The `#%%` markers are often used by notebook environments to delineate code cells.

## Libraries and Modules Used

This project leverages several powerful Python libraries and modules for data handling, analysis, testing, and visualization:

*   **`pandas` (version X.Y.Z):** Essential for efficient data manipulation and analysis, primarily through its DataFrame structure. It's used for loading CSV files and performing data operations.
*   **`matplotlib` (version X.Y.Z):** A fundamental plotting library used for creating static visualizations, often in conjunction with Seaborn.
*   **`unittest` (built-in):** Python's standard library for writing and running unit tests, ensuring the code's correctness and data integrity.
*   **`bokeh` (version X.Y.Z):** Used to generate interactive visualizations, particularly scatter and line plots, suitable for web browser display. Key modules used are `bokeh.plotting` for creating figures and glyphs, `bokeh.io` for managing output, and `bokeh.models` for data sources like `ColumnDataSource`.
*   **`seaborn` (version X.Y.Z):** Built on top of Matplotlib, it provides a high-level interface for drawing attractive statistical graphics. Used for heatmaps, histograms, bar plots, and box plots.
*   **`numpy` (version X.Y.Z):** Provides support for large, multi-dimensional arrays and matrices, along with a large collection of high-level mathematical functions to operate on these arrays. Used for numerical computations, especially in the Least Squares calculation.
*   **`plotly` (version X.Y.Z):** A powerful interactive plotting library capable of creating complex and visually appealing graphs, including 3D plots. The `plotly.graph_objects` module is used to define the structure of the 3D scatter plot.
*   **`IPython.display` (version X.Y.Z):** Used in notebook environments to display various output types.
*   **`IPython` (version X.Y.Z):** Provides an enhanced interactive Python environment.
*   **`google.colab.drive` (specific to Google Colab):** A module within the Google Colab environment to facilitate mounting Google Drive.

*(Note: Please replace the placeholder version numbers "X.Y.Z" with the actual versions of the libraries you have installed or are using in your environment. You can typically check library versions using `pip show <library_name>` in a terminal or by running `import <library_name>; print(<library_name>.__version__)` in a Python environment.)*

## Code

The complete code for both tasks is contained within a single Python script. It includes class definitions, functions for data handling and visualization, and execution blocks that orchestrate the analysis and plotting. The script is designed to be run sequentially in a notebook environment.

## Results

Upon successful execution of the script, the following will be observed in the output of the notebook:

*   **Task 1:**
    *   Printed output indicating the identified best-fit ideal functions for each training column.
    *   Printed output showing a sample of the validated test data points, including the data point, the best-fit ideal function it matched, and the calculated deviation.
    *   Interactive Bokeh plots displaying:
        *   The ideal functions.
        *   The training data.
        *   The training data points overlaid with their corresponding best-fit ideal function lines.
    *   Output from the `unittest` execution, indicating whether the dataset integrity tests (missing values, data types, x-range) passed or failed.
*   **Task 2:**
    *   Printed output indicating the start and end of Task 2 execution and confirming successful visualization generation.
    *   Output from the `unittest` execution for Task 2, confirming successful data loading, numeric column presence, and absence of missing values.
    *   Static Matplotlib/Seaborn plots displaying:
        *   A heatmap of feature correlations.
        *   A histogram of Thermal Conductivity.
        *   A bar plot of Heat Transfer Coefficient by Nanoparticle Type.
        *   A box plot of Viscosity Across Nanoparticle Types.
    *   An interactive Bokeh scatter plot of Flow Velocity vs Heat Transfer Coefficient.
    *   An interactive Plotly 3D scatter plot of Flow Velocity, Heat Transfer Coefficient, and Viscosity.

## Potential Issues

*   **File Not Found Errors:** The most common issue is incorrect file paths for the datasets. Double-check that the paths in the script exactly match the location of the files in your mounted Google Drive.
*   **Empty or Corrupt Data:** The `DataHandler` class in Task 1 includes error handling for cases where the input CSV files are empty or corrupt. The script will print an error message if this occurs.
*   **Missing Columns:** The `get_best_fit_functions` method in Task 1 expects specific column names ('x' and subsequent numeric columns). If these are missing or misspelled in your input CSV files, a `KeyError` will be raised and printed.
*   **Library Installation:** If you are not using Google Colab, ensure all necessary libraries are installed in your Python environment using the provided `pip` command.
*   **Plotly in Colab:** While Plotly is generally well-supported in Colab, occasional issues with interactive plot rendering can occur. If the 3D plot does not display correctly, ensure your Colab session is healthy and try re-running the cell.
*   **Google Drive Mounting Issues:** Ensure you successfully complete the Google Drive authentication and mounting process when prompted.


Flowchart Description for Task 1: Function Mapping and Data Validation
This flowchart outlines the execution flow of the Task 1 script.

    A[Start] --> B{Mount Google Drive?};
    B -- Yes --> C[Mount Google Drive];
    B -- No --> D[Proceed without mounting]; % Assuming local files are used, although the code currently expects Drive
    C --> E[Initialize DataHandler <br/> (Load ideal.csv, train.csv)];
    D --> E;
    E --> F{Data Loading Successful?};
    F -- No --> G[Handle Loading Errors <br/> (e.g., File Not Found, Empty)];
    G --> H[End with Error];
    F -- Yes --> I[Get Best Fit Functions];
    I --> J{Best Fit Calculation Successful?};
    J -- No --> K[Handle Best Fit Errors];
    K --> H;
    J -- Yes --> L[Plot Ideal Data <br/> (Bokeh)];
    L --> M[Plot Training Data <br/> (Bokeh)];
    M --> N[Plot Best Fit <br/> (Bokeh)];
    N --> O[Validate Test Data <br/> (Load test.csv, check points)];
    O --> P{Test Data Validation Successful?};
    P -- No --> Q[Handle Validation Errors];
    Q --> H;
    P -- Yes --> R[Run Unit Tests <br/> (TestDatasetIntegrity)];
    R --> S{Unit Tests Pass?};
    S -- No --> T[Report Unit Test Failures];
    T --> U[End];
    S -- Yes --> U;
    H --> U;
Use code with caution
Explanation of Nodes:

A [Start]: The beginning of the program execution.
B {Mount Google Drive?}: A decision point checking if Google Drive needs to be mounted (as is the case in the provided code).
C [Mount Google Drive]: The process of connecting to Google Drive.
D [Proceed without mounting]: An alternative path if data is assumed to be local (less relevant for the provided Colab code).
E [Initialize DataHandler (Load ideal.csv, train.csv)]: Creating an instance of the DataHandler class, which involves reading the ideal and training CSV files.
F {Data Loading Successful?}: A decision point checking if the data loading process encountered any errors.
G [Handle Loading Errors (e.g., File Not Found, Empty)]: The process of catching and reporting errors during data loading.
H [End with Error]: The program terminates due to a critical error.
I [Get Best Fit Functions]: Calculating the best-fit ideal function for each training column.
J {Best Fit Calculation Successful?}: A decision point checking if the best fit calculation completed without errors.
K [Handle Best Fit Errors]: The process of catching and reporting errors during best fit calculation.
L [Plot Ideal Data (Bokeh)]: Generating the visualization for the ideal functions.
M [Plot Training Data (Bokeh)]: Generating the visualization for the training data.
N [Plot Best Fit (Bokeh)]: Generating the visualization showing the training data and their best-fit ideal functions.
O [Validate Test Data (Load test.csv, check points)]: Loading the test dataset and validating each point against the best-fit functions.
P {Test Data Validation Successful?}: A decision point checking if the test data validation completed without errors.
Q [Handle Validation Errors]: The process of catching and reporting errors during test data validation.
R [Run Unit Tests (TestDatasetIntegrity)]: Executing the unit tests for data integrity.
S {Unit Tests Pass?}: A decision point checking if all unit tests passed.
T [Report Unit Test Failures]: Reporting which unit tests failed.
U [End]: The program finishes execution.


Flowchart Description for Task 2: Nanofluid Heat Transfer Dataset Analysis
This flowchart outlines the execution flow of the Task 2 script.

    A[Start] --> B{Mount Google Drive?};
    B -- Yes --> C[Mount Google Drive];
    B -- No --> D[Proceed without mounting]; % Less relevant for provided Colab code
    C --> E[Load Data <br/> (nanofluid_heat_transfer_dataset.csv)];
    D --> E;
    E --> F{Data Loaded Successfully?};
    F -- No --> G[Handle Data Loading Errors];
    G --> H[End with Error];
    F -- Yes --> I[Preprocess Data <br/> (Select Numeric Columns)];
    I --> J[Run Unit Tests <br/> (TestNanofluidDataset)];
    J --> K{Unit Tests Pass?};
    K -- No --> L[Report Unit Test Failures];
    L --> M[End];
    K -- Yes --> N[Plot Heatmap];
    N --> O[Plot Bokeh Scatter Plot];
    O --> P[Plot Histogram];
    P --> Q[Plot Bar Plot];
    Q --> R[Plot Box Plot];
    R --> S[Plot Plotly 3D Scatter Plot];
    S --> T[Print Success Message];
    T --> M;
    H --> M;
Use code with caution
Explanation of Nodes:

A [Start]: The beginning of the program execution.
B {Mount Google Drive?}: A decision point checking if Google Drive needs to be mounted.
C [Mount Google Drive]: The process of connecting to Google Drive.
D [Proceed without mounting]: An alternative path if data is assumed to be local.
E [Load Data (nanofluid_heat_transfer_dataset.csv)]: Calling the load_data function to read the CSV file into a DataFrame.
F {Data Loaded Successfully?}: A decision point checking if the data loading process was successful.
G [Handle Data Loading Errors]: The process of handling potential errors during data loading.
H [End with Error]: The program terminates due to a critical error.
I [Preprocess Data (Select Numeric Columns)]: Calling the preprocess_data function to keep only numeric columns.
J [Run Unit Tests (TestNanofluidDataset)]: Executing the unit tests defined in the TestNanofluidDataset class.
K {Unit Tests Pass?}: A decision point checking if all unit tests passed.
L [Report Unit Test Failures]: Reporting which unit tests failed.
M [End]: The program finishes execution.
N [Plot Heatmap]: Generating the heatmap visualization.
O [Plot Bokeh Scatter Plot]: Generating the Bokeh scatter plot.
P [Plot Histogram]: Generating the histogram.
Q [Plot Bar Plot]: Generating the bar chart.
R [Plot Box Plot]: Generating the box plot.
S [Plot Plotly 3D Scatter Plot]: Generating the interactive 3D scatter plot.
T [Print Success Message]: Printing a confirmation message indicating successful execution.
You can use these descriptions to create visual flowcharts using online tools or drawing software.
