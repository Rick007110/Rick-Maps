add travel modes, favorites system, and dynamic navigation UI (v1.1.0)
**New Features**
* **Travel Modes:** Added support for 'Driving' and 'Cycling' modes.
  * Implemented `setTravelMode()` to toggle profiles.
  * Updated OSRM API calls to switch between `routed-car` and `routed-bike` endpoints.
  * Added UI selectors for travel modes in the route preview.
* **Favorites System:**
  * Implemented `localStorage` persistence for "Home", "Work", and custom "Favorites".
  * Added `save-location-modal` UI for saving destinations.
  * Added logic to prevent duplicate entries in favorites.
* **Dynamic Home Screen:**
  * Added `renderHomeShortcuts()` to inject saved locations into the start screen.
  * Replaced hardcoded "Recent" suggestions with dynamic history rendering.
* **Speedometer:** Added a floating speedometer component (`#speedometer`) to the active navigation view.

**UI/UX Improvements**
* **Dynamic Route Stats:** Replaced static HTML placeholders with dynamic IDs (`#preview-duration`, `#preview-eta`, `#nav-distance-speed`) to allow real-time updates.
* **Loading States:** Added "Calculating route..." feedback labels during API fetches.
* **Toast Notifications:** Added alerts for missing Home/Work presets and successful saves.

**Refactoring & Configuration**
* **Global Settings:** Centralized settings state (`TRAVEL_MODE`, `USE_METRIC`, `AVOID_TOLLS`) with local storage initialization.
* **Cleanup:** Removed hardcoded static route data (e.g., "Empire State Building" mocks) in favor of dynamic DOM manipulation.
* **Version:** Bumped application version to `1.1.0`.
