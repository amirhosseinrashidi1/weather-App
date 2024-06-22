Weather App using Python and Tkinter

This Python script creates a graphical weather application using Tkinter for the user interface and various APIs to fetch weather and location data. Here's a breakdown of how the script works and what each part does:

Libraries Used:
- tkinter: GUI library for Python.
- geopy.geocoders: Used to geocode the city entered by the user into latitude and longitude coordinates.
- timezonefinder: Determines the timezone based on the latitude and longitude.
- datetime: Provides functionalities to work with dates and times.
- requests: Used to make HTTP requests to fetch weather data from the OpenWeatherMap API.
- pytz: Handles timezones in Python.

Function get_weather():
This function is triggered when the user clicks the search button (search_icon_button). It performs the following tasks:
1. Location: Retrieves the city name entered in the search box (textfield) and uses Nominatim to get its latitude (lat) and longitude (lng). It then determines the timezone (result) using TimezoneFinder.
2. Time: Retrieves the current local time based on the determined timezone (result).
3. Weather: Fetches weather data using the OpenWeatherMap API (api_key). It retrieves information such as temperature, weather condition, humidity, wind speed, pressure, and description.
4. Display: Updates the GUI labels (city_lable, clock, temp_lable, condition_lable, wind_lable, humidity_lable, description_lable, pressure_lable) with the fetched data.

GUI Components:
- Search Box: Allows the user to enter the city name.
- Search Button: Triggers the get_weather() function to fetch and display weather data.
- Labels: Display weather information such as city name, current time, temperature, weather condition, wind speed, humidity, description, and pressure.
- Images: Used for decorative purposes (search.png, search_icon.png, logo.png, box.png).

Error Handling:
- If an error occurs during the execution of get_weather(), it catches the exception and displays an error message using messagebox.showerror().

Usage:
1. Replace placeholders like search.png, search_icon.png, logo.png, box.png with your own images.
2. Ensure you have valid API keys (api_key) for geopy, timezonefinder, and OpenWeatherMap.
3. Run the script to launch the weather application. Enter a city name and click the search button to see weather details.

Notes:
- This script provides a basic weather application GUI using Tkinter. You may further enhance it by adding more features, error handling, or improving the user interface based on your requirements.
