# DC Food Desert Simulation

An interactive simulation tool designed to help alleviate food deserts in Washington, DC by visualizing and analyzing grocery store accessibility patterns.

## Website Link
[https://gtownhack.vercel.app/](https://gtownhack.vercel.app/)


## Overview

This project helps urban planners and policymakers combat food deserts in DC by simulating residents' access to grocery stores. Using real-time animations and demographic data, it visualizes how residents navigate to their nearest grocery stores, highlighting areas where access to fresh food is limited and how adding new grocery stores could combat food insecurity.

## Purpose

- **Food Desert Analysis**: Identify underserved areas where residents lack easy access to fresh, healthy food
- **Impact Assessment**: Simulate how adding new grocery stores could improve food accessibility
- **Policy Planning**: Help decision-makers visualize the impact of potential solutions
- **Community Understanding**: Demonstrate the real-world challenges residents face in accessing grocery stores

## Features

- **Interactive 3D Map**

  - Real-time simulation of residents traveling to grocery stores
  - Food desert visualization with intensity levels
  - Census tract demographics and food access metrics
  - Grocery store coverage analysis

- **Simulation Tools**

  - Add potential new grocery store locations via drag-and-drop
  - Watch how new stores affect resident travel patterns
  - Analyze impact on food desert zones

- **Data Insights**
  - Population density and demographic overlays
  - Walking distance analysis
  - Food insecurity heat maps
  - Demographic statistics

## Technology Stack

- **Frontend**

  - Next.js 15.1.6
  - TypeScript
  - Mapbox GL JS
  - Turf.js for geospatial calculations

- **Data Sources (DC area only)**
  - DC Census tract boundaries
  - Current fully operational grocery store locations
  - Demographic data
  - Food access metrics

## Setup

1. Clone the repository:

   ```bash
   git clone [repository-url]
   cd gtown_hack
   ```

2. Install dependencies:

   ```bash
   npm install
   ```

3. Create a `.env.local` file with your Mapbox token:

   ```
   MAPBOX_TOKEN=your_mapbox_token_here
   ```

4. Run the development server:

   ```bash
   npm run dev
   ```

5. Open [http://localhost:3000](http://localhost:3000) in your browser

## How It Works

### Population Simulation

- Green dots represent DC residents moving between homes and grocery stores
- Movement follows actual walking routes using Mapbox Directions API
- One dot per census tract shows typical travel patterns
- Routes update dynamically when new stores are added

### Food Desert Analysis

- Color gradient showing food insecurity levels:
  - 0-30%: Light pink (minimal food access issues)
  - 30-50%: Light orange (emerging food desert)
  - 50-70%: Orange-red (significant food access problems)
  - 70-100%: Deep red (severe food desert)

### Impact Assessment

- Drag and drop new grocery stores onto the map
- Watch real-time updates to resident travel patterns to grocery stores
- See impact on people's accessibility to their nearest grocery stores
- Observe improved convenience for people closer to a new grocery store

### Data Visualization

- Hover over census tracts to view:
  - Total population affected
  - Current food access metrics
  - Demographic breakdown
- Click grocery stores to view:
  - Store details
  - Population/Ward served
  - Coverage area

## Using the Simulation

1. **Observe Current State**

   - Watch green dots move along actual roads and sidewalks
   - Note areas with longer travel times
   - Identify food desert zones (darker red areas)

2. **Test Solutions**

   - Drag new grocery store icons onto the map
   - Watch how travel patterns and flow change
   - New stores result in shorter travel for people in food insecure areas

3. **Analyze Impact**
   - Review updated metrics
   - Compare travel times
   - Assess population coverage
   - Evaluate demographic impact
