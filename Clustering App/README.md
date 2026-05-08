# Clustering App

A C# / WinForms desktop application for visualizing and benchmarking clustering algorithms on 2D point datasets.
Originally developed as part of my **Bachelor's thesis**: *Comparative study between different clustering algorithms* (final grade 9.60/10).

## Features

- Loads 2D point datasets from `.txt` files (sample datasets included with 3, 4, 5, 6, 7, 8 clusters)
- Runs clustering algorithms (e.g. K-Means) on the loaded points
- Visualizes the resulting clusters in the form
- Computes evaluation metrics for cluster quality (`FormRezultateMetrici.cs`)
- Exports results to Excel via the **EPPlus** library

## Sample Datasets

`Date de Analizat/`:
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
