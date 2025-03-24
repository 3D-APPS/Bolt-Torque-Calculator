# ASME/API Code Reference System

A sophisticated browser-based application for searching and referencing engineering codes and standards from ASME and API. This system allows engineers and technical professionals to find relevant code references using natural language questions or keyword searches.

## Overview

The ASME/API Code Reference System provides an intelligent interface for accessing important engineering standards information. The application operates entirely in the browser, with no server-side processing required, making it ideal for deployment on static hosting platforms like GitHub Pages.

## Features

- **Natural Language Question Processing**: Ask questions in plain English like "What are the requirements for pressure vessel inspection?" and receive relevant references
- **Code Reference Search**: Query across multiple ASME and API standards simultaneously
- **Intelligent Code Detection**: Automatically identifies relevant codes based on question content and terminology
- **Subject Matter Recognition**: Understands industry-specific terminology and maps it to appropriate standards
- **Relevance-Based Results**: Prioritizes search results based on question context and technical relevance
- **Filtering Options**: Narrow results by specific code (e.g., ASME B31.3, API 510) or section numbers
- **Quick Search**: Rapid access to code references via the top search bar
- **Advanced Search**: Detailed filtering options for precise queries
- **Responsive Design**: Functions well on both desktop and mobile devices
- **Dark Theme**: Eye-friendly interface for extended use
- **No External Dependencies**: Completely self-contained HTML/CSS/JavaScript application

## Supported Standards

The system currently includes reference data for:

- ASME B31.3 (Process Piping)
- ASME Section I (Power Boilers)
- ASME Section V (Nondestructive Examination)
- ASME Section VIII (Pressure Vessels)
- API 510 (Pressure Vessel Inspection)
- API 570 (Piping Inspection)
- API 653 (Tank Inspection)
- API 580 (Risk-Based Inspection)

## Deployment

This application is designed for deployment on GitHub Pages:

1. Fork or clone this repository
2. Navigate to the repository Settings
3. Select the Pages section
4. Choose your main branch as the source
5. Save the configuration
6. Your site will be published at `https://[username].github.io/[repository-name]/`

## Local Development

To run the application locally:

1. Clone this repository to your local machine
2. Open the `index.html` file in any modern web browser
3. The application will load with sample data ready for testing

## Customizing Reference Data

The system uses two approaches for reference data:

### 1. External JSON File (Recommended)

Create a file named `code-references.json` in your repository with this structure:

```json
{
  "ASME B31.3": [
    {
      "section": "300.1.1",
      "content": "This Code contains requirements for piping typically found in petroleum refineries..."
    },
    {
      "section": "300.2",
      "subsection": "2",
      "content": "The Code is applicable to piping for all fluids including..."
    }
  ],
  "API 510": [
    {
      "section": "1.1",
      "content": "API 510 covers the in-service inspection, repair, alteration..."
    }
  ]
}
```

The system will automatically load this file when available.

### 2. Built-in Sample Data

The application includes some built-in sample data that serves as a fallback if the external JSON file cannot be loaded.

## Technical Details

### Architecture

The application is built using:
- HTML5 for structure
- CSS3 for styling and layout
- Vanilla JavaScript for functionality
- Object-oriented programming patterns for code organization

### Search Functionality

The search system uses several advanced techniques:

1. **Code-Specific Keyword Dictionary**: The system maintains a comprehensive dictionary mapping technical terms to specific codes. For example, terms like "piping," "fluid," and "chemical" are associated with ASME B31.3.

2. **Question Pattern Recognition**: The system identifies common question patterns (e.g., "What is...", "How to...", "Requirements for...") and extracts subject matter for searching.

3. **Relevance Scoring Algorithm**: Search results are ranked using a scoring algorithm that considers:
   - Match with important technical terminology
   - Presence of terms in section titles vs. content
   - How specifically the term relates to a particular code
   - Explicit mentions of code or section numbers

4. **Reference Data Management**: The system loads data from an external JSON file when available, with a fallback to built-in sample data.

## Enhancing the System

### Adding More Code-Specific Keywords

To improve natural language understanding, you can enhance the code keyword dictionary in the HTML file:

```javascript
this.codeKeywords = {
    "ASME B31.3": ["piping", "pipe", "fluid", "chemical", "refinery", ...],
    "API 510": ["pressure", "vessel", "inspection", "repair", ...],
    // Add more keywords for each code
};
```

### Expanding Reference Data

Add more comprehensive reference data to your JSON file to improve search results.

## Future Enhancements

Potential improvements for future versions:

- Expanded reference database with more comprehensive code coverage
- Advanced filtering by topics and categories
- User accounts for saving favorite references
- Export functionality for reports
- Incorporation of code images and diagrams
- Full-text search with fuzzy matching

## License

This project is available under the MIT License. See the LICENSE file for details.

## Disclaimer

This tool is provided for reference purposes only. Always consult the official documentation for definitive answers regarding engineering codes and standards. The creators of this application are not responsible for any decisions made based on the information provided.
