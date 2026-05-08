# C# Projects

Four academic projects built in C# (.NET / WinForms / Visual Studio).

---

## 1. Chat_C# — TCP Chat Application

A client/server chat application demonstrating socket programming in C#.

- **Server** (`Chat_C#/Server/`) — TCP listener that accepts multiple clients (`MyServer.cs`) and broadcasts messages between them.
- **Client** (`Chat_C#/Chat/`) — WinForms UI (`Form1.cs`) that connects to the server, sends and receives messages (`MyClient.cs`).

**Tech:** C#, .NET, `System.Net.Sockets`, WinForms

**Run:** open `Chat_C#/Server/Server.sln` and `Chat_C#/Chat/Chat.sln` in Visual Studio. Start the server first, then one or more client instances.

---

## 2. Coder — Compression Algorithms

Four separate Windows Forms applications, each implementing a classic data compression algorithm. Built for the *Coding & Information Theory* course.

| Sub-project | Algorithm | Notes |
|---|---|---|
| `Coder_LZ77` | LZ77 (sliding window) | Compress and decompress text/files |
| `LZW_Coder` | LZW (dictionary-based) | Used in GIF, TIFF compression |
| `Shannon_Fano_Coder` | Shannon-Fano coding | Variable-length prefix coding |
| `Predict_image_Coder` | Predictive image coding | Image compression via pixel prediction |

**Tech:** C#, WinForms

**Run:** open the `.sln` inside each sub-folder in Visual Studio.

---

## 3. MazeGameC# — Maze Game with Auto-Solver

A maze game where the player navigates through a labyrinth. Includes an automatic pathfinding solver.

- `Labirint.cs` — maze logic
- `LabirintData.cs` — map loading from `Matrice.txt`
- `Rezolvare.cs` — automatic solver
- `PunctLabirint.cs` — point/cell representation
- `Matrice.txt` — sample maze map

**Tech:** C#, WinForms, file-based map data

**Run:** open `MazeGameC#/LabirintJocuri.sln` in Visual Studio.

---

## 4. Real-Time System — Traffic Intersection 2.0

A real-time traffic intersection simulator built for the *Real-Time Systems* course. Uses Win32 API timers (`WinApiClass.cs`) to simulate concurrent traffic flows and traffic-light scheduling.

**Tech:** C#, WinForms, Win32 API (P/Invoke)

**Run:** open `Proiect_Real_Time_System_Intersection2.0/ProiectRTS2.0.sln` in Visual Studio.
