# Perception_mea4 — Color & Circle Detection with OpenCV

Computer-vision practical work (Polytech Montpellier, MEA — 4th year): detecting a colored ball
in images and video with **OpenCV**. The write-up is in `CR_perception.pdf`.

## What it does

Two small pipelines around the same idea (isolate a color, then find the circle):

1. **Still image** — convert to HSV, pick a reference color (by click), threshold with `inRange`,
   clean the mask with morphological operations (erode/dilate), then detect the ball with the
   **Hough circle transform** (`cv.HoughCircles`).
2. **Video sequence** — same pipeline applied frame by frame, with an initial scan that
   **auto-detects the ball's reference color** on the first frame, for real-time tracking.

## Contents

- `CR_perception.pdf` — report (method, code excerpts, result figures).
- `TP_perception/`, `TP_perception_video/` — the two scripts and their assets.

## Tech

Python, OpenCV, NumPy (HSV thresholding, morphological filtering, Hough circle transform).
