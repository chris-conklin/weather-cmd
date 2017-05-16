
# weather-cmd

command line weather information using various tools


## For api requests
https://darksky.net/dev/docs/forecast

https://api.darksky.net/forecast/[key]/[latitude],[longitude]

a request for the example area with my key embedded:
curl https://api.darksky.net/forecast/${WEATHER_KEY}/42.3601,-71.0589

$ curl https://api.darksky.net/forecast/${WEATHER_KEY}/42.3601,-71.0589 |  jq .currently.temperature

## Query Using Python

quick and dirty notes from a test I ran:
pip install requests

>>> WEATHER_KEY='24eabababab........'
>>> import requests
>>> response = requests.get('https://api.darksky.net/forecast/' + WEATHER_KEY + '/42.3601,-71.0589')
>>> print(response.content)


