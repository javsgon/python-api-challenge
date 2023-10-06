# Python API Challenge

## Background
Use of Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"

## Files
Files provided: WeatherPy.ipynb, VacationPy.ipynb, cities.csv

## Instructions
This activity is broken down into two deliverables, WeatherPy and VacationPy.

### Part 1: WeatherPy
In this deliverable, a Python script was created to visualize the weather of over 500 cities of varying distances from the equator. Used the citipy Python libraryLinks to an external site, the OpenWeatherMap APILinks to an external site, and problem-solving skills to create a representative model of weather across cities.

For this part, I used the WeatherPy.ipynb Jupyter notebook provided in the starter code ZIP file. 

The code required to generate random geographic coordinates and the nearest city to each latitude and longitude combination is provided.

#### Requirement 1: Create Plots to Showcase the Relationship Between Weather Variables and Latitude
To fulfill the first requirement,  the OpenWeatherMap API was used to retrieve weather data from the cities list generated in the starter code. Next, you'll create a series of scatter plots to showcase the following relationships:

Latitude vs. Temperature

<img width="557" alt="Screenshot 2023-10-06 at 1 15 02 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/9f8d4a30-b389-4b27-94dd-acbc39f60306">

Latitude vs. Humidity

<img width="567" alt="Screenshot 2023-10-06 at 1 15 10 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/25bf848f-6379-40ae-8708-7470e9e895d2">

Latitude vs. Cloudiness

<img width="574" alt="Screenshot 2023-10-06 at 1 15 16 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/931f69a1-522d-4aa1-955b-2624867932c3">

Latitude vs. Wind Speed

<img width="551" alt="Screenshot 2023-10-06 at 1 15 23 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/2f58fb2d-b127-4fa9-b21c-7a2fcdec9fb3">

#### Requirement 2: Compute Linear Regression for Each Relationship
The linear regression for each relationship was computed. The plots into Northern Hemisphere (greater than or equal to 0 degrees latitude) and Southern Hemisphere (less than 0 degrees latitude) were separated. 

A series of scatter plots were created.

The following plots were created:

Northern Hemisphere: Temperature vs. Latitude

<img width="573" alt="Screenshot 2023-10-06 at 1 15 36 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/bca3fdb2-806d-406e-b88a-b1a3607622a6">

Southern Hemisphere: Temperature vs. Latitude

<img width="556" alt="Screenshot 2023-10-06 at 1 15 43 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/50da570c-b380-4a54-ae6c-1763693afd3c">

Northern Hemisphere: Humidity vs. Latitude

<img width="569" alt="Screenshot 2023-10-06 at 1 15 50 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/3e03cbda-3129-4de6-b00c-cb04bbadfabc">

Southern Hemisphere: Humidity vs. Latitude

<img width="573" alt="Screenshot 2023-10-06 at 1 15 57 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/6bb051b4-9d69-4cca-9371-250100e4a949">

Northern Hemisphere: Cloudiness vs. Latitude

<img width="558" alt="Screenshot 2023-10-06 at 1 21 33 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/5cc7ad02-9dbf-4d96-8a16-0070a3b59c1f">

Southern Hemisphere: Cloudiness vs. Latitude

<img width="563" alt="Screenshot 2023-10-06 at 1 21 48 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/2ff13dc1-4c61-4837-864e-19f6563cacf4">


Northern Hemisphere: Wind Speed vs. Latitude

<img width="545" alt="Screenshot 2023-10-06 at 1 21 58 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/4dae36e4-3b8e-4063-a723-68ad935023ff">

Southern Hemisphere: Wind Speed vs. Latitude

<img width="547" alt="Screenshot 2023-10-06 at 1 22 06 PM" src="https://github.com/javsgon/python-api-challenge/assets/125521896/bc97e9cf-f5cf-4f23-bf86-fd0743e6583a">


### Part 2: VacationPy
Used Jupyter notebooks, the geoViews Python library, and the Geoapify API.

The code needed to import the required libraries and load the CSV file with the weather and coordinates data for each city created in Part 1 is provided to get started.

The main tasks is to use the Geoapify API and the geoViews Python library and employ your Python skills to create map visualizations.

To succeed on this deliverable of the assignment, the VacationPy.ipynb starter code was used and the following steps were completed:

- Created a map that displays a point for every city in the city_data_df DataFrame. The size of the point should be the humidity in each city.

- Narrowed down the city_data_df DataFrame to find the ideal weather condition. For example:

  - A max temperature lower than 27 degrees but higher than 21

  - Wind speed less than 4.5 m/s

  - Zero cloudiness

Created a new DataFrame called hotel_df to store the city, country, coordinates, and humidity.

For each city, the Geoapify API was used to find the first hotel located within 10,000 meters of the coordinates.

Added the hotel name and the country as additional information in the hover message for each city on the map.
