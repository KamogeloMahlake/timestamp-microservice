
# Timestamp Microservice

This project is a microservice that provides timestamp conversion. It can convert a date string or a Unix timestamp into a JSON object containing both Unix and UTC timestamps.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/KamogeloMahlake/timestamp-microservice.git
    cd timestamp-microservice
    ```

2. Install the dependencies:
    ```bash
    npm install
    ```

## Usage

1. Run the application:
    ```bash
    npm run start
    ```

2. Open a web browser and navigate to `http://localhost:3000`.

## API Endpoints

- `/api/`: Returns the current timestamp in both Unix and UTC formats.
  - Example response:
    ```json
    {
      "unix": 1645795200000,
      "utc": "Wed, 26 Feb 2025 16:00:00 GMT"
    }
    ```

- `/api/:date?`: Converts a given date string or Unix timestamp to both Unix and UTC formats.
  - Example requests:
    - `/api/2025-02-26`
    - `/api/1645795200000`
  - Example responses:
    ```json
    {
      "unix": 1645795200000,
      "utc": "Wed, 26 Feb 2025 16:00:00 GMT"
    }
    ```
    ```json
    {
      "error": "Invalid Date"
    }
    ```

## Files

- `index.js`: The main file that defines the routes and logic for the timestamp microservice.
