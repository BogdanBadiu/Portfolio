# Image Processing — Game Piece Detection (MATLAB)

A MATLAB project that automatically detects red and blue game pieces on a **"Mill" (Moara)** board from a photograph. Built for the *Image Processing* course at "Lucian Blaga" University of Sibiu.

## Pipeline

The script `Proiect_Final.m` performs:

1. **Image loading** — reads the input image and normalizes pixel values to `[0, 1]`
2. **Grayscale conversion** — weighted RGB → gray (`0.3R + 0.6G + 0.1B`)
3. **Smoothing** — applies a 3×3 averaging filter to remove fine details
4. **K-Means segmentation** — iterative two-class clustering to separate pieces from the board
5. **Piece classification** — separates red vs blue pieces by color analysis on the segmented regions
6. **Detection output** — annotates and visualizes the detected pieces

## Test Images

- `T5.png`, `T6.jpg` — main test boards (the "Mill" board)
- `ImagineTest1.png`, `ImagineTest2.png`, `ImagineTest3.png` — additional test cases

## Documentation

- `Documentation Part Detection (English).pptx` — full project documentation in English
- `Documentatie Detectare de piese.pptx` — Romanian version

## Tech

MATLAB (Image Processing Toolbox), K-Means clustering

## Run

Open `Proiect_Final.m` in MATLAB and run. Switch the input by changing the `numePoza` variable near the top of the file.
