# LZ77 Coder

A C# WinForms application that implements **LZ77** — the classic sliding-window dictionary compression algorithm by Lempel & Ziv (1977).

## Algorithm

LZ77 compresses data by finding repeated sequences within a *sliding window* of recently seen input. Each match is emitted as a `(offset, length, next-symbol)` token. It is the foundation of `DEFLATE` (used by `gzip`, `zip`, `PNG`).

## What the app does

The form is split into two halves — **Coder** (left) and **Decoder** (right).

**Coder side:**
- *Load file* — pick any text/binary file as input
- *Choose the number of bits for the offset* — controls the window size (`2^bits`)
- *Choose the number of bits for the length* — controls maximum match length
- *Encode file* — runs LZ77 and emits a stream of tokens
- *Show Tokens* — opens a data grid displaying every emitted token: `Position | Length | Symbol`

**Decoder side:**
- *Load encoded file* — load a previously encoded file
- *Decode file* — reconstructs the original from the token stream

## Tech

C#, .NET Framework, WinForms, Visual Studio

## Run

Open `Coder_LZ77.sln` in Visual Studio and build/run.

## Course

Built for the *Coding & Information Theory* course at "Lucian Blaga" University of Sibiu.
