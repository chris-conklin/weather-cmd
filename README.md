
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


### Desired Output

Wed, May 17, 2017 8:14 am

Chapel Hill, NC 	Currently: 85	H/L: 93/83	Precip: 20%
----------------------------------------------------------------------
 9   10   11   12   1   2   3   4   5   6   7   8   9   10   11   12
----------------------------------------------------------------------
 0%  20%  20%  20%  30% 0%  0%  0%  0%  0%  0%  0%  0%   0%   0%   0%
 85  87   89   89   89  90  93  90  88  86  84  83  83   83   83   83 

Tavares, FL	Currently: 85	H/L: 93/83	Precip: 20%


