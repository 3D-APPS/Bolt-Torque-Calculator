# ASME/API Code Reference System

A lightweight, browser-based application for searching and referencing engineering codes and standards from ASME and API. This system allows engineers and technical professionals to quickly find relevant code references without the need for external databases or server infrastructure.

## Overview

The ASME/API Code Reference System provides a streamlined interface for accessing important engineering standards information. The application operates entirely in the browser, with no server-side processing required, making it ideal for deployment on static hosting platforms like GitHub Pages.

## Features

- **Code Reference Search**: Query across multiple ASME and API standards simultaneously
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

To add or modify the reference data:

1. Locate the `initializeWithSampleData()` function in the HTML file
2. Add new references using the format:
   ```javascript
   db.addReference(new CodeReference(
       "ASME B31.3",
       "300.1.1",
       "This is the content of the reference.",
       "optional_subsection"
   ));
   ```
3. Save your changes and redeploy if necessary

## Future Enhancements

Potential improvements for future versions:

- External JSON data loading for larger reference sets
- User accounts for saving favorite references
- Export functionality for reports
- Additional engineering codes and standards

## Technical Details

The application is built using:

- HTML5 for structure
- CSS3 for styling and layout
- Vanilla JavaScript for functionality
- Object-oriented programming patterns for code organization

## License

This project is available under the MIT License. See the LICENSE file for details.

## Disclaimer

This tool is provided for reference purposes only. Always consult the official documentation for definitive answers regarding engineering codes and standards. The creators of this application are not responsible for any decisions made based on the information provided.
