# Client/Server Chess — C++ Builder

A network multiplayer chess game built with **Embarcadero C++ Builder** (Borland VCL). Two players connect over TCP and play against each other through synchronized client instances coordinated by a server.

## Components

- **`ProiectDeSah _Server/`** — Server application
  Manages connections between two clients, relays moves and game state.

- **`ProiectDeSah _Client/`** — Client application
  Full chess UI with board rendering and piece movement validation.

  Key files:
  - `Tabla.cpp` / `Tabla.h` — board representation and rendering
  - `Piese.cpp` / `Piese.h` — chess piece logic and movement rules
  - `Joc.cpp` / `Joc.h` — game state and turn management
  - `Init_Pozitie.cpp` — initial board setup
  - `JocDeSah.cpp` — main game loop
  - `USah.dfm` — VCL form definition (chess UI)

- **`Resurse/`** — chess piece images and icons (`ChessIco.ico`)

## Tech

C++, C++ Builder (Borland VCL), TCP sockets

## Build & Run

Open `.cbproj` files in **Embarcadero C++ Builder**. Start the server, then launch two client instances and connect them to the server.
