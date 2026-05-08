# Predictive Image Coder

A C# WinForms application that implements **predictive image coding** — a lossless image-compression technique. The most feature-rich of the four compression coders in this portfolio: it lets you experiment with **9 different predictors** and inspect the prediction error visually.

## Algorithm

For each pixel, a predictor estimates its value from already-encoded neighboring pixels. Only the **residual** (difference between the actual and predicted value) is encoded. Because residuals tend to be small and clustered around zero, they compress well. This technique sits at the core of **JPEG-LS**, **PNG** filters, and **lossless JPEG**.

The neighborhood used for prediction is the standard three-pixel context:

```
C  B
A  X    ← X is the pixel being predicted, from A, B, C
```

## What the app does

**Image input:**
- *Load Image* — load any image file
- *Choose Image and Scale* — image source and display scale

**Predictor choices** (radio buttons — pick one):
- `128` — constant predictor (baseline)
- `A`, `B`, `C` — single-neighbor predictors
- `A+B-C` — planar predictor
- `A+(B-C)/2` — gradient-adjusted A
- `B+(A-C)/2` — gradient-adjusted B
- `(A+B)/2` — average of A and B
- `jpegLS` — the **MED (Median Edge Detector)** predictor used in **JPEG-LS**

**Coder workflow:**
- *Predict* — run the chosen predictor and produce the error matrix
- *Show error matrix* — visualize the residuals as a grayscale image
- *Show histogram* — plot the distribution of prediction errors
- *Save encoded* — save the encoded output to disk

**Decoder workflow:**
- *Load encoded* — load a previously encoded file
- *Decode* — reconstruct the image from the residuals
- *Save decode* — save the decoded image

**Visualization toggles** (radio buttons):
- *Original* / *Error prediction* / *Decoded* — switch between viewing the source image, the prediction errors, or the reconstructed image

## Tech

C#, .NET Framework, WinForms, Visual Studio

## Run

Open `AlgPredictiv.sln` in Visual Studio and build/run.

## Course

Built for the *Coding & Information Theory* course at "Lucian Blaga" University of Sibiu.
