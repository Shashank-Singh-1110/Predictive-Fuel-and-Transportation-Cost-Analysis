This project is built by collecting, cleaning, and merging three distinct datasets:

1) Historical Fuel Prices:

  Source: Petroleum Planning & Analysis Cell (PPAC), Government of India.
  Method: A Python script (pdfplumber, requests) scrapes the PPAC website, finds the link to the multi-page historical PDF, loops through all 35 pages, and parses the tables.
  Data: Daily Petrol (MS) and Diesel (HSD) prices for Delhi, Mumbai, Chennai, and Kolkata.

2) Synthetic Transportation Data:

  Source: Generated synthetically using Python (pandas, numpy).
  Method: A script simulates a logistics company by looping through every date/city from the fuel data and generating random trips.
  Data: Includes Trip_ID, Vehicle_Type (Motorcycle, Van, Truck), Distance_km, and Load_Weight_kg.
  Key Feature: The Total_Fuel_Cost for each trip is calculated based on the vehicle's mileage and the actual fuel price for that specific day, creating the core relationship for the model to learn.

3) Historical Weather Data: 

  Source: Open-Meteo Historical Weather API.
  Method: A script uses the date range from the fuel data to call the API and fetch historical weather for all four cities.
  Data: Includes daily Temp_Mean_C (mean temperature) and Precipitation_mm (rainfall).
