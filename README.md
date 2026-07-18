# Thesis Report — Object Classification, Detection and State Estimation using YOLO-v3 and Sensor Fusion of Stereo Camera and LiDAR

LaTeX source for the Master's thesis of **Kamalkumar Mehta** (Aerospace System Laboratory, Department of Mechanical and Aerospace Engineering, The University of Texas at Arlington). Defended June 1, 2021; graduation August 2021. Committee: Dr. Kamesh Subbarao (supervisor), Dr. Alan Bowling, Dr. Animesh Chakravarthy.

## About the Thesis

This research implements a real-time object detection and tracking pipeline for collision avoidance on an autonomous ground vehicle:

- **Object detection** — transfer learning on a pre-trained YOLO-v3 deep neural network, trained on a custom labeled dataset of four 3D shapes (cylinder, cone, pyramid, rectangular parallelepiped).
- **Hyper-parameter tuning** — mini-batch size, L2 regularization, epochs, and learning rate tuned to study the bias/variance trade-off.
- **Sensor calibration** — intrinsic calibration of the stereo camera (Sony IMX 179) and LiDAR (Intel RealSense L515), plus extrinsic calibration between the two sensors.
- **Sensor fusion & state estimation** — a centralized fusion framework using a linear Kalman filter to estimate object states.

The framework was developed in MATLAB 2020b (Deep Learning, Computer Vision, Image Processing, LiDAR, and Sensor Fusion & Tracking toolboxes) and validated both in the MATLAB Driving Scenario Designer and on an experimental platform with an Intel NUC onboard computer.

## Repository Structure

| File | Description |
|---|---|
| `Main.tex` | Root document — compile this file. Assembles front matter, chapters, bibliography, and biography. |
| `Abstract.tex` | Thesis abstract. |
| `Acknowledge.tex` | Acknowledgements page. |
| `Chapter-Introduction.tex` | Motivation, background, and contributions. |
| `Chapter-Optical-Sensors-and-Object-Detection-Fundamentals.tex` | Camera/LiDAR fundamentals and object detection background. |
| `Chapter-The-Artificial-Neural-Network.tex` | ANN and CNN theory, YOLO-v3 architecture. |
| `Chapter-Supervised-Learning.tex` | Supervised learning, dataset creation, and training. |
| `Chapter-Hyper-parameters-Tuning.tex` | Hyper-parameter tuning experiments. |
| `Chapter-Sensor_Fusion.tex` | Calibration and Kalman-filter-based sensor fusion framework. |
| `Chapter-Results-discussion-and-future-scope.tex` | Simulation/experimental results, discussion, and future work. |
| `Biography.tex` | Author biography. |
| `appA.tex` | Appendix A (currently unused, commented out in `Main.tex`). |
| `references.bib` | BibTeX bibliography (IEEEtran style). |
| `utamsASL.sty`, `utaComp.sty`, `psfig.sty` | UTA thesis style files (formatting required by the UTA Graduate School). |
| `Images/` | All figures: architecture diagrams, calibration figures, training/testing plots, and experimental result plots (PNG/PDF). |

## Building

Requires a LaTeX distribution (e.g., MiKTeX or TeX Live). From this directory:

```
pdflatex Main.tex
bibtex Main
pdflatex Main.tex
pdflatex Main.tex
```

The output is `Main.pdf`, formatted per UTA Graduate School requirements.

## Related Projects

- `../Thesis_presentation` — full defense slide deck (Beamer).
- `../Thesis-presentation-Updated` — condensed version of the defense deck.
