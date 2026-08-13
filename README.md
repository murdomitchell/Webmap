# TIGIS Webmap

An interactive web map built for the University of Edinburgh's 2025 Capitol Greenspace Group 5 project. It visualises the output of an Analytic Hierarchy Process (AHP) model that ranked 65 Category C-listed buildings in Edinburgh for potential retrofitting into new community centres.

Designed for government and council stakeholders, the map lets users dynamically explore final site scores and see how they're shaped by four ranking criteria: **Deprivation**, **Accessibility**, **Greenspace Type**, and **Proximity to Nearest Existing Community Centre**.

<!--screenshot-->

**Live demo** (University of Edinburgh network access required, may not always be available): https://www.geos.ed.ac.uk/dev/cgsgroup5

## My Role

I was the primary developer of this codebase — the Oracle database integration, SQL data layer, and the Leaflet-based interactive front-end — with contributions from my Capitol Greenspace Group 5 teammates on the underlying AHP analysis and data preparation.

## Tech Stack

- **Backend:** Python (Flask, GeoPandas), Oracle database (`oracledb`)
- **Frontend:** JavaScript, HTML/CSS, Leaflet

## Running the Development Version

Requires University of Edinburgh VPN or Remote Desktop access, and permission to the relevant Oracle SQL data tables.

1. Install dependencies: `flask`, `geopandas`, `python-dotenv`, `oracledb`, `pathlib` (and their dependencies).
2. Create a `.env` file with your Oracle credentials:
   ```
   ORACLE_USER=s1234567
   ORACLE_PASSWORD=***
   ```
   Point `dotenv.load_dotenv()` in [`app.py`](app.py) at this file if it isn't in the same folder.
3. Run [`app.py`](app.py), then open http://127.0.0.1:5000 in your browser.
   (Change the port by passing it to `app.run()`.)
