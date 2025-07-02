# Weather-App-using-OpenWeather-API
Overview:
The Weather App is a command-line Python application that allows users to check real-time weather information for any city in the world. 
It fetches data such as temperature and weather conditions using the OpenWeatherMap API and displays it in a user-friendly format.

import requests

city = input("Enter city: ")
api_key = "your_api_key"
url = f"http://api.openweathermap.org/data/2.5/weather?q={city}&appid={api_key}&units=metric"

data = requests.get(url).json()
print(f"{city}: {data['main']['temp']}°C, {data['weather'][0]['description']}")
