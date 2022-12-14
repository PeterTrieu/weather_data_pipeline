# Introduction

Hi all,

The language used to write the weather data pipeline solution was Python.
<div id="header" align="center">
  <img src="https://media0.giphy.com/media/KAq5w47R9rmTuvWOWa/giphy.gif" width="100"/>
</div>

The modules that are used in this solution are listed below.
- [json](https://docs.python.org/3/library/json.html) - JSON encoder and decoder
- [os](https://docs.python.org/3/library/os.html) - Miscellaneous operating system interfaces
- [collections](https://docs.python.org/3/library/collections.html) - Container datatypes
- [csv](https://docs.python.org/3/library/csv.html) - CSV File Reading and Writing
- [datetime](https://docs.python.org/3/library/datetime.html) - Basic date and time types
- [shutil](https://docs.python.org/3/library/shutil.html) - High-level file operations

## How to run solution
To run the solution, the following is required:
- Ensure that the data to be processed is located within a folder called **weather_data**, that is on the same folder level as the **data_pipeline.py** script
- Ensure that there are folders called **archived_weather_data** and **weather_results** that are on the same folder level as **data_pipeline.py** script
- Drop the JSON files to be processed into the folder **weather_data** folder
- For the JSON files that will be processed, it must be in a similar format as shown below:
```
[
    {
        "LocalObservationDateTime": "2022-08-04T09:55:00+08:00",
        "EpochTime": 1659578100,
        "WeatherText": " MOstlY ClOudy ",
        "WeatherIcon": 6,
        "HasPrecipitation": false,
        "PrecipitationType": null,
        "IsDayTime": true,
        "Temperature": {
            "Metric": {
                "Value": 12.2,
                "Unit": "C",
                "UnitType": 17
            },
            "Imperial": {
                "Value": 54.0,
                "Unit": "F",
                "UnitType": 18
            }
        },
        "city": " pERTH "
    }
]
```
Run the **data_pipeline.py** script to generate the weather results as a csv file located in the **weather_results** folder, it will also archive all the JSON files into the **archived_weather_data** folder and rename the files with the start date and city name of the data.