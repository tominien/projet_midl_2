# Piano Hand Pose & Key Press Prediction (MMPose)

Piano hand pose estimation and pressed-key prediction from video using MMPose (OpenMMLab).  
Academic project for the Math & CS double degree (University of Toulouse).

---

## General Overview

This project takes as input a **top-down video of a piano** and:
1. Detects the **2D hand keypoints** (wrist + fingers) with MMPose hand models.
2. Calibrates the **piano geometry** in image space (location of white/black keys).
3. Detects **key press events** per finger over time (temporal analysis of fingertip motion).
4. Maps each detected press to a **musical key name** (e.g. `G4`, `C5`, `F#5`).
5. Exports the detected notes as a structured **Python list / CSV** to be reused or visualised.

The core of the project lives in the main notebook: - `Projet MIDL 2 - Tom LE BER (22308482) & Tony PEROTTINO (22303877).ipynb`

The code is designed to run mainly in **Google Colab**, with a reproducible CPU-only setup for MMPose.

---

## Execution tutorial (Google Colab)
1. Open the notebook in Google Colab.
2. Run the **environment setup cells** (installation + clone of MMPose).
3. Upload a **top-down piano video** (single hand is recommended).
4. Configure the **piano geometry** for your video.
5. Choose:
   - Which MMPose model to use (among `MODELS_CONFIG`),
   - Which finger(s) to track (among `["Pouce", "Index", "Majeur", "Annulaire", "Auriculaire"]`).
6. Run section V.2 to extract keypoints, detect key presses and print the detected sequence of notes.
