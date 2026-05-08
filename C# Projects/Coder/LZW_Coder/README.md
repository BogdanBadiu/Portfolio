# LZW Coder

A C# WinForms application that implements **LZW** (Lempel-Ziv-Welch) — a dictionary-based lossless compression algorithm.

## Algorithm

LZW builds a dictionary of substrings as it scans the input. Encoder and decoder build the dictionary identically from the input stream, so it does not need to be transmitted. Famously used in **GIF**, **TIFF**, and the Unix `compress` command.

## What the app does

The form is split into two halves — **Coder** (left) and **Decoder** (right).

**Coder side:**
- *Load file* — pick the file to compress
- *Choose the number of bits for INDEX* — sets the maximum dictionary size (`2^bits`)
- **Dictionary-full strategy** (radio buttons):
  - *Freeze* — stop adding new entries when the dictionary is full
  - *Empty* — clear the dictionary and start fresh
- *Encode file* — runs LZW
- *Show emitted Indexes* — displays the index stream produced by the encoder

**Decoder side:**
- *Load encoded file* — load a previously encoded file
- *Decode file* — reconstructs the original

## Tech

C#, .NET Framework, WinForms, Visual Studio

## Run

Open `LZW.sln` in Visual Studio and build/run.

## Course

Built for the *Coding & Information Theory* course at "Lucian Blaga" University of Sibiu.
