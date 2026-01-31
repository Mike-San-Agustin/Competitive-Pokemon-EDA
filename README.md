**Project Overview**

This project analyes the "meta-game" of Pokemon Generation 9 competitive play. By merging usage statistics from Smogon with game data from PokeAPI, this analysis explores why certain Pokemon dominate the competitive scene.

This project demonstrates a complete data science lifecycle: Web Scraping, API integration, Data Cleaning, Multivariate Statistical Testing, and Ineteractive visualization.

Key Insights

-   **The "Stats" Fallacy:** While High base stats generally correlate with usage, specific abilities
(ex: *Regenerator*) and items (ex: *Heavy-Duty Boots*) allow lower-stat Pokemon to remain
top-tier threats.

- **Typing and Stat Distribution:** A **MANOVA** test confirmed that Pokemon types have significantly
different average stat profiles (p<0.0001) reflecting intentional game design balance. 

- **The "Great Tusk" Phenomenon:** Analysis of the most-used Pokemon reveals a "perfect storm" of
high stats, optimal typing (Ground/Fighting), and ability synergy, leading to an unprecedented 33.6%
usage rate.

**Technical Toolkit**

- **Language:** R

- **Data Retrieval:** jsonlite, rvest, purr, API parsing

- **Wrangling:** tidyverse (dplyr, tidyr, stringr), joins, pivots

- **Statistics:** prcomp (PCA), manova

- **Visualizations:** ggplot2, plotly (interactive and 3D plots)

**Data Sources and processing**

1. **Competitive Data:** Scraped from Smogon chaos stats (JSON), involving custom parsing of nested lists to extract ability and item frequencies.

2. **Game Data:** Programmatically retrieved from PokeAPI using a custom-built parser to handle over 1,000 unique entries.

3. **Wrangling Highlights:** Resolved naming inconsistencies between datasets using stringr.

  - Applied c_across() and case_when() for custom Pokémon tier classification.

  - Reduced 6D combat stats into 3D space using Principal Component Analysis for visualization.
  
  
**How to Run**

1. **HTML file:** The HTML file can be viewed on your web browser (ex: Google Chrome). The html file contains the plots
and a written report, but no code. This is optimal to see the plots and tables.

2. **Rmarkdown** CompetitivePokemon-datacleaningandEDA.Rmd contains all code. 

  * Ensure all libraries in the setup chunk are installed in order to run the code.