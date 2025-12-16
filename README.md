# 🗺️ Rick Maps

**Rick Maps** is a lightweight, web-based GPS navigation application built with Vanilla JavaScript and Tailwind CSS. It utilizes **OpenStreetMap (OSRM)** for routing and **Leaflet** for map rendering, offering a mobile-first navigation experience directly in the browser.

![Version](https://img.shields.io/badge/version-1.1.0-green)
![Status](https://img.shields.io/badge/status-active-blue)

## ✨ Features

### 🚗 Navigation & Routing
* **Turn-by-Turn Navigation:** Real-time routing using the OSRM API.
* **Travel Modes:** Toggle between **Driving** 🚗 and **Cycling** 🚲 modes (updates route paths and ETAs).
* **Live Metrics:** dynamic display of:
    * Speedometer (Floating UI).
    * Estimated Time of Arrival (ETA).
    * Distance remaining.
* **Avoid Tolls:** Option to calculate routes excluding toll roads.

### 📍 Favorites & Shortcuts
* **Smart History:** Automatically tracks recent search history.
* **Saved Locations:** Save locations as:
    * 🏠 **Home**
    * 💼 **Work**
    * ❤️ **Custom Favorites**
* **Quick Access:** One-tap navigation from the home screen to saved destinations.
* **Local Privacy:** All favorites and history are stored in your browser's `localStorage` — no external database is used.

### 🎨 UI/UX
* **Dark Mode Support:** Adaptive UI for night-time driving.
* **Responsive Design:** Mobile-first interface with large touch targets.
* **Toast Notifications:** Non-intrusive alerts for app status and errors.

---

## 🛠️ Tech Stack

* **Core:** HTML5, Vanilla JavaScript (ES6+).
* **Styling:** [Tailwind CSS](https://tailwindcss.com/) (via CDN).
* **Maps:** [Leaflet.js](https://leafletjs.com/).
* **Routing API:** [OSRM (Open Source Routing Machine)](http://project-osrm.org/).
* **Icons:** Lucide Icons.

---

## 🚀 Getting Started

Since Rick Maps relies on CDNs and Vanilla JS, there is no heavy build process.

### Prerequisites
* A modern web browser (Chrome, Firefox, Safari, Edge).
* An active internet connection (for fetching map tiles and API routes).

### Installation
1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/Rick007110/Rick-Maps.git](https://github.com/Rick007110/Rick-Maps.git)
    ```
2.  **Navigate to the folder:**
    ```bash
    cd Rick-Maps
    ```
3.  **Run the app:**
    * Simply open `index.html` in your browser.
    * *Tip:* For the best experience (geolocation features), run it via a local server (e.g., Live Server in VS Code or Python `http.server`).

---

## 🔄 Changelog

### [v1.1.0] - Latest
**New Features**
* **Multi-Mode Routing:** Added infrastructure to switch between Car (`routed-car`) and Bike (`routed-bike`) routing profiles.
* **Favorites System:** Completely overhauled the start screen. Users can now save, edit, and quickly launch routes to Home, Work, and Favorites.
* **Dynamic UI:** Added a floating speedometer and connected route stats (ETA/Distance) to live data streams.

**Fixes & Improvements**
* Refactored global settings (Metric/Imperial, Voice, Tolls).
* Replaced static HTML placeholders with dynamic DOM injection.
* Improved error handling for missing GPS signals.

---

## ⚙️ Configuration

The app manages settings via `localStorage`. The following keys are used:
* `HOME_LOCATION`: JSON object containing lat/lon/name for Home.
* `WORK_LOCATION`: JSON object containing lat/lon/name for Work.
* `FAVORITE_LOCATIONS`: Array of saved favorite objects.
* `TRAVEL_MODE`: Saves the last used mode ('driving' or 'cycling').
* `USE_METRIC`: Boolean for unit preference.
* `AVOID_TOLLS`: Boolean for routing preference.

---

## 🤝 Contributing

Contributions are welcome!
1.  Fork the Project
2.  Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3.  Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4.  Push to the Branch (`git push origin feature/AmazingFeature`)
5.  Open a Pull Request

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for more information.
