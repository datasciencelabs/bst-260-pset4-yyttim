# Problem Set 4: Data Wrangling (API Data Extraction, Web Scraping, and COVID-19 Data Analysis)

## Overview

This assignment focuses on extracting data from web APIs, processing JSON responses, and analyzing COVID-19 data across US states. You'll learn to interact with the US Census and CDC APIs, wrangle complex datasets, and create visualizations to explore relationships between population demographics and COVID-19 outcomes. 

## Getting Started

1. **Accept the assignment** via the GitHub Classroom link
2. **Clone this repository** to your local machine
3. **Open the repository folder** in RStudio as a project
4. **Complete all problems** in the `pset-04-wrangling.qmd` file

## Assignment Files

- `pset-04-wrangling.qmd` - Main assignment file with all 15 problems
- `census-key.R` - Census API key file (you'll create this)
- `README.md` - This instruction file

## Technical Requirements

### Required Packages

- **httr2** - HTTP requests and API interactions
- **tidyverse** - Data manipulation, visualization, and analysis
- **janitor** - Data cleaning and formatting
- **jsonlite** - JSON data parsing
- **lubridate** - Date and time manipulation

### API Requirements

- **US Census API Key** - Sign up at https://api.census.gov/data/key_signup.html
- **Internet connection** - Required for API calls throughout assignment
- **File management** - Store your API key in `census-key.R` (never commit this file)

### Key Concepts Covered

- **HTTP requests** - Using `httr2` to interact with web APIs
- **JSON parsing** - Converting JSON responses to R data structures
- **Data extraction** - Pulling specific data from complex API responses
- **Data cleaning** - Using `janitor` for header management and formatting
- **Date parsing** - Converting strings to proper Date formats with `lubridate`
- **API parameters** - Handling limits, filters, and query parameters
- **Data visualization** - Creating time series and summary plots

## What You'll Create

By the end of this assignment, your repository should have this structure:

**Root Directory:**

- `pset-04-wrangling.qmd` - Main assignment file with all 15 problems
- `pset-04-wrangling.html` - Rendered HTML output
- `census-key.R` - Your Census API key file (Problem 1) **[DO NOT COMMIT]**
- `README.md` - This instruction file

**Important Security Note:**

- Add `census-key.R` to your `.gitignore` file to prevent accidentally committing your API key
- Your API key should never appear in your Git history or be visible on GitHub

## Assignment Structure

**15 Problems covering:**

- **Problems 1-2**: US Census API setup and request construction
- **Problems 3-5**: HTTP response handling and content extraction
- **Problems 6-7**: Data cleaning and visualization with Census data
- **Problems 8-9**: JSON parsing and regional data integration
- **Problems 10-11**: CDC API data extraction with parameter handling
- **Problems 12-13**: Time series analysis and date manipulation
- **Problems 14-15**: Additional CDC data and summary visualizations

## Key Instructions

1. **Obtain a Census API key** and store it securely in `census-key.R`
2. **Never commit your API key** - add `census-key.R` to `.gitignore`
3. **Handle API responses properly** - check status codes and content types
4. **Clean data thoroughly** - APIs often return messy, nested data
5. **Create informative visualizations** - properly label all plots
6. **Show both code and output** in your rendered document

## Technical Tips

- **API rate limits**: Be mindful of how frequently you call APIs
- **Error handling**: Check response status codes before processing data
- **Data types**: Convert strings to appropriate types (dates, numbers)
- **Missing data**: Handle `NA` values that may come from API responses
- **URL construction**: Use `httr2` functions rather than manual string concatenation
- **JSON structure**: Examine JSON responses carefully before parsing

## Data Sources

**US Census Population Estimates API**
- Provides state population data for 2020-2021
- Requires API key for access
- Returns data in JSON format with nested structure

**CDC COVID-19 Data APIs**
- Case data: Daily COVID-19 cases by state
- Death data: COVID-19 deaths with demographic breakdowns
- Large datasets requiring limit parameter adjustments
- Public APIs with no authentication required

**Additional Data**
- Regional classifications from GitHub JSON file
- State abbreviation mappings using R's built-in data

## Submission

Your submission is your final committed and pushed repository. Make sure to:

1. **Complete all 15 problems** in the assignment file
2. **Render your document to HTML** successfully
3. **Include both .qmd and .html files** in your submission
4. **DO NOT commit your `census-key.R` file**
5. **Commit your changes** with meaningful messages
6. **Push your final work** to GitHub
7. **Verify** that all code and output are visible in your GitHub repository

## Due Date

**October 5, 2025, 11:59 PM**

## Getting Help

- Post questions on our class Slack in the #pset-04 channel
- Attend office hours for API and data extraction help
- Review course materials on web scraping and APIs
- Check package documentation using `?function_name`
- Consult API documentation for parameter details

## Common Pitfalls to Avoid

- **Committing your API key** (serious security issue)
- **Not checking API response status** before processing
- **Ignoring data type conversions** (keeping everything as character)
- **Poor error handling** when APIs return unexpected responses
- **Not adjusting API limits** (getting incomplete data)
- **Forgetting to handle missing values** in API responses

## Grading

| **Criteria** | **Excellent (A)** | **Good (B)** | **Satisfactory (C)** | **Needs Improvement (D-F)** |
|:-------------|:------------------|:-------------|:---------------------|:---------------------------|
| **API Integration & HTTP Requests (30 points)** | 27-30: Perfect use of httr2, proper error handling, all API calls successful. Demonstrates mastery of web API integration. | 24-26: Good API usage with minor issues in parameter handling or response processing. | 18-23: Basic API functionality working but missing some error handling or parameter optimization. | 0-17: Poor API usage, failed requests, major errors in HTTP handling or missing functionality. |
| **Data Extraction & JSON Parsing (25 points)** | 23-25: Excellent JSON parsing, perfect data extraction from complex nested structures. Clean conversion to tidy data formats. | 20-22: Good data extraction with minor issues in JSON parsing or data structure handling. | 15-19: Basic data extraction working but some issues with complex nested data or inefficient parsing. | 0-14: Poor data extraction, major JSON parsing errors, or inability to handle API response structures. |
| **Data Cleaning & Transformation (20 points)** | 18-20: Masterful data cleaning, proper type conversions, excellent use of janitor and tidyverse tools. Perfect date parsing. | 16-17: Good data cleaning with minor issues in type conversion or date handling. | 12-15: Basic cleaning completed but some issues with data types, dates, or missing value handling. | 0-11: Poor data cleaning, major type conversion errors, or improper handling of messy API data. |
| **Visualization & Analysis (15 points)** | 14-15: Beautiful, informative visualizations with proper labels, titles, and formatting. Clear insights from data. | 12-13: Good visualizations with minor aesthetic or labeling issues. Plots convey intended information. | 9-11: Basic plots created but missing some labels, poor aesthetics, or unclear presentation. | 0-8: Poor or missing visualizations, major labeling problems, or plots don't convey meaningful information. |
| **Code Organization & Documentation (5 points)** | 5: Exceptionally clean, well-documented code. Clear logic flow, excellent error handling, easy to follow. | 4: Good code organization with minor documentation gaps. Code is readable and well-structured. | 3: Basic code organization but some unclear sections or missing comments where needed. | 0-2: Poor code organization, unclear logic, missing documentation, or difficult to follow. |
| **Technical Requirements & Security (5 points)** | 5: Perfect API key handling, document renders flawlessly, all technical requirements met, excellent GitHub practices. | 4: Meets technical requirements with minor issues. Good security practices maintained. | 3: Some technical issues but basic requirements met, minor security oversights. | 0-2: Major technical problems, security issues (committed API keys), or rendering failures. |

## Key Assessment Points

**Specific Things Graders Will Look For:**

1. **Secure API key handling**: Never commits sensitive credentials
2. **Proper HTTP request construction**: Correct use of httr2 functions
3. **Robust error handling**: Checks response status before processing
4. **Accurate data extraction**: Successfully parses complex JSON structures
5. **Clean data transformation**: Proper type conversions and date parsing
6. **Informative visualizations**: Well-labeled, publication-quality plots

**Common Deductions:**

- Committing API keys or other sensitive information (-15 points)
- Not checking API response status (-5 points per instance)
- Poor JSON parsing or data extraction (-5 points per problem)
- Incorrect data type handling (-3 points per problem)
- Missing or poor plot labels (-3 points per plot)
- Document rendering failures (-10 points)

This rubric emphasizes **API integration skills** and **data extraction techniques** essential for modern data science workflows involving web data sources.

## Resources

- **httr2 package documentation**: `help(package = "httr2")`
- **US Census API documentation**: https://www.census.gov/data/developers/data-sets.html
- **CDC Data Portal**: https://data.cdc.gov/
- **JSON structure exploration**: Use `str()` to examine parsed JSON objects
- **HTTP status codes**: https://en.wikipedia.org/wiki/List_of_HTTP_status_codes
- **lubridate cheat sheet**: RStudio cheat sheets for date/time manipulation