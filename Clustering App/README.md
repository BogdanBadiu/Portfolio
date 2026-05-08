# Clustering App

A C# / WinForms desktop application for visualizing and benchmarking clustering algorithms on 2D point datasets.
Originally developed as part of my **Bachelor's thesis**: *Comparative study between different clustering algorithms* (final grade 9.60/10).

## Algorithms Implemented

- **DBSCAN** (`Class/DBSCAN.cs`) — density-based clustering with `eps` (neighborhood radius) and `minPoints` parameters. Identifies arbitrary-shaped clusters and marks outliers as noise (`ClusterId = -1`).
- **Hierarchical Agglomerative Clustering (HAC)** (`Class/HAC.cs`) — bottom-up clustering with two linkage strategies:
  - **Single-link** (minimum distance between clusters)
  - **Complete-link** (maximum distance between clusters)

## Features

- Loads 2D point datasets from `.txt` files (sample datasets included with 3, 4, 5, 6, 7, 8 clusters)
- Runs DBSCAN or HAC (single- or complete-link) on the loaded points
- Visualizes the resulting clusters in the form (`Class/Draw.cs`)
- Computes evaluation metrics (`FormRezultateMetrici.cs`, `Class/Evaluare.cs`, `Class/MetriciExterne.cs`) including confusion-matrix-based external metrics
- Distance matrix computation (`Class/Distante.cs`) and data normalization (`Class/Normalizare.cs`)
- Exports results to Excel via the **EPPlus** library (`Class/ExcelDoc.cs`)

## Sample Datasets (`Date de Analizat/`)

- `puncte_3 nori.txt` — 3 clusters
- `puncte_4 nori.txt` — 4 clusters
- `puncte_5 nori.txt` — 5 clusters
- `puncte_6 nori.txt` — 6 clusters
- `puncte_7 nori.txt` — 7 clusters
- `puncte_8 nori.txt` — 8 clusters

## Tech

C#, .NET Framework, Windows Forms, EPPlus 5.6.3 (Excel export)

## Build & Run

Open `Clusterring/AplicatieClusterring.sln` in Visual Studio (NuGet packages are already restored under `packages/`). Build and run.
