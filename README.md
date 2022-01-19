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
