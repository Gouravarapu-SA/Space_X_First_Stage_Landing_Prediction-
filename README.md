# Space X First Stage Landing Prediction

April 17, 2024

This document contains code to retrieve data from the SpaceX API and perform some analysis on the first stage landing success of SpaceX rockets.

## Data Retrieval

The code uses the `requests` library to make HTTP requests to the SpaceX API and retrieve data about rocket launches, payloads, cores, and other related information.

### Functions

1. `getBoosterVersion(data)`: Takes a dataset and uses the `rocket` column to call the API and append the booster version name to a list.

2. `getLaunchSite(data)`: Takes a dataset and uses the `launchpad` column to call the API and append the launch site longitude, latitude, and name to respective lists.

3. `getPayloadData(data)`: Takes a dataset and uses the `payloads` column to call the API and append the payload mass and orbit to respective lists.

4. `getCoreData(data)`: Takes a dataset and uses the `cores` column to call the API and append various core data (block, reused count, serial number, outcome, flights, grid fins, reused status, legs, and landing pad) to respective lists.

## Usage

1. Import the necessary libraries (`requests`, `pandas`, `numpy`, `datetime`).
2. Set display options for pandas DataFrame using `pd.set_option`.
3. Define the helper functions mentioned above.
4. Retrieve the launch data from the SpaceX API.
5. Process the data as needed using the helper functions.

## Note

This code assumes that you have an active internet connection and the SpaceX API is accessible. It also assumes that the API endpoints and response structure remain consistent with the code.
