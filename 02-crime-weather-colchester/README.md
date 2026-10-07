# Crime and Weather Trends in Colchester

## Question
**Where and when does crime happen in Colchester, and is it linked to the weather?**

## Data
- 5,956 street-level crime records for Colchester (2025) from [data.police.uk](https://data.police.uk), collected with the `ukpolice` R package
- 365 days of weather data from [Ogimet](https://www.ogimet.com), collected with the `climate` R package
- Place the files at `data/crime25.csv` and `data/temp25.csv`

## Method
- Cleaned and merged crime and weather data, handled missing values, and aggregated daily data to monthly level
- Profiled crime by category and season
- Built an **interactive hotspot map** (Leaflet) and **interactive charts** (Plotly)
- Measured the correlation between temperature and monthly crime volume

## Key results
- **Strong positive correlation** between temperature and monthly crime (r = 0.70)
- Violent crime was the largest category and rose clearly in summer
- Findings support seasonal planning of policing resources

## Files
- `crime_weather_analysis.Rmd` – R Markdown source
- `crime_weather_report.html` – rendered interactive report (download and open in a browser)
