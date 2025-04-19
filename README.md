# InterIIT-TechMeet-11.0

This present our end-to-end solution for the CloudPhysician: Vital Extraction Challenge, on of the Mid-Prep Problem Statements at the Inter IIT Tech Meet 11.0. The objective of this project was to extract critical patient vitals — Heart Rate, SPO2, RR, SBP, DBP, and MAP — from ICU monitor images using computer vision and OCR techniques.

## Problem Overview

The challenge was broken down into the following major tasks:
- Monitor Screen Localization
- Feature (Vitals) Extraction
- Text Recognition & Graph Digitization

## Data 

We worked with the following datasets as a part of this challenge:

- Monitor Dataset (2000 labeled images): Used for training Model M1 to detect and crop monitor screens using bounding boxes. Each image included labels for the screen coordinates.
- Classification Dataset (4 folders × 250 images each, with feature coordinates): Used for training Model M2 for detecting features - the vitals. Each folder corresponds to a different vital type and includes bounding box annotations. Text values and graph signals are extracted from the cropped regions.
- Unlabelled Dataset (7000 raw monitor images without annotations): Contains only raw images (without any bounding box labels for screens or features). Used for inference using the pipeline trained on the labeled datasets.

## Pipeline

![image](https://github.com/user-attachments/assets/61f77d0e-6c15-4430-909a-fb9cf351561e)

## Results Summary

| **Component**         | **Metric**       | **Value**                       |
|-----------------------|------------------|----------------------------------|
| Monitor Detection     | F1 Score         | ≈ 1.00 with confidence 0.912       |
| Feature Extraction    | F1 Score         | ≈ 0.93 with confidence 0.702       |
| Inference Speed       | Time per image   | ~3.5 seconds                    |


