## Project Aim

We aim to build a pipeline that detects individual bacterial cells in time-lapse microscopy images, tracks them across frames, and identifies when one cell divides into two. The pipeline will produce cell trajectories and lineage trees.

## Data

We will use time-lapse microscopy sequences with annotated cell masks and parent–daughter relationships. These annotations will serve as reference data for evaluating segmentation, tracking, and division detection.

## Planned Methods

1. **Segmentation.** Use a pretrained deep learning model to generate a separate mask for each bacterial cell in each frame.
2. **Tracking.** Match cells between consecutive frames based on the distance between their centers and how much their masks overlap.
3. **Division detection.** Apply rules to identify when one parent cell corresponds to two daughter cells, then record those links to reconstruct lineages.
4. **Learned tracking.** Once the baseline is in place, test whether a small neural network improves cell matching.

## Evaluation

We will run the tracker with annotated masks to measure tracking performance independently of segmentation errors, then repeat the evaluation with predicted masks to measure end-to-end performance. We will report segmentation accuracy and F1 scores for cell matches and division events.


## Citations:


Seiffarth, J., Blöbaum, L., Paul, R. D., Friederich, N., Sitcheu, A. J., Mikut, R., Scharr, H., Grünberger, A., & Nöh, K. (2025). Tracking one-in-a-million: Large-scale benchmark for microbial single-cell tracking with experiment-aware robustness metrics. Lecture Notes in Computer Science, 318–334. https://doi.org/10.1007/978-3-031-91721-9_20 

