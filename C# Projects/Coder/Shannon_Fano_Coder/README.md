# Shannon-Fano Coder

A C# WinForms application that implements **Shannon-Fano coding** — a variable-length prefix code based on symbol probabilities.

## Algorithm

Shannon-Fano sorts symbols by frequency and recursively splits them into two groups of (approximately) equal probability, assigning `0` to one group and `1` to the other. The result is a prefix-free binary code where more frequent symbols get shorter codes. It is the historical predecessor of Huffman coding (which is generally optimal where Shannon-Fano is not).

## What the app does

The form is split into two halves — **Coder** (left) and **Decoder** (right).

**Coder side:**
- *Load File* — encode an entire file
- *Encode input text* — encode text typed directly in the form (useful for short demos)
- *Encode Info* — displays the computed code table (symbol → code) and statistics
- *Show Codes* — opens a view of all generated prefix codes

**Decoder side:**
- *Load encoded file* — load a previously encoded file
- *Decode file* — reconstructs the original from the encoded stream and the code table

## Tech

C#, .NET Framework, WinForms, Visual Studio

## Run

Open `Coder.sln` in Visual Studio and build/run.

## Course

Built for the *Coding & Information Theory* course at "Lucian Blaga" University of Sibiu.
