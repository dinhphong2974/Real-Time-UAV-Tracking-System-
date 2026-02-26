# Real-Time-UAV-Tracking-System-
Developed a telemetry dashboard using a smartphone to simulate UAV flight. Engineered a JSON data pipeline to stream real-time GPS coordinates for centralized trajectory visualization and monitoring
# Real-Time UAV Tracking System 🚁

A telemetry dashboard that simulates UAV flight using a smartphone. This system engineers a JSON data pipeline to stream real-time GPS coordinates from a client device to a centralized server, allowing for live trajectory visualization and monitoring on an interactive map.

## 📂 Project Structure

* **`app.py`**: The main application script that initializes a local Flask server to receive data and launches a PyQt5 desktop GUI for management.
* **`gps_sender.html`**: A web-based client application. Open this on a smartphone to capture its GPS location and stream it to the server.
* **`map.html`**: The web dashboard utilizing Leaflet.js. It fetches the streaming data and visualizes the UAV trajectories on an interactive map.
* **`positions.json`**: The local JSON storage file where the server logs all received GPS coordinates.

## ✨ Key Features

* **Real-time Telemetry:** Streams live GPS data (Latitude, Longitude) from any browser-enabled device.
* **Live Trajectory Map:** Visualizes multiple UAV paths dynamically using Leaflet.js.
* **Device Filtering:** Includes a control panel to toggle the visibility of different UAVs on the map.
* **Local Server & GUI:** Uses Flask to handle API requests and PyQt5 for a desktop control interface.

## 🚀 How to Run

1.  **Start the Server:**
    Run the main Python script to start the Flask server and the PyQt5 GUI.
    ```bash
    python app.py
    ```
2.  **Start Sending GPS Data:**
    * Find your computer's local IP address (e.g., `192.168.1.x`).
    * Open `gps_sender.html` and update the `fetch` URL with your IP.
    * Open this file on your smartphone (or any device with GPS) to begin broadcasting coordinates.
3.  **Monitor the Flight:**
    * Open `map.html` in your browser. (Note: Ensure the `ngrok` URL in the script is active or updated to your local IP for local testing).
    * Watch the UAV's path update in real-time!

---
*Built with Python (Flask, PyQt5), JavaScript, and Leaflet.js.*
