# Lumel Backend Project

This repository contains the backend code for the Lumel project, focusing on historical sales data analysis. The project involves efficient data handling, normalization, API design, and core analysis calculations.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/YaswanthAdari12/Lumel_backend.git
    cd Lumel_backend
    ```

2. Set up a virtual environment and activate it:
    ```bash
    python3 -m venv venv
    source venv/bin/activate
    ```

3. Install the required dependencies:
    ```bash
    pip install pandas
    pip install numpy
    pip install flask
    ```

## Usage

1. Ensure your data files are in the correct format and placed in the `data/` directory.
2. Run the Jupyter notebook to preprocess the data:
    ```bash
    jupyter notebook Lumel_backend.ipynb
    ```
3. Start the Flask API server:
    ```bash
    python app.py
    ```

## API Endpoints

### Refresh Data

- **Endpoint**: `/refresh`
- **Method**: `POST`
- **Description**: Trigger data refresh.

### Total Sales by Product

- **Endpoint**: `/total_sales_by_product`
- **Method**: `GET`
- **Description**: Get total sales by product within a specified date range.
- **Query Parameters**:
  - `start_date`: The start date for the sales data (YYYY-MM-DD).
  - `end_date`: The end date for the sales data (YYYY-MM-DD).
  - `limit`: The number of top products to retrieve.

## Data Processing

The data processing is done using the `Lumel_backend.ipynb` Jupyter notebook, which includes:

1. **Loading Data in Chunks**:
    - Loading data from CSV files in chunks for efficient processing.

2. **Renaming Columns**:
    - Standardizing column names across different data tables (orders, customers, products, order details).

3. **Database Interaction**:
    - Connecting to an SQLite database.
    - Inserting preprocessed data into the database.
    - Viewing table information using `pandas`.
