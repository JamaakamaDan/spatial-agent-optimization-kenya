# Spatial Optimization of Urban Financial Agent Networks in Kenya

An end-to-end spatial data science pipeline using graph theory, sparse matrix operations, and location-allocation algorithms to optimize mobile money agent locations across major Kenyan cities.

## Executive Summary
Mobile money platforms like M-PESA drive financial inclusion in East Africa, yet physical agent networks face spatial coverage gaps and liquidity distribution costs. This project models:
1. **Maximum Coverage Location Problem (MCLP):** Optimal placement of agents within a strict 2,000m pedestrian walking radius.
2. **Minimum Spanning Tree (MST):** Cash-in-transit (CIT) street-level routing connecting agents to minimize operational logistics costs.

## Results Overview

| City | Mapped Demand Structures | Optimal Agents Placed | Total Coverage achieved (%) |
| :--- | :---: | :---: | :---: |
| **Mombasa** | 53,838 | 20 | **99.3%** |
| **Kisumu** | 100,171 | 20 | **91.8%** |
| **Nakuru** | 101,019 | 20 | **91.5%** |
| **Nairobi** | 211,984 | 20 | **86.2%** |

## Key Features & Methodology
- **Geospatial Ingestion:** Extracted road network graphs and building footprints via `OSMnx` using a 7.5km spatial radius.
- **Sparse Matrix Acceleration:** Handled graph distances ($O(N^2)$ scaling) via `scipy.sparse.csc_matrix` and boundary-constrained Dijkstra ego-graphs.
- **Logistics Routing:** Computed exact street-level shortest paths using `NetworkX` graph topologies.
- **Interactive Visualizations:** Exported multi-layer HTML dashboards built with `Folium`.

## Quickstart

```bash
# Clone the repository
git clone [https://github.com/YOUR_USERNAME/spatial-agent-optimization-kenya.git](https://github.com/YOUR_USERNAME/spatial-agent-optimization-kenya.git)
cd spatial-agent-optimization-kenya

# Install dependencies
pip install -r requirements.txt

# Run the optimization pipeline
python src/pipeline.py