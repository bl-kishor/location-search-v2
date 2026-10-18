# Location Search

A small React app for learning how to connect a location search to an interactive map. It combines Leaflet, OpenStreetMap data, Tailwind CSS, and TypeScript.

## Live demo

[Try Location Search](https://location-search-virid.vercel.app/)

## How it works

1. Enter a place name in the search panel and submit the form.
2. The app requests up to five matching addresses from the Nominatim search service.
3. Choose a result with **Go** to move the map to that location and show its marker.

The map starts centered near New York City. Search results are held in React state and passed between the search panel and map as typed `Place` data.

## Learning topics

- Embedding and controlling a Leaflet map with React Leaflet
- Fetching and mapping geocoding results into application data
- Sharing state and typed props between React components
- Applying utility classes with Tailwind CSS

## Tech stack

- React 19 and TypeScript
- Vite
- Leaflet and React Leaflet
- Tailwind CSS 4
- OpenStreetMap tiles and the Nominatim search API

## Getting started

Use a current Node.js installation with npm. Install dependencies and start the development server:

```bash
npm install
npm run dev
```

Search uses the public Nominatim service, and map tiles come from OpenStreetMap. The app does not currently require an API key.

## Project structure

| Path | Purpose |
| --- | --- |
| `src/App.tsx` | Holds the selected place and lays out the search panel and map |
| `src/components/LocationSearch.tsx` | Submits location searches and displays results |
| `src/components/Map.tsx` | Renders the map, moves to the selected place, and displays its marker |
| `src/api/search.ts` | Calls Nominatim and converts results into `Place` objects |
| `src/api/Place.ts` | Defines the location data type |
| `src/index.css` | Loads Tailwind CSS |

## Available scripts

| Command | Description |
| --- | --- |
| `npm run dev` | Start the development server |
| `npm run build` | Type-check and build for production |
| `npm run preview` | Preview the production build locally |
| `npm run lint` | Run ESLint |
