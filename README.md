# PRODIGY_WD_05
This project is a **Premium Weather Intelligence Dashboard**, a responsive web application that allows users to view current weather conditions and a 5-day forecast for any location. It is built entirely with **HTML, CSS, and JavaScript**, while integrating external APIs and an interactive map to provide real-time weather information. 

---

# Project Overview

The application has four main components:

1. **Search Panel**
2. **Weather Dashboard**
3. **Interactive Map**
4. **Weather Details & Forecast**

Whenever a user searches for a city, clicks on the map, or uses their current location, the application fetches live weather data from an API and updates every section of the dashboard automatically.

---

# Technologies Used

### HTML

HTML creates the webpage structure.

It contains:

* Search bar
* Search button
* Current location button
* Weather card
* Weather details
* Forecast section
* Interactive map

Everything visible on the page is created using HTML.

---

### CSS

CSS is responsible for making the website attractive.

Some of the features include:

* Glassmorphism cards
* Gradient background
* Blur effects
* Responsive design
* Hover animations
* Dark modern theme
* Mobile-friendly layout

The dashboard automatically adjusts itself for desktop, tablet, and mobile screens using CSS Grid and media queries. 

---

### JavaScript

JavaScript is the brain of the project.

It handles

* User input
* API requests
* Updating weather information
* Loading forecasts
* Map interaction
* Error handling

Without JavaScript, the webpage would only display an empty layout.

---

# How the Project Works

The application follows this workflow:

```
User opens website
        │
        ▼
Search city OR
Use current location OR
Click on map
        │
        ▼
Find latitude & longitude
        │
        ▼
Request weather from API
        │
        ▼
Receive JSON data
        │
        ▼
Update dashboard
        │
        ▼
Display forecast
```

---

# Step 1 – User Searches for a City

The user enters a city name like

```
London
```

and presses the Search button.

JavaScript reads the text from the search box and sends it to the **OpenStreetMap Nominatim API**, which converts the city name into geographic coordinates (latitude and longitude). 

Example:

```
London
```

becomes

```
Latitude : 51.5072

Longitude : -0.1276
```

These coordinates are then used to request weather data.

---

# Step 2 – Getting Weather Data

Once the coordinates are known, the application sends another request to the **Open-Meteo API**.

The API returns weather information in JSON format, including:

* Current temperature
* Humidity
* Wind speed
* Wind direction
* UV index
* Pressure
* Dew point
* Weather condition
* 5-day forecast

The application extracts these values and displays them on the dashboard. 

---

# Step 3 – Displaying the Weather

JavaScript updates the webpage by changing the text inside the HTML elements.

For example:

```
Temperature

28°C

Humidity

75%

Wind Speed

14 km/h
```

Every weather card is updated automatically without refreshing the page.

---

# Interactive Map

The project uses the **Leaflet.js** library to display an interactive map.

Features include:

* Zooming
* Panning
* Marker placement
* Click-to-select location

When the user clicks anywhere on the map:

```
Click
↓

Latitude & Longitude

↓

Reverse Geocoding

↓

Weather API

↓

Dashboard Updates
```

This allows users to view weather conditions for any location simply by clicking on the map.

---

# Current Location Feature

The **Locate Me** button uses the browser's **Geolocation API**.

After the user grants permission, the browser provides the user's latitude and longitude.

The application then requests weather data for that exact location and displays it on the dashboard.

---

# Reverse Geocoding

When a user clicks on the map, only coordinates are available.

Example:

```
13.0827

80.2707
```

These numbers are not user-friendly.

The application sends them to the **Nominatim Reverse Geocoding API**, which converts them into a readable place name, such as **Chennai**.

This makes the displayed location meaningful.

---

# Weather Metrics

The dashboard presents multiple weather parameters:

* Current Temperature
* Apparent (Feels Like) Temperature
* Relative Humidity
* Wind Speed
* Wind Direction
* UV Index
* Dew Point
* Atmospheric Pressure
* Precipitation

Displaying all these metrics gives users a comprehensive view of current weather conditions rather than only showing the temperature.

---

# 5-Day Forecast

The project also displays a five-day forecast.

For each day it shows:

* Day name
* Weather condition
* Maximum temperature
* Minimum temperature

This allows users to plan ahead based on upcoming weather trends.

---

# Quick Search Chips

Below the search bar are predefined city buttons such as:

* London
* New York
* Tokyo
* Sydney
* Rio

Clicking one instantly loads the weather for that city without typing, improving usability.

---

# Autocomplete

The search input includes a datalist with popular cities.

As the user types,

```
Lo...
```

the browser suggests

```
London
```

making searches faster and reducing typing errors.

---

# Error Handling

The application gracefully handles errors such as:

* Invalid city names
* Internet connection problems
* API failures
* Geolocation permission denied

Instead of crashing, it displays informative messages to guide the user.

---

# Responsive Design

The dashboard uses CSS Grid and media queries to adapt to different screen sizes.

On large screens, information is displayed in two columns, while on smaller devices the layout stacks vertically, ensuring a good user experience across desktops, tablets, and smartphones.

---

# APIs and Libraries Used

The project integrates several external services:

* **Open-Meteo API** – Provides current weather data and multi-day forecasts.
* **OpenStreetMap Nominatim API** – Converts city names to geographic coordinates and performs reverse geocoding.
* **Leaflet.js** – Displays and manages the interactive map.

---

# Skills Demonstrated

This project showcases practical frontend development skills, including:

* HTML page structuring
* Advanced CSS styling and responsive design
* JavaScript programming
* DOM manipulation
* Event handling
* Asynchronous programming with `fetch()` and `async/await`
* REST API integration
* JSON data processing
* Browser Geolocation API
* Interactive mapping with Leaflet.js
* Error handling and user-friendly interface design

---

## Overall Summary

This Weather Intelligence Dashboard is more than a simple weather application. It combines a modern responsive interface with live weather services, interactive maps, geolocation, and forecast visualization to create a complete real-world web application. It demonstrates how frontend technologies can work together with external APIs to deliver dynamic, location-based information in an intuitive and user-friendly way, making it an excellent project for showcasing skills in web development, API integration, and interactive UI design.
