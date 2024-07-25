# Nunam---Two-Fold-Dashboard-



### Code Description

1. **Import Libraries:**
   - `numpy` and `pandas` are imported for numerical operations and data manipulation.
   - `requests` is used for making HTTP requests.
   - `dash`, `dash_core_components`, `dash_html_components`, and `plotly.express` are imported to build and visualize the web dashboard.

2. **Define Functions and Load Excel Files:**
   - `load_excel_files(file_paths, cell_id)`: This function reads Excel files from the provided file paths, adds a 'CellId' column, and combines data from all sheets into a dictionary of DataFrames.
   - `file_paths_5308` and `file_paths_5329` specify the paths to Excel files for two different cell IDs.
   - `dfs_5308` and `dfs_5329` are populated with data from these files using the `load_excel_files` function.

3. **Calculate State of Health (SoH):**
   - `discharge_capacities` dictionary defines the discharge capacities for each cell.
   - `calculate_soh(discharge_capacity, nominal_capacity)` function computes the State of Health by comparing the discharge capacity to the nominal capacity.
   - `soh` dictionary calculates the SoH for each cell and prints the results.

4. **Install and Check Packages:**
   - Checks for the installation of `dash`, `plotly`, and other dependencies, providing warnings for invalid distributions and errors for any issues encountered during installation.

5. **Initialize the Dash App:**
   - Creates a Dash app instance.
   - `fetch_cell_data(cell_id)` function sends a request to a local API to fetch data for a specific cell ID and returns it as a DataFrame.

6. **Define Layout and Callbacks:**
   - `app.layout` sets up the layout of the dashboard with buttons and dropdowns to navigate between different views and data.
   - `toggle_dropdown_visibility(n_clicks)` controls the visibility of the dropdown menu based on button clicks.
   - `display_page(dashboard_n_clicks, cell_id)` determines which content to display based on the button clicked or the selected cell ID.
   - `create_cell_visualizations(cell_id)` generates visualizations (line graphs) for the selected cell ID using Plotly.

7. **Run the Server:**
   - The application is run on a local server with debug mode enabled on port 8080.
   
8. **Added Small GIF:**
   - Add a small GIF of the UI dashboard in a working situation to show its workings and usability.
   - ![Dashboard GIF](path/to/your/dashboard.gif)


---

---

This code sets up a Dash application that dynamically loads Excel data, calculates State of Health for battery cells, and provides interactive visualizations based on user input provided.
