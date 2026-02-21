# Arduino Web Application

This project is a web application that interfaces with an Arduino device to control sensors and record video using the user's camera. It consists of a Node.js backend and a JavaScript frontend.

## Project Structure

```
arduino-web-app
├── src
│   ├── backend
│   │   ├── server.js          # Entry point for the Node.js backend
│   │   ├── serialHandler.js    # Manages serial communication with Arduino
│   │   ├── routes
│   │   │   └── sensors.js      # Defines routes for sensor management
│   │   └── config
│   │       └── arduino.js      # Configuration settings for Arduino connection
│   └── frontend
│       ├── index.html          # Main HTML file for the frontend application
│       ├── styles.css          # CSS styles for the frontend application
│       ├── js
│       │   ├── app.js          # Initializes the frontend application
│       │   ├── camera.js       # Handles camera access using getUserMedia()
│       │   ├── videoRecorder.js # Manages video recording functionality
│       │   └── sensorControl.js # Manages interaction with the backend for sensor control
│       └── pages
│           ├── dashboard.html   # Dashboard page displaying sensor data
│           └── settings.html     # Settings page for configuring sensor active time
├── package.json                 # npm configuration file
└── README.md                    # Documentation for the project
```

## Setup Instructions

1. **Clone the repository:**
   ```
   git clone <repository-url>
   cd arduino-web-app
   ```

2. **Install dependencies:**
   ```
   npm install
   ```

3. **Configure Arduino connection:**
   Update the `src/backend/config/arduino.js` file with the appropriate serial port and baud rate for your Arduino device.

4. **Start the server:**
   ```
   npm start
   ```

5. **Access the application:**
   Open your web browser and navigate to `http://localhost:3000` (or the port specified in your server configuration).

## Usage Guidelines

- Use the **Settings** page to set the sensor active time from 1 minute to 24 hours.
- The **Dashboard** page displays real-time sensor data and allows you to start video recording using your camera.
- Ensure that you grant camera access when prompted by the browser.

## Contributing

Feel free to submit issues or pull requests for any improvements or bug fixes.