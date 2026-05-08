# LZW Coder

A C# WinForms application that implements **LZW** (Lempel-Ziv-Welch) compression — a dictionary-based lossless algorithm.

## Algorithm

LZW builds a dictionary of substrings as it scans the input. It does not transmit the dictionary itself: encoder and decoder build it identically from the input stream. Famously used in **GIF**, **TIFF**, and the Unix `compress` command.

## Tech

C#, .NET, WinForms

## Run

Open `LZW.sln` in Visual Studio and build/run.
