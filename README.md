# tasdk-1-wheather
This project is a simple weather dashboard web application that allows users to input a city name and receive real-time weather information for that location. It leverages the OpenWeatherMap API to fetch weather data and displays key weather conditions such as temperature, weather description, and an appropriate weather icon.

Features

1. City Input Field:

Users can input the name of any city in the world.



2. Weather Display:

After entering a city and clicking the "Get Weather" button, the app displays:

City name

Temperature (in Celsius)

Weather description (e.g., clear sky, rain)

Weather icon that visually represents the weather (e.g., sun, clouds)


![Screenshot 2024-10-18 113601](https://github.com/user-attachments/assets/bd07dda0-8b54-40b3-bc4c-486189f95eba)


3. Responsive and Interactive UI:

The interface is styled using basic CSS and is designed to center the content for easy interaction.




How It Works

1. HTML Structure

The HTML file contains a simple structure with:

A container div to hold the weather dashboard UI.

An input field (#city) where users can type the city name.

A button (#getWeather) to trigger the weather fetch process.

Two divs (#currentWeather and #forecast) that will be populated with the weather data.



2. Styling with CSS

The app uses minimal, clean styling to make it user-friendly. The weather dashboard is centrally aligned on the page, and the button has hover effects to improve user interaction.

The weather data is shown inside the #currentWeather div, with proper spacing and layout for clarity.


3. JavaScript (app logic)

The core functionality lies in the JavaScript section:

a. API Key Setup:

An OpenWeatherMap API key is required to fetch data. This key must be stored in the apiKey variable in the code.


b. Event Listener:

When the user clicks the Get Weather button, an event listener triggers the getWeatherData function. This function reads the city name from the input field and calls the OpenWeatherMap API to fetch weather data.


c. Fetching Weather Data:

The getWeatherData function constructs the API request URL based on the user's input (city name) and fetches the weather data using the fetch API.

The API request returns a JSON response containing weather information, such as:

City name

Temperature

Weather conditions (like clear sky, rain, etc.)

Weather icon (to visually represent the weather)



d. Displaying Weather Information:

If the API response is successful (data.cod === 200), the displayCurrentWeather function is called, which updates the #currentWeather div with:

City name

Temperature (in Celsius)

Weather description

Weather icon


The weather icon is retrieved by using the icon property from the API response, which points to an icon image hosted by OpenWeatherMap.


e. Error Handling:

If the API returns an error (e.g., if the city name is invalid), an alert is shown to the user stating that the city was not found.


How to Use the Application

1. Enter a city name in the input field (e.g., "London").


2. Click the "Get Weather" button.


3. The current weather for the city will be displayed, including:

Temperature

Weather description (e.g., "clear sky")

Weather icon representing the current conditions (e.g., a sun icon for clear sky).




How to Run the Application

1. Download or copy the combined HTML, CSS, and JavaScript code.


2. Replace the apiKey variable in the JavaScript with your own OpenWeatherMap API key. You can obtain one by signing up on the OpenWeatherMap website.


3. Save the file as an .html file (e.g., weather-dashboard.html).


4. Open the file in your browser (Chrome, Firefox, etc.).


5. The app will be displayed, and you can start entering city names to get weather updates.



Key Technologies Used

1. HTML:

Provides the structure and elements like input fields, buttons, and divs for displaying data.



2. CSS:

Used for styling the UI, making it visually appealing and user-friendly.



3. JavaScript:

Responsible for fetching weather data from the OpenWeatherMap API.

Handles dynamic DOM manipulation (updating the page with weather information).



4. OpenWeatherMap API:

A third-party service used to fetch real-time weather data based on city names.




Possible Extensions

1. 5-Day Forecast:

You can extend the application by fetching the 5-day forecast data from the OpenWeatherMap API and displaying it in the #forecast section.



2. Improved UI:

Use advanced CSS or front-end frameworks like Bootstrap to make the app more responsive and visually appealing.



3. Geolocation:

Add functionality to fetch the user's current location using the browser's geolocation API and display the weather for their current city automatically.
