# Chat_C# — TCP Chat Application

Client/server chat in C# demonstrating socket programming with `System.Net.Sockets`.

## Components

- **`Server/`** — TCP listener (`MyServer.cs`) that accepts multiple clients and broadcasts messages between them.
- **`Chat/`** — WinForms client (`Form1.cs` + `MyClient.cs`) that connects to the server, sends and receives messages.

## Tech

C#, .NET, WinForms, `System.Net.Sockets`

## Run

1. Open `Server/Server.sln` in Visual Studio and start the server.
2. Open `Chat/Chat.sln`, run multiple instances of the client.
3. Connect each client to the server's IP and port.

## Course

Built for the *Distributed Systems / Networking* coursework at "Lucian Blaga" University of Sibiu.
