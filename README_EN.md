# Python Script: DOI Resolution and Metadata Processing

## Overview
This Python script automates the process of resolving DOIs (Digital Object Identifiers) and retrieving metadata for academic references from a `.txt` file. It supports:

- Resolving DOIs via the CrossRef API.
- Fetching metadata such as title, journal, authors, pISSN, and eISSN.
- Matching journals with the FNEGE 2022 ranking.
- Calculating similarity indices between the source reference and retrieved metadata (Title, Journal).
- Exporting results to an Excel file with conditional formatting.

The script is designed to handle large datasets efficiently with multithreading and progress indicators.

---

## Features

1. **DOI Resolution**:
   - Uses the CrossRef API to resolve DOIs for references provided in a `.txt` file.

2. **Metadata Retrieval**:
   - Fetches metadata for each resolved DOI, including Title, Journal, Authors, pISSN, and eISSN.

3. **FNEGE 2022 Ranking**:
   - Matches journal metadata against an external FNEGE 2022 ranking file and adds the corresponding ranking to the output.

4. **Similarity Indices**:
   - Calculates similarity between the source reference and the resolved metadata (Title and Journal).

5. **Excel Export with Conditional Formatting**:
   - Exports the results to an Excel file with:
     - Highlighted similarity scores based on thresholds.
     - Progress tracking during export.

6. **Progress Indicators**:
   - Uses `tqdm` to display progress bars for key operations.

7. **Multithreading**:
   - Processes multiple API requests simultaneously to improve performance.

---

## Requirements

### Dependencies
The script requires the following Python packages:

- `requests`
- `pandas`
- `openpyxl`
- `tqdm`
- `tkinter`
- `queue`

Install the dependencies with:
```bash
pip install requests pandas openpyxl tqdm
```

### External Files
1. **Input File**: A `.txt` file containing references (one reference per line).
2. **FNEGE File**: The Excel file containing journal rankings is automatically downloaded from GitHub.

---

## Usage

1. Clone this repository:
   ```bash
   git clone <repository_url>
   cd <repository_folder>
   ```

2. Run the script:
   ```bash
   python <script_name>.py
   ```

3. Follow the prompts to:
   - Select the `.txt` file containing the references.

4. The script will:
   - Resolve DOIs.
   - Fetch metadata.
   - Match the FNEGE ranking.
   - Calculate similarity indices.
   - Export the results to an Excel file (`_resolved_dois.xlsx`).

---

## Output

### Excel File
The output file contains the following columns:

- **Source Reference**: The original reference from the `.txt` file.
- **DOI**: Resolved DOI for the reference.
- **Title**: Title retrieved from the DOI.
- **Journal**: Journal name retrieved from the DOI.
- **Authors**: Authors retrieved from the DOI.
- **pISSN_PRINT**: Print ISSN.
- **eISSN**: Electronic ISSN.
- **Classement FNEGE 2022**: Journal ranking from the FNEGE 2022 file.
- **Similarity (Source vs Title)**: Similarity score between the source reference and the title.
- **Similarity (Source vs Journal)**: Similarity score between the source reference and the journal.

### Conditional Formatting
- **Green**: Strong similarity (80-100%).
- **Orange**: Moderate similarity (60-79%).
- **Red**: Low similarity (<60%).

---

## License
This project is licensed under the Apache License 2.0.

---

## Contributing
Feel free to open issues or submit pull requests for bug fixes, improvements, or additional features.

---

## Author
Developed by aymericscientist

---

