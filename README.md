# Generalized Hough Transform Object Detection

This project demonstrates how the **Generalized Hough Transform (GHT)** algorithm detects specific objects in an image. GHT can identify complex shapes, even if they appear multiple times, by analyzing edges to estimate the object's location and orientation.

## Table of Contents

- [About](#about)
- [How it works](#how-it-works)
- [Dataset](#dataset)
- [Results](#results)
- [Installation](#installation)

## About

The **Generalized Hough Transform** is an extension of the classical Hough Transform that can detect arbitrary shapes that are hard to explain using mathematical equations (unlike straight lines and circles). It works by transforming edge points to a parameter space and finding consistent offsets that match the template.

This repository implements a Python-based demonstration of GHT via edge detection and template matching.

## How it works

1. **Edge Detection**
   Use edge detection to extract the boundaries of shapes in the input image.
2. **Tempalte Representation**
   Convert a template image of the objectto be detected into its edge form.
3. **Accumulator Voting**
   For each edge point in the image, use the template's reference model (known as the R-table) to vote in parameter space.
4. **Peak Detection**
   Peaks in the accumulator correspond to potential object locations in the image.

This method allows detection objects even if they are translated, rotated, or scaled relative to the template.

## Dataset

The repository includes example datasets such as
- dataset_daisy: images of a daisy template
- dataset_fish: images of a fish template

## Results
<img width="1273" height="609" alt="image" src="https://github.com/user-attachments/assets/7a1c7202-aec3-41f4-b312-e2402c21590d" />

<img width="1258" height="597" alt="image" src="https://github.com/user-attachments/assets/8616f151-24ed-48f2-8716-84aee3bf13c8" />

## Installation
```bash
   git clone https://github.com/meddyahya/Generalized-Hough-Transform-Object-Detection.git
   cd Generalized-Hough-Transform-Object-Detection
   pip install -r requirements.txt
```
