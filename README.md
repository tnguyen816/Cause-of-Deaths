# Cause-of-Deaths
An interactive Tableau Public dashboard exploring the leading causes of death worldwide between 1990 and 2019, grouped into communicable, non-communicable, and injury-related causes.

🔗 Live dashboard: https://public.tableau.com/views/CauseofDeathsAroundtheWorld/MainDashboard?:language=en-US&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link


## Overview

This dashboard covers 1990 to 2019, so it shows the world before COVID-19, which went on to cause about 7.1 million confirmed deaths reported to WHO (add the "as of" date for this figure).

It lets viewers pick a year and see the most common cause of death in every country on an interactive map, alongside total deaths by cause group, the leading causes, and the countries with the highest death counts.

## Dataset: 
Source: Kaggle:[Cause of Deaths Around the World (Kaggle)](https://www.kaggle.com/datasets/iamsouravbanerjee/cause-of-deaths-around-the-world)

Coverage: countries and territories, 1990 to 2019

Structure: one row per country and year, with one column of death counts for each cause (e.g. Cardiovascular Diseases, Neoplasms, Malaria, Drowning)

## Tools
Tableau Public: data preparation, calculated fields, and the interactive dashboard

## Approach
Pivoted the wide cause columns into a long format (one row per country, year, and cause), which Tableau needs for ranking causes.
Found the top cause per country and year with a FIXED level-of-detail calculation (the maximum deaths for each country-year, matched back to its cause).
Grouped causes into Communicable, Non-communicable, and Injuries with a calculated field (see below).
Added interactivity: a year control for the map and filters for country and cause.
Published the dashboard to Tableau Public.
Cause grouping

The grouping follows the WHO / Global Burden of Disease convention.

## Group	Examples
Communicable (includes maternal, neonatal, and nutritional causes)	Lower respiratory infections, diarrheal diseases, tuberculosis, malaria, meningitis, HIV/AIDS, neonatal disorders, maternal disorders
Non-communicable	Cardiovascular diseases, neoplasms, chronic respiratory diseases, diabetes, dementias, kidney disease, liver disease, digestive diseases, drug and alcohol use disorders
Injuries	Road injuries, drowning, self-harm, interpersonal violence, conflict and terrorism, poisonings, fire and heat, natural disasters

# Key Findings

## Overall

Over these 30 years, the dataset records about 1.47 billion deaths.
Non-communicable diseases account for the largest share, almost 67% of all deaths. They are led by cardiovascular diseases, neoplasms (cancers), and chronic respiratory diseases.
Communicable, maternal, neonatal, and nutritional causes account for about 26%, roughly a quarter. This group includes lower respiratory infections, diarrheal diseases, tuberculosis, and HIV/AIDS.
Injuries, including road injuries, drowning, and self-harm, account for approximately 6.5%, the smallest share.
Cardiovascular disease is the single leading cause, responsible for 30.5% of all deaths.

## By country

China and India together account for about 32% of recorded deaths. This largely reflects population size, since the two countries make up roughly over a third of the world's population, rather than higher risk.
China's deaths are dominated by non-communicable diseases, which is consistent with an aging population.
India has far more communicable deaths than China (96M vs. 19M).

## What the map shows

In most countries across the Americas, Europe, Asia, and North Africa, cardiovascular disease is the leading cause of death.

Neoplasms lead in a smaller group of mostly high-income countries, such as Canada and Australia.

Infectious, maternal, and neonatal causes lead mainly in sub-Saharan Africa. HIV/AIDS leads across southern Africa, and malaria, lower respiratory infections, diarrheal diseases, and neonatal disorders lead in parts of West and East Africa.

Overall, chronic disease is the top cause in most of the world, while infectious and maternal causes still lead mostly in lower-income countries.

## Limitations
Counts, not rates. These figures are death counts, so larger countries naturally have higher totals. Comparing countries fairly would need per-capita rates.

Modeled estimates. The figures are likely modeled estimates rather than raw death registrations.

Grouping is a convention. Some causes are debatable (for example, cirrhosis can result from hepatitis but is counted as non-communicable here).

Cumulative totals. Headline totals add up all years from 1990 to 2019; they are not single-year figures.

Pre-COVID only. The data ends in 2019 and does not include COVID-19 deaths.


### Disclaimer

This project is for educational and portfolio purposes only and is not intended to inform medical or public health decisions.
