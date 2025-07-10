# Visual-PupillaryBehavior

This script processes eye-tracking data (tobii pro studio files) to analyze pupil responses and gaze behavior in response to neonatal pain face stimuli. It extracts features such as fixation/saccade counts, pupil dilation, and explore-exploit ratios across two time intervals.

## Purpose

Processes gaze and pupil data from Tobii eye-tracking devices to extract visual attention features and visualize differences between participant groups (e.g., experts vs. non-experts).

## Key Features

- Applies low-pass filtering to pupil data
- Extracts gaze-based features per stimulus:
  - Fixation/saccade counts and durations
  - Relative pupillary response (RPR)
  - Explore/Exploit ratio (EER) 
- Compares metrics across two time windows:
  - 0–2 seconds (early response)
  - 2–7 seconds (late response)
- Visualizes results using `seaborn`

## Usage

This script assumes that the raw `.tsv` files have already been processed and are stored in:
> experiments/neonatal_pain_faces/db_processed/
