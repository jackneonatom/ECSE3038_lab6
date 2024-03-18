# Project README

This code is designed to facilitate temperature and light monitoring using an Arduino board, in conjunction with various sensors and an HTTP API. The purpose of this assignment could be to create a system for environmental monitoring and reporting.

## Functions and Expected Operation

### `putTemp(float temp)`
- **Purpose**: This function is responsible for sending temperature data to the specified API endpoint.
- **Operation**: It constructs a JSON payload containing the temperature data, makes a PUT request to the API endpoint, and logs the response. Additionally, it prints the temperature and light data to the serial monitor.

### `getLight()`
- **Purpose**: This function retrieves light data from the designated API endpoint.
- **Operation**: It sends a GET request to the API endpoint and processes the response. If successful, it extracts the light information from the JSON response and controls the LED pin based on the light data.

### `setup()`
- **Purpose**: This function initializes the serial communication, connects to the specified WiFi network, and sets the LED pin as an output.
- **Operation**: It begins serial communication, establishes a connection to the WiFi network, and configures the LED pin for output.

### `loop()`
- **Purpose**: This function continuously checks the WiFi connection status and, if connected, retrieves temperature and light data.
- **Operation**: It continuously monitors the WiFi connection status. When the connection is established, it requests temperature data from the sensor, sends the data to the API using `putTemp()`, and retrieves light data using `getLight()`.

## Assignment Purpose
The purpose of this assignment may be to implement a system that collects temperature and light data from sensors, sends the data to a remote server via HTTP requests, and controls an output (such as an LED) based on the received light information. This system could be utilized for environmental monitoring, allowing the collection and remote access of real-time data.

Feel free to modify and extend the code for your specific application needs.

If you have any further questions or need additional assistance, please feel free to ask!
