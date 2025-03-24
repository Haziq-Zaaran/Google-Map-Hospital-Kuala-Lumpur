```markdown
# Kuala Lumpur Hospitals Data Extraction Using Power BI

## Project Overview

This project demonstrates how to scrape and analyze hospital data in Kuala Lumpur using Power BI. The extracted data includes essential details such as hospital name, type, rating, location, operation hours, and phone number. After processing the data, it is validated, cleaned, and saved in CSV format for further analysis or reporting.

---

## Problem Statement

A healthcare consulting firm has requested detailed information on hospitals in Kuala Lumpur to support their market research and operational planning. They require a structured dataset containing hospital names, types (e.g., private or public), ratings, locations, operation hours, and phone numbers. To address this need, I utilized Power BI's web scraping capabilities to extract and transform the required data from Google Search results. The final dataset is validated and cleaned to ensure its accuracy and usability.

---

## Features

* **Web Scraping with Power BI**:
  - Extracts hospital data directly from Google Search results for "hospitals in Kuala Lumpur."
* **Data Extraction**:
  - Collects the following details for each hospital:
    - Hospital Name
    - Type (e.g., Private or Public)
    - Rating (from Google Reviews)
    - Location (Address)
    - Operation Hours
    - Phone Number
* **Data Validation**:
  - Ensures all extracted fields are complete and correctly formatted.
  - Validates phone numbers and operation hours for consistency.
* **Data Cleaning**:
  - Removes irrelevant or incomplete entries.
  - Standardizes address formats.
  - Handles missing values appropriately.
* **CSV Export**:
  - Saves the validated and cleaned data into a CSV file for easy integration with other tools.

---

## Tech Stack

* **Power BI Desktop**:
  - Web scraping via Power Query.
  - Data modeling and visualization.
  - Data validation and cleaning.
* **Power Query (M Code)**:
  - Used for HTML parsing, cleaning, validation, and transformation.
* **CSV Export**:
  - Saves the transformed data in CSV format.

---

## How It Works

1. **Connect to Web Source**:
   - Use Power BI's "Get Data > Web" feature to connect to Google Search results for "hospitals in Kuala Lumpur."
2. **HTML Parsing**:
   - Extract relevant tables or lists containing hospital details using Power Query's `Html.Table` function.
3. **Data Validation**:
   - Check for completeness of all required fields (e.g., no missing phone numbers or ratings).
   - Validate data formats (e.g., numeric ratings between 1-5).
4. **Data Cleaning**:
   - Remove unnecessary columns and irrelevant rows.
   - Standardize formats for addresses and phone numbers.
   - Handle missing values by imputation or removal.
5. **CSV Export**:
   - Save the cleaned dataset as a CSV file using Power BI’s export functionality.

---

## Example Output

Below is an example of the cleaned and validated dataset extracted from Google Search:

| Hospital Name                | Type     | Rating | Location                                    | Operation Hours        | Phone Number   |
|------------------------------|----------|--------|---------------------------------------------|------------------------|----------------|
| Gleneagles Hospital Kuala Lumpur | Private  | 4.2    | 286 & 288, Jalan Ampang, 50450 Kuala Lumpur | Open 24 hours          | +60-3-4141-3000 |
| Prince Court Medical Centre    | Private  | 4.5    | 39, Jalan Kia Peng, 50450 Kuala Lumpur       | Open 24 hours          | +60-3-2160-0000 |
| Kuala Lumpur General Hospital   | Public   | 3.8    | Jalan Pahang, 50586 Kuala Lumpur            | Open 24 hours          | +60-3-2615-5555 |

*Note*: The above is sample data; actual results depend on the information available on Google Search.

---

## Setup Instructions

1. Open Power BI Desktop.
2. Use the "Get Data > Web" option and enter the URL: `https://www.google.com/search?q=hospital+in+kuala+lumpur&tbm=lcl`.
3. In Power Query Editor:
   * Parse the HTML table or list containing hospital details using `Html.Table`.
   * Apply transformations to extract fields such as name, type, rating, location, operation hours, and phone number.
4. Validate the extracted data:
   * Ensure all fields are complete and formatted correctly.
   * Check for duplicates or inconsistencies.
5. Clean the data:
   * Remove irrelevant rows or columns.
   * Standardize address formats and handle missing values.
6. Load the cleaned dataset into Power BI’s data model.
7. Export the final dataset as a CSV file by navigating to "File > Export > CSV."

---

## Future Improvements

* Automate periodic updates using scheduled refreshes in Power BI Service.
* Add support for scraping multiple pages of search results to capture more hospitals.
* Enhance validation rules to detect incorrect or outdated information (e.g., closed hospitals).
* Integrate additional metrics such as patient reviews or bed capacities.

---

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE) for details.
