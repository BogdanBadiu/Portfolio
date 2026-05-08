# Shannon-Fano Coder

A C# WinForms application that implements **Shannon-Fano coding** — a variable-length prefix code based on symbol probabilities.

## Algorithm

Shannon-Fano sorts symbols by frequency and recursively splits them into two groups of (approximately) equal probability, assigning `0` to one group and `1` to the other. The result is a prefix-free binary code where more frequent symbols get shorter codes. It is the historical predecessor of Huffman coding (which is generally optimal where Shannon-Fano is not).

## Tech

C#, .NET, WinForms

## Run

Open `Coder.sln` in Visual Studio and build/run.
