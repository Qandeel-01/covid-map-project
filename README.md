# Interactive COVID-19 Map

An interactive web map that visualizes live global COVID-19 statistics by country. Built with [Leaflet](https://leafletjs.com/) and powered by the free [disease.sh](https://disease.sh/) API.

**Live site:** https://qandeel-01.github.io/covid-map-project/

---

## Features

- **Live data** — pulls current country-level COVID-19 statistics from the disease.sh API on page load
- **Three toggleable layers** — Cases (orange), Deaths (red), Recovered (green)
- **Proportional circles** — marker size scales with the metric value
- **Detailed popups** — click any country to see total cases, active, deaths, recovered, today's new cases/deaths, and population
- **Standard map controls** — zoom (wheel + buttons), pan (click-and-drag), world wrap
- **Legend** — bottom-right corner shows what each color represents
- **Responsive** — works on desktop and mobile viewports

---

## Tech Stack

| Component     | Purpose                                    |
| ------------- | ------------------------------------------ |
| Leaflet 1.9.4 | Interactive map rendering                  |
| OpenStreetMap | Base map tiles                             |
| disease.sh    | Live COVID-19 data (no API key required)   |
| GitHub Pages  | Static hosting                             |

---

## Project Structure

```
covid-map-project/
├── index.html    # Complete single-page app (HTML + CSS + JS)
└── README.md
```

Everything lives in `index.html` — no build step, no dependencies to install.

---

## Running Locally

1. Clone the repository:
   ```bash
   git clone https://github.com/Qandeel-01/covid-map-project.git
   cd covid-map-project
   ```
2. Open `index.html` directly in a browser, **or** serve it locally:
   ```bash
   python -m http.server 8000
   # then visit http://localhost:8000
   ```

An internet connection is required at runtime so the map can fetch tiles and COVID data.

---

## Deployment

Deployed via **GitHub Pages** from the `main` branch, root folder (`/`).

To enable Pages on a fork:

1. Go to **Settings → Pages**
2. Under **Source**, select branch `main` and folder `/ (root)`
3. Click **Save**
4. Wait ~30 seconds, then visit `https://<your-username>.github.io/covid-map-project/`

---

## Data Source

Country statistics come from:
```
https://disease.sh/v3/covid-19/countries
```
See the [disease.sh docs](https://disease.sh/docs/) for the full response schema.

---

## License

Released under the [MIT License](https://opensource.org/licenses/MIT).

---

## Author

**Qandeel** — [github.com/Qandeel-01](https://github.com/Qandeel-01)
