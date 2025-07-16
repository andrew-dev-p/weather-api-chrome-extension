# Weather Chrome Extension ☀️🌧️

A **React-based Chrome extension** that brings real-time weather updates to your browser! Add multiple cities, view weather overlays on any page, and enjoy a sleek, Material-UI powered interface—all with persistent settings and OpenWeatherMap integration.

## 🔍 Description

This extension lets you:
- Track weather for multiple cities
- Instantly view weather overlays on any webpage
- Set a home city and see its temperature in the extension badge
- Add cities from selected text via context menu
- Switch between Celsius and Fahrenheit
- Enjoy a modern, responsive UI

All data is stored locally in your browser, and weather is fetched from the OpenWeatherMap API.

## 📁 Project Structure

```
.
├── src/
│   ├── background/         # Background scripts (context menu, alarms, badge)
│   ├── components/
│   │   └── WeatherCard/    # Weather display component
│   ├── contentScript/      # Overlay logic for weather on web pages
│   ├── options/            # Options page (home city, overlay toggle)
│   ├── popup/              # Popup UI (main extension window)
│   ├── static/             # manifest.json, icon
│   └── utils/              # API, storage, messages
├── package.json
├── webpack.*.js            # Webpack configs
└── README.md
```

## 🚀 Features

- **Add/Remove Cities** to track weather
- **Weather Overlay** on any webpage
- **Temperature Scale Toggle** (°C/°F)
- **Persistent Settings** (home city, overlay, city list)
- **Context Menu Integration** (add city from selected text)
- **Extension Badge** with current temperature
- **Material-UI Design** for a clean, modern look

## 🛠️ Tech Stack

- **React 17**
- **TypeScript**
- **Material-UI**
- **Webpack 5**
- **Chrome Extension Manifest v3**
- **OpenWeatherMap API**

## ⚙️ Installation

### 1. Clone the Repo

```bash
git clone https://github.com/andrew-dev-p/weather-api-chrome-extension
cd weather-api-chrome-extension
```

### 2. Install Dependencies

```bash
npm install
```

### 3. Add OpenWeatherMap API Key
- Open `src/utils/api.ts`
- Replace `"OPEN_WEATHER_API_KEY"` with your actual API key.

### 4. Build the Extension

```bash
npm run build
```
- Output will be in the `dist/` folder.

## 🧪 Loading the Extension in Chrome

1. Open Chrome and go to `chrome://extensions/`
2. Enable **Developer mode** (top right)
3. Click **Load unpacked**
4. Select the `dist/` folder

## 🔐 Environment Variables
- No `.env` file; API key is set directly in `src/utils/api.ts`.

## 📬 Usage
- Click the extension icon to open the popup.
- Add cities, switch temperature scale, or toggle overlay.
- Use the options page to set your home city and overlay preference.
- Right-click selected text on any page to add it as a city.

## 🚀 Deployment
- Build with `npm run build`
- Zip the `dist/` folder and upload to the Chrome Web Store.

---

**Enjoy instant weather updates—right in your browser!**
