Weather Dashboard
Overview
The Weather Dashboard is a web application that provides users with current weather information and a 5-day weather forecast for any city. Users can enter a city name, choose temperature units (Celsius or Fahrenheit), and visualize the weather data using various chart types. The application utilizes the OpenWeather API for fetching weather data and Chart.js for visualizing charts.

Features
Current Weather Display: Get real-time weather conditions for any city.
5-Day Forecast: View a forecast for the next five days.
Filter Options: Filters for sorting temperatures, filtering out non-rainy days, and highlighting the day with the highest temperature.
Unit Toggle: Switch between metric (Celsius) and imperial (Fahrenheit) temperature units.
Visual Charts: Display temperature data using bar, doughnut, and line charts.
Chatbot: A chatbot that responds to user queries, powered by an external API.
Responsive Design: Adaptable layout for different devices.
Usage
Enter City Name: In the input field, type the name of the city for which you want to fetch weather data.
Apply Filters: Use the checkboxes in the "Filters" section to apply various filters to the weather data:
Sort temperatures in ascending or descending order.
Show only rainy days.
Display the day with the highest temperature.
Select Temperature Unit: Check the box to show the temperature in Fahrenheit, or leave it unchecked for Celsius.
Get Weather: Click the "Get Weather" button to fetch and display the current weather and forecast.
View Charts: Observe the visual representation of weather data through various charts.
Chatbot Interaction: Enter a query in the chatbot input field, click "Send," and view the response from the chatbot.
Code Explanation
HTML Structure
Dashboard.html:
Body Structure:
Hamburger Menu: Toggles the visibility of the sidebar.
Sidebar: Contains navigation links for the dashboard and tables.
Main Content: Displays the user's profile image, a heading, a weather search section, a toggle for temperature units, a weather widget, and a container for charts.
JavaScript Functionality
Unit Toggle: Allows users to switch between metric and imperial temperature units.
Weather Fetching: On clicking the "Get Weather" button, the application fetches the coordinates for the entered city, retrieves current weather data, and updates the weather widget.
Chart Creation: Fetches a 5-day weather forecast and visualizes the data using three types of charts: bar, doughnut, and line.
Functions
createCharts(dates, temps): Responsible for generating the bar, doughnut, and line charts based on the provided dates and temperatures.
clearCharts(): Clears existing chart data to prepare for new charts.
Error Handling: Alerts the user if the entered city is not found.


Tables.html:
HTML Structure
Body Structure:
Hamburger Menu: A toggle button to show or hide the sidebar.
Sidebar: Contains navigation links to switch between the dashboard and tables pages.
Main Content:
Displays the user's profile image, city search bar, and filter options.
Provides the weather widget for displaying current weather and a forecast table for the 5-day forecast.
Contains a chatbot section for user interaction.
JavaScript Functionality
Unit Toggle: Allows the user to toggle between metric and imperial units (Celsius or Fahrenheit).
Weather Fetching:
Fetches city coordinates based on the user input using OpenWeather's Geocoding API.
Retrieves the current weather data and a 5-day forecast using OpenWeather’s Weather API.
Filter Application: Based on user selection, various filters are applied to the forecast data:
Ascending/Descending Temperature: Sorts the temperatures in either ascending or descending order.
Rainy Days: Filters out days without rain if selected.
Highest Temperature: Displays only the day with the highest temperature if selected.
Forecast Table Generation: Builds an HTML table dynamically to display the filtered forecast data.
Chatbot Functionality:
User queries are processed and sent to the Gemini API for responses.
Responses are displayed in the chatbot section on the page.
Functions
Weather-Related Functions:
Fetches current weather and 5-day forecast based on city coordinates.
Filters and sorts the forecast data based on user preferences.
Generates the forecast table in HTML.
Chatbot Functionality:
Sends user input to the Gemini API and displays the chatbot's response in the chatbot section.
Chatbot API Integration
The chatbot is powered by the Gemini API, which receives user input and returns a generated response based on the query. The API interaction is handled using fetch(), sending POST requests with the user's query and displaying the response within the web page.

