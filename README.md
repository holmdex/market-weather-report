# Global Market Weather Report 🌍

## Overview

The Global Market Weather Report is an automated financial markets analysis tool that generates comprehensive monthly reports. It provides insights into market performance across major global indices in an accessible, weather-themed format. The report combines technical analysis with intuitive visualizations to make market movements understandable for both financial professionals and interested observers.

## Features

The report provides detailed analysis of market performance through several key components:

The Monthly Weather Check presents current market conditions using weather-themed indicators to illustrate market health and momentum. Each market receives a weather designation ranging from sunny to rainy, providing an intuitive understanding of current conditions.

The Performance Journey section displays both monthly and yearly market trajectories, with all markets normalized to a starting value of 100 for clear comparison. Interactive visualizations allow users to focus on specific markets of interest.

The Crystal Ball Forecast utilizes statistical modeling to project potential market movements for the coming two weeks, including confidence intervals to represent uncertainty. The forecast integrates seamlessly with historical data to provide context for future projections.

The Market Health Review evaluates stability metrics and trend patterns across all tracked indices, providing a systematic assessment of market conditions.

## Technical Implementation

### Prerequisites

The report requires the following software:
- R (version 4.0.0 or higher)
- RStudio (recommended for local development)
- Git

### Required R Packages

The following R packages are essential for report generation:
- tidyverse: Data manipulation and visualization
- quantmod: Financial data acquisition
- plotly: Interactive visualizations
- forecast: Statistical forecasting
- kableExtra: Enhanced table formatting
- Additional dependencies are handled through the pacman package manager

## Installation

1. Clone the repository:
```bash
git clone https://github.com/your-username/market-weather-report.git
cd market-weather-report
```

2. Install required R packages:
```R
if (!require("pacman")) install.packages("pacman")
pacman::p_load(tidyverse, quantmod, rvest, httr, jsonlite, plotly, DT, 
               scales, lubridate, viridis, kableExtra, forecast, TTR, gridExtra)
```

## Usage

### Automated Monthly Generation

The report automatically generates on the first day of each month through GitHub Actions. The workflow:
1. Fetches latest market data
2. Generates comprehensive analysis
3. Produces an HTML report
4. Commits the report to the repository

### Manual Generation

To generate the report manually:

1. Open the R project in RStudio
2. Navigate to the R/market_report.Rmd file
3. Click 'Knit' or run:
```R
rmarkdown::render("R/market_report.Rmd")
```

## Output

The generated report includes:
- Interactive market performance visualizations
- Market health indicators
- Forward-looking analysis
- Comprehensive market correlations
- Weekly trading pattern analysis

Reports are saved with the naming convention: `market_report_YYYY_MM.html`

## Maintenance

The system requires minimal maintenance due to its automated nature. However, periodic checks are recommended for:
- Data source availability
- Package compatibility
- GitHub Actions workflow status

## Contributing

Contributions to improve the report are welcome. Please:
1. Fork the repository
2. Create a feature branch
3. Submit a pull request with detailed description of changes

## License

This project is not licensed through github.

## Contact

For questions or support, please open an issue in the GitHub repository.

---
Last Updated: December 2024

Note: This report is for informational purposes only and should not be considered financial advice. Always consult with financial professionals for investment decisions.
