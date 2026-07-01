# Map of Japan Weather Stations

This folder contains information and code on how to draw a informative map of the Automated Meteorological Data Acquisition System (AMeDAS) weather stations of the Japan Meteorological Agency (JMA). The location of the weather stations are marked on the map, and information such as the type of meteorlogical data collected are provided with pop-ups. The map also provides information useful for data scraping (`prec_no`, `block_no` and whether the weather station is a `s` or `a` type station).

## Links
[See the map here](https://datadrivenmai.com/projects/map-japan-weather-stations/)
[Read the full project documentation here](https://datadrivenmai.com/projects/map-japan-weather-stations/deets-n-docs.html)

## Project Structure
- `README.md` (you are here)
- `map-japan-weather-stations.ipynb`
    - Jupyter notebook that generates the Quarto dashboard with the two maps
- `deets-n-docs.ipynb`
    - Jupyter notebook identical to the [full project documentation online](https://datadrivenmai.com/projects/map-japan-weather-stations/deets-n-docs.html)
- `data/`
    - contains the CSV file with the data of all weather stations
- `images/`

## The Ins and Outs
### Input 
- None

### Output
- Folium maps
    - A simpler map of all AMeDAS stations 
    - Six informative regional maps that display the more information about each weather station through pop-ups

## Project Value

### Motivation
When data scraping Japan's weather data, it can be time-consuming to search for the closest weather station to a desired spot, navigate the JMA website, and identify the parameters needed to pinpoint its URL (`prec_no`, `block_no` and whether it is a `s` or `a` type station). This map helps data scrapers to quickly locate the desired weather station on a map, figure out whether the required meteorological data is collected, and note the parameters needed when data scraping. 

### Key Skills Demonstrated
- Scrape data from URL links to identify a JMA stations's `prec_no` and `block_no`
- Read a file of unknown encoding 
- Convert Japanese 'reki' type dates into the Gregorian calendar
- Convert names of places from Japanese to romaji (using English alphabet)
- Draw stations on a map using `folium`
    - Generate simple HTML for legends, mouse-over text, and pop-up text 

## How to Run
To get the final maps, open the `map-japan-weather-stations.ipynb` notebook and run all cells sequentially. If you'd like to trace through the data collection and preprocessing steps taken, please refer to the `deets-n-docs.ipynb` notebook. 

### Requirements for Code to Run
- Python 3 (Verified on 3.14.3)
- Python libraries for `map-japan-weather-stations.ipynb`
    - `pandas`
    - `folium`
    - `base64`
    - `IPython.display`
- Python libraries for `deets-n-docs.ipynb`
    - `pandas`
    - `requests`
	- `time`
    - `bs4`
- `data/` subfolder to save or load the `amedas-df-all.csv` file 
