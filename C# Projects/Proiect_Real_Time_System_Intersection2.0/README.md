# Real-Time System — Traffic Intersection 2.0

A real-time traffic-intersection simulator built for the *Real-Time Systems* course at "Lucian Blaga" University of Sibiu.

## What it does

Simulates a four-way road intersection with traffic lights and concurrent traffic flows. Uses **Win32 API timers** (via P/Invoke) for time-deterministic scheduling of traffic-light phases and vehicle movement.

## Code Structure

| File | Purpose |
|---|---|
| `Form1.cs` | Main UI, intersection rendering, simulation loop |
| `WinApiClass.cs` | P/Invoke wrapper around Win32 timer API |
| `Program.cs` | Entry point |

## Tech

C#, .NET Framework 4.7.2, Windows Forms, Win32 API (P/Invoke)

## Run

Open `ProiectRTS2.0.sln` in Visual Studio (Windows only — depends on Win32 API) and run.
