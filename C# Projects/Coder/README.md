# Coder — Compression Algorithms

Four standalone WinForms applications, each implementing a classic data-compression algorithm. Built for the *Coding & Information Theory* course at "Lucian Blaga" University of Sibiu.

## Sub-projects

| Folder | Algorithm | Use case |
|---|---|---|
| [`Coder_LZ77/`](./Coder_LZ77/) | **LZ77** — sliding-window dictionary compression | Foundation for `gzip`, `zip`, `PNG` |
| [`LZW_Coder/`](./LZW_Coder/) | **LZW** — Lempel-Ziv-Welch dictionary coding | Used in GIF, TIFF, Unix `compress` |
| [`Shannon_Fano_Coder/`](./Shannon_Fano_Coder/) | **Shannon-Fano** — variable-length prefix coding | Predecessor of Huffman coding |
| [`Predict_image_Coder/`](./Predict_image_Coder/) | **Predictive image coding** — pixel prediction + residual encoding | Lossless image compression |

## Tech

C#, .NET Framework, WinForms, Visual Studio

## Run

Each sub-folder has its own `.sln` — open it in Visual Studio and run.
