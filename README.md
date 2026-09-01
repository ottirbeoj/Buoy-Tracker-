# Buoy Watch and Telemetry Monitoring System

A fully browser-based marine buoy monitoring dashboard built for ICMB buoy telemetry data.
No server, no database, no installation - just open the page, upload your Excel file, and everything runs in your browser.

## Features

- Interactive Map with buoy track, drift path, and heatmap
- Watch Zone Engine using Haversine distance calculation
- Watch Status: SAFE / WARNING / BREACH auto-detected per GPS fix
- Sensor Charts: Battery, Temperature, Salinity, pH, Current Speed, Depth, Distance
- Ocean Gauges: Live readout of all oceanographic parameters
- Full Data Table with 30+ telemetry columns and real-time search
- Alarm Log with breach/warning events and auto-computed duration
- Excel Export with distances and watch status added
- Settings saved in localStorage (survives page refresh)
- Mobile Responsive with bottom navigation bar

## Accepted File Formats

### Format 1 - Standard 4G Format
Columns: Buoy ID, Time stamp, Date and time, Latitude, Longitude, Battery voltage, Depth,
Temperature, Salinity, DO, pH, Nitrate, Nitrite, Ammonia, Phosphate, Silicate,
pCO2 Air, pCO2 Water, Chlorophyll, Turbidity, Scattering, Hydorcarbon refined,
Hydrocarbon crude, CDOM, Phycocyanin, Phycoerythrin, Methane, Current speed, Current direction

### Format 2 - INSAT Format
Columns: Station ID, Timestamp, Received Time (UTC), Observation Time (IST), Latitude, Longitude,
Battery Voltage, Sensor Depth, Water Temperature, Salinity, Dissolved Oxygen, pH, Nitrate,
Nitrate Nitrite, Ammonium, Phosphate, Silicate, pCO2 Air, pCO2 Water, Chlorophyll, Turbidity,
Scattering @ 700nm, Hydrocarbon Refined, Hydrocarbo Crude, CDOM, Phycocyanin, Phycoerythrin,
Dissolved Methane, Current Speed, Current Direction

Files not matching either format are rejected with a clear error message.

## How to Use

1. Open the app URL in any modern browser
2. Upload your .xlsx or .xls file using the sidebar drag-and-drop area
3. The app parses everything in your browser - no data is sent to a server
4. Adjust Anchor coordinates and Watch Radius as needed
5. Explore Map, Sensor Charts, and Data Table tabs
6. Click Export Excel to download the analysed dataset

## Deploy to GitHub Pages

1. Fork or clone this repository
2. Go to Settings -> Pages -> Source: main branch / root
3. App will be live at: https://YOUR_USERNAME.github.io/REPO_NAME/

## Local Development

No build tools needed. Just open index.html in a browser.

## Tech Stack

- Leaflet.js 1.9.4 - Interactive map
- Leaflet.heat 0.2.0 - Heatmap layer
- SheetJS xlsx 0.18.5 - Excel parsing and export
- Chart.js 4.4.3 - Sensor time-series charts
- chartjs-plugin-zoom 2.0.1 - Chart zoom and pan
- Hammer.js 2.0.8 - Touch gesture support
- CARTO Dark Tiles - Ocean-themed map background

All libraries loaded via CDN - no npm install needed.

## Privacy

All data is processed entirely in your browser.
Your Excel files are never uploaded to any server.

## License

MIT