# Statistical Analysis of Diamond Prices

## Question
**What drives the price of a diamond, and do price differences between cut grades hold up statistically?**

## Data
- A 1,000-row sample of the classic *diamonds* dataset (also available in the R `ggplot2` package)
- 10 variables: carat, cut, color, clarity, depth, table, price and dimensions (x, y, z)
- Place the file at `data/diamonds_sample.csv`

## Method
- Descriptive statistics, distributions and correlation matrix
- Probability calculations, binomial probability, and 90% / 95% confidence intervals
- **Log transformation** to correct right-skewed prices
- **Welch t-tests** (Ideal vs. Very Good cut) and a **chi-square test** of independence (price level vs. clarity)
- **Simple and multiple linear regression** of ln(price) on ln(carat) and cut

## Key results
- Carat is very strongly correlated with price (r = 0.92)
- A 1% increase in carat is linked to about a 1.67% increase in price
- ln(carat) alone explains **93% of price variation** (R² = 0.93)
- Clarity level was not significantly linked to whether a diamond costs over $5,000 (p = 0.08)

## Files
- `diamond_analysis.Rmd` – R Markdown source
- `report.pdf` – rendered report
