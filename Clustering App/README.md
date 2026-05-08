# Clustering App

A C# / WinForms desktop application for benchmarking and visualizing clustering algorithms on **two kinds of data**:

1. **Synthetic 2D point datasets** — for visualization and intuitive demos (3 to 8 cluster shapes).
2. **High-dimensional sparse text data** — the **Reuters multi-class benchmark** in ARFF-like format (sparse `index:value` records with `@attribute`, `@topic`, `@data` headers and per-document topic labels such as `c22`, `c31`, `c151`, `gcat`, `gcrim` ...). Tested at **100** and **1309** features, split 80/20 (Pareto) into training and test sets.

Originally developed as part of my **Bachelor's thesis**: *Comparative study between different clustering algorithms* (final grade 9.60/10).

## Algorithms Implemented

- **DBSCAN** (`Class/DBSCAN.cs`) — density-based clustering with `eps` (neighborhood radius) and `minPoints` parameters. Identifies arbitrary-shaped clusters and marks outliers as noise (`ClusterId = -1`).
- **Hierarchical Agglomerative Clustering (HAC)** (`Class/HAC.cs`) — bottom-up clustering with two linkage strategies:
  - **Single-link** (minimum distance between clusters)
  - **Complete-link** (maximum distance between clusters)

## Distance Metrics (`Class/Distante.cs`)

- **Euclidean**
- **Manhattan**
- **Cosine** — important for sparse text vectors where Euclidean/Manhattan are dominated by document length

## Normalization Strategies (`Class/Normalizare.cs`)

- **Nominal**
- **Cornell** (smart text-IR style)
- **Sum = 1** (probability-mass)
- **Min-Max**
- **Binary** (presence/absence)

This is the dimension that matters most for text data: results vary significantly depending on which normalization is paired with which distance metric.

## File Format Support (`Class/ReadFile.cs`)

- `Read2DFile` &mdash; comma-separated 2D points with cluster label (used for the `puncte_*.txt` demo files)
- `ReadNDFile` &mdash; ARFF-like sparse N-dimensional format with `@attribute` declarations, `@topic` labels, and `# topic` cluster suffix per data line. Handles the Reuters-style files such as `MultiClass_Training_SVM_100.0.arff` and `MultiClass_Training_SVM_1309.0.arff` (with corresponding `MultiClass_Test_SVM_*.arff` for evaluation).

## Features

- Loads either 2D point datasets or N-dimensional sparse ARFF datasets
- Runs DBSCAN or HAC (single- or complete-link) with chosen distance + normalization
- Visualizes 2D results in the form (`Class/Draw.cs`)
- Computes evaluation metrics (`FormRezultateMetrici.cs`, `Class/Evaluare.cs`, `Class/MetriciExterne.cs`) including confusion-matrix-based external metrics
- Distance matrix computation (`Class/Distante.cs`) and data normalization (`Class/Normalizare.cs`)
- Exports results to Excel via the **EPPlus** library (`Class/ExcelDoc.cs`) &mdash; the `FisiereExcelRaport/` folder contains generated reports for every algorithm + metric + normalization combination on the Reuters 1309-feature dataset

## Sample 2D Datasets (`Date de Analizat/`)

- `puncte_3 nori.txt` &mdash; 3 clusters
- `puncte_4 nori.txt` &mdash; 4 clusters
- `puncte_5 nori.txt` &mdash; 5 clusters
- `puncte_6 nori.txt` &mdash; 6 clusters
- `puncte_7 nori.txt` &mdash; 7 clusters
- `puncte_8 nori.txt` &mdash; 8 clusters

## Tech

C#, .NET Framework, Windows Forms, EPPlus 5.6.3 (Excel export)

## Build & Run

Open `Clusterring/AplicatieClusterring.sln` in Visual Studio (NuGet packages are already restored under `packages/`). Build and run.
