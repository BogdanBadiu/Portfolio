# Predictive Image Coder

A C# WinForms application that implements **predictive image coding** — a lossless image-compression technique.

## Algorithm

For each pixel, a predictor estimates its value from already-encoded neighboring pixels (e.g. left, top, top-left). Only the **residual** (difference between actual and predicted value) is encoded. Because residuals tend to be small and clustered around zero, they compress well. This technique is at the core of **JPEG-LS**, **PNG** filters, and **lossless JPEG**.

## Tech

C#, .NET, WinForms

## Run

Open `AlgPredictiv.sln` in Visual Studio and build/run.
