# 🏃 GPS Run Tracker

### Track Every Kilometre. Anywhere.

A lightweight, GPS-based running tracker that records your running distance, duration, and average pace without requiring a continuous internet connection.

<p align="center">
  <a href="https://bigrishi.github.io/Offline_run_logs/">
    <strong>🚀 Open GPS Run Tracker</strong>
  </a>
</p>

---

## 📌 About the Project

GPS Run Tracker is a browser-based running application designed to help users track outdoor running sessions using their device's GPS.

The application works as a Progressive Web App (PWA), allowing users to install it on their Android home screen and access its cached application interface offline.

It uses the browser's Geolocation API to collect GPS coordinates and calculate running statistics.

## ✨ Features

- **GPS Tracking:** Records your location using your device's GPS.
- **Distance Calculation:** Calculates total distance travelled.
- **Run Timer:** Tracks elapsed running time.
- **Average Pace:** Calculates average pace in minutes per kilometre.
- **Periodic GPS Sampling:** Collects location samples every 40 seconds.
- **Final GPS Reading:** Requests a final location reading when you stop the run.
- **CSV Export:** Exports GPS records, timestamps, coordinates, and accuracy.
- **Offline Support:** The PWA application shell can be accessed offline after it has been cached.
- **Installable:** Can be added to your Android home screen through Chrome.

## ⚙️ How It Works

1. Open the application and allow location permission.
2. Press **Start** to begin tracking.
3. The application records an initial GPS location and starts the timer.
4. Additional GPS readings are collected every 40 seconds.
5. Press **Stop** to stop the timer and request a final GPS reading.
6. View your running statistics and export the recorded GPS data as a CSV file.

## 📐 Distance Calculation

The application uses the Haversine formula to calculate the distance between two GPS coordinates on the Earth's surface.

The total distance is calculated by adding the distances between consecutive GPS samples.

Average pace is calculated as:

`Average Pace = Total Time / Total Distance`

The result is displayed in minutes per kilometre.

## 📱 Installation

### Android

1. Open the [GPS Run Tracker](https://bigrishi.github.io/Offline_run_logs/) link in Google Chrome.
2. Allow location permission when prompted.
3. Open Chrome's menu.
4. Select **Add to Home screen** or **Install app**, if available.
5. Launch the application from your home screen.

### Desktop

Open the live application using a modern browser that supports the Geolocation API.

## 🌐 Offline Functionality

The application uses a service worker to cache its essential files.

Once the application has been loaded online and its files have been cached, the application interface can be opened without an internet connection.

**Important:** GPS tracking still requires the device's Location setting to be enabled. Offline access does not guarantee uninterrupted tracking if Android suspends the browser or closes the application.

Export your CSV file before closing or reloading the application because recorded session data is currently held in application memory.

## 🔐 Privacy

- Location data is processed locally by the application.
- GPS coordinates are not intentionally uploaded to a server.
- Users can export their recorded GPS data as a CSV file.
- Location permission is required for GPS tracking.

## 🛠️ Technologies Used

- HTML5
- CSS3
- JavaScript
- Browser Geolocation API
- Progressive Web App (PWA)
- Service Workers
- Web App Manifest
- GitHub Pages

## 📂 Project Structure

```text
Offline_run_logs/
│
├── index.html
├── manifest.webmanifest
├── sw.js
├── icon-192.png
├── icon-512.png
└── README.md
```

## ⚠️ Limitations

- GPS accuracy depends on the device and surrounding environment.
- Buildings, trees, and poor satellite visibility may affect location accuracy.
- GPS sampling every 40 seconds may not capture every turn or movement precisely.
- Background tracking is not guaranteed when the browser is suspended.
- Export your run data before closing or refreshing the application.

## 🚀 Future Enhancements

- Run history and session storage.
- Interactive route maps.
- Live speed and pace monitoring.
- Improved background tracking.
- Weekly and monthly running statistics.
- Personal running goals and progress reports.

## 🎯 Project Goal

The goal of GPS Run Tracker is to provide a simple, accessible, and privacy-conscious running tracker that works without depending on continuous internet connectivity.

---

<p align="center">
  **Track your run. Measure your progress. Keep moving!** 🏃
</p>
