# Maze Game (C#)

A maze game in C# WinForms with manual play and an automatic pathfinding solver.

## Features

- Loads a labyrinth map from `Matrice.txt` (a textual matrix where each cell is wall, free, start or finish)
- Manual play — user navigates through the maze
- **Automatic solver** — finds and animates a path from start to finish (`Rezolvare.cs`)

## Code Structure

| File | Purpose |
|---|---|
| `Labirint.cs` | Maze data structure |
| `LabirintData.cs` | Loads the maze from `Matrice.txt` |
| `PunctLabirint.cs` | Cell / point representation |
| `Rezolvare.cs` | Automatic solver (pathfinding) |
| `Form1.cs` | WinForms UI and game loop |

## Tech

C#, .NET Framework, Windows Forms

## Run

Open `LabirintJocuri.sln` in Visual Studio and run. The maze is loaded from `Matrice.txt` — edit that file to test custom layouts.
