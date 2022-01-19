# MagicMirror² Weather Module with OpenWeatherMap OneCall enhancements and extra data

Default Weather module (left) vs Onecall module (right) with same design https://github.com/hangorazvan/onecall

<img style="height:1000px" src=https://github.com/hangorazvan/weather/blob/master/weather.png> <img style="height:1000px" src=https://github.com/hangorazvan/weather/blob/master/onecall.png>

#### Current weather (onecall)

- humidity
- sunrise
- sunset
- temperature
- units
- weatherType
- windDirection
- windSpeed
- feels like

plus
- dew point
- UV index
- mmHg pressure
- visibility
- description
- alerts

#### Weather forecast (hourly and daily onecall)

- date
- maxTemperature
- minTemperature
- rain
- units
- weatherType

plus
- feels like
- dew point
- UV index
- mmHg pressure
- visibility
- humidity

		{
			module: "weather",
			position: "top_left",
			header: "Current weather in",
			classes: "night currentweather current",
			disabled: false,
			config: {
				apiKey: "",
				appendLocationNameToHeader: true,
				showPrecipitationAmount: true,
				showAlerts: true
			}
		},
		{
			module: "weather",
			position: "top_left",
			header: "Hourly forecast in",
			classes: "hourly weatherforecast forecast day",
			disabled: false,
			config: {
				apiKey: "",
				appendLocationNameToHeader: true,
				type: "hourly",
				maxEntries: 4,
				initialLoadDelay: 2000,
				extra: false
			}
		},
		{
			module: "weather",
			position: "top_left",
			header: "Daily forecast in",
			classes: "daily weatherforecast forecast day",
			disabled: false,
			config: {
				apiKey: "",
				appendLocationNameToHeader: true,
				type: "daily",
				maxNumberOfDays: 8,
				initialLoadDelay: 4000,
				extra: true
			}
		},

Weather compliments to put in your config.js

			compliments: {			
					day_sunny : [
						"<i class=\"gold wi wi-day-sunny\"></i> Sunny",
					],
					day_cloudy : [
						"<i class=\"lightblue wi wi-day-cloudy\"></i> Cloudy",
					],
					cloudy : [
						"<i class=\"skyblue wi wi-cloudy\"></i> Cloudy",
					],
					day_cloudy_windy : [
						"<i class=\"powderblue wi wi-day-cloudy-windy\"></i> Cloudy windy",
					],
					day_showers : [
						"<i class=\"skyblue wi wi-day-showers\"></i> Showers",
					],
					day_rain : [
						"<i class=\"deepskyblue wi wi-day-rain\"></i> Raining",
					],
					day_thunderstorm : [
						"<i class=\"dodgerblue wi wi-day-thunderstorm\"></i> Thunderstorm!",
					],
					day_snow : [
						"<i class=\"normal wi wi-day-snow\"></i> Snowing",
					],
					day_fog : [
						"<i class=\"bright wi wi-day-fog\"></i> Fog",
					],
					night_clear : [
						"<i class=\"dimmed wi wi-night-clear\"></i> Clear night",
					],
					night_cloudy : [
						"<i class=\"powderblue wi wi-night-cloudy\"></i> Cloudy night",
					],
					night_alt_cloudy : [
						"<i class=\"powderblue wi wi-night-alt-cloudy\"></i> Cloudy night",
					],
					night_alt_showers : [
						"<i class=\"skyblue wi wi-night-alt-showers\"></i> Night showers",
					],
					night_alt_rain : [
						"<i class=\"deepskyblue wi wi-night-alt-rain\"></i> Raining night",
					],
					night_alt_thunderstorm : [
						"<i class=\"royalblue wi wi-night-alt-thunderstorm\"></i> Thunderstorm!",
					],
					night_alt_snow : [
						"<i class=\"normal wi wi-night-alt-snow\"></i> Snowing night",
					],
					night_alt_cloudy_windy : [
						"<i class=\"skyblue wi wi-night-alt-cloudy-windy\"></i> Clouds and fog",
					],
			}

Redesigned by Răzvan Cristea
https://github.com/hangorazvan
Creative Commons BY-NC-SA 4.0, Romania.