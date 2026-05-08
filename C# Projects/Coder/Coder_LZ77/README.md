# LZ77 Coder

A C# WinForms application that implements **LZ77** — the classic sliding-window dictionary compression algorithm by Lempel & Ziv (1977).

## Algorithm

LZ77 compresses data by finding repeated sequences within a *sliding window* of recently seen input. Each match is encoded as a `(offset, length, next-character)` tuple. It is the foundation of `DEFLATE` (used by `gzip`, `zip`, `PNG`).

## Tech

C#, .NET, WinForms

## Run

Open `Coder_LZ77.sln` in Visual Studio and build/run.
