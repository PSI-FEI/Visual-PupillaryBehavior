# Visual-PupillaryBehavior

This script processes eye-tracking data (tobii pro studio files) to analyze pupil responses and gaze behavior in response to neonatal pain face stimuli.

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

## Project Structure

| File                        |                                                         Description                                                         |
|-----------------------------|:---------------------------------------------------------------------------------------------------------------------------:|
| 1_processing_raw_data.ipynb | It extracts features such as fixation/saccade counts, pupil dilation, and explore-exploit ratios across two time intervals. |
| 2_mapping.ipynb             | It performs visualization of gaze-based behavioral metrics on facial areas of interest.                                     |
| 3_face.png                  | An image for the background of facial maps.                                                                                 |
| 3_face_All_AOIs.txt         | AOIs boundaries for facial maps.                                                                                            |
| 4_aoi_data.csv              | Sample data generated from processing raw.                                                                                  |

## Usage

This script assumes that the raw `.tsv` files have already been processed and are stored in:
> experiments/neonatal_pain_faces/db_processed/

See  Step 1: Merge AOI columns in https://github.com/PSI-FEI/eye-tracking

Run 1_processing_raw_data.ipynb to process metrics and 2_mapping.ipynb to get facial mapping results.


