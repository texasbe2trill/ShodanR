# ShodanR

## Overview

This project analyzes ransomware infections using data retrieved from the **Shodan API**. It visualizes infected hosts on an interactive world map using `ggplot2` and `plotly`.

## Features

-   **Shodan API Integration**: Fetches live data on ransomware-infected hosts.
-   **Interactive Map**: Uses `ggplot2` and `plotly` for a dynamic geographic display.
-   **Secure API Key Handling**: Hides API credentials using environment variables.

## Setup Instructions

### 1. Install `renv` (if not already installed)

Before activating the lock file, ensure you have the `renv` package installed:

``` r
install.packages("renv")
library(renv) # Loads the renv package
renv::restore() # Install exact packages used during development
```

### 2. Store API Key Securely

Add your **Shodan API key** to the `.Renviron` file to avoid exposing it in your code:

1\. Open `.Renviron`: `file.edit("~/.Renviron")`

2\. Add your API key: `SHODAN_API_KEY=your_api_key_here`

3\. Save and restart R.

4\. Access it securely in R: `api_key <- Sys.getenv("SHODAN_API_KEY")`

## Future Improvements

-   [ ] Automate periodic data fetching for time-series analysis.
-   [ ] Implement machine learning models to predict ransomware outbreaks.
-   [ ] Enhance visualization with additional geospatial insights.
-   [ ] Add more API query examples

## License

This project is open-source under the **MIT License**.

## Author

Chris Campbell - [GitHub](https://github.com/texasbe2trill)
