Climate Data Analysis Project
This project utilizes Python, SQLAlchemy, Flask, and SQLite to analyze climate data from a provided database. The application includes Jupyter Notebook scripts for data exploration and analysis, as well as a Flask API for accessing summarized data and visualizations.

Table of Contents
Overview
Technologies Used
Installation
Project Structure
Jupyter Notebook Analysis
Flask API
Endpoints
Usage
Deployment
License
Overview
This project integrates data engineering and analysis techniques to explore climate data stored in a SQLite database. The data includes information such as precipitation levels, temperature observations, and station details. The project is divided into two main components: data analysis in Jupyter Notebook and API development using Flask.

Technologies Used
Python
SQLAlchemy
Flask
SQLite
Jupyter Notebook
Pandas
Matplotlib
Installation
Clone the repository:

Install dependencies:

Database Setup:

Place the provided hawaii.sqlite database file in the project's root directory.
Run the Flask application:

Project Structure
/JupyterNotebook/: Contains Jupyter Notebook files for data exploration and analysis.
/FlaskApp/:
app.py: Main Flask application file containing API endpoints.
static/: Folder for static files such as CSS, JavaScript.
templates/: HTML templates for Flask views.
Jupyter Notebook Analysis
Data Connection:

Use SQLAlchemy to connect to hawaii.sqlite.
Reflect database tables into classes using automap_base().
Create a session to interact with the database.
Data Analysis:

Perform precipitation analysis:
Retrieve last year's data.
Plot precipitation data.
Calculate summary statistics.
Perform station analysis:
Determine the number of stations.
Identify the most active station.
Retrieve temperature statistics for the most active station.
Plot temperature histogram for the most active station.
Flask API
The Flask API provides endpoints to interact with the climate data:

Endpoints
Precipitation Data:

/api/v1.0/precipitation
Returns JSON with date as the key and precipitation as the value for the last year of data.
Station Information:

/api/v1.0/stations
Returns JSON with data of all weather stations.
Temperature Observations:

/api/v1.0/tobs
Returns JSON with temperature observations for the most active weather station for the last year of data.
Temperature Statistics by Date Range:

Usage
Access the API routes using tools like Postman or a web browser.
Navigate to http://localhost:5000/ to view available routes and their functionalities.
Deployment
Deploy the Flask application to a cloud platform or server for production use. Make sure to configure environment variables and manage dependencies using a virtual environment.

