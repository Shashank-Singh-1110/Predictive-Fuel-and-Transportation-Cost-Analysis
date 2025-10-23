📊 The Data Pipeline

The project relies on three core datasets that are merged to train our models.

1. Fuel Prices

Source: Petroleum Planning &Analysis Cell (PPAC), India.

Method: A Python script (pdfplumber, requests) scrapes the PPAC website, finds the link to the multi-page historical PDF, loops through all 35 pages, and parses the tables.

Output: fuel_prices_historical_all_pages.csv - A clean, historical record of daily petrol and diesel prices for four major cities.

2. Transportation Data

Source: Synthetically generated (pandas, numpy).

Method: To create realistic data, a script simulates thousands of trips. It loops through every date/city in our fuel data and generates trips with varying vehicles, distances (15km to 3000km), and loads.

Key Logic: The Total_Fuel_Cost is calculated based on vehicle mileage, load (which creates a mileage penalty), and the actual fuel price for that specific day, creating the core relationship for our models to learn.

3. Weather Data

Source: Open-Meteo API.

Method: A script fetches historical daily weather (Temp_Mean_C, Precipitation_mm) for all cities within the date range of our fuel data.
