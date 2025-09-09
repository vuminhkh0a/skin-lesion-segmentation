# [Warm-up][AI VIETNAM] Kaggle Challenge: Binary Skin Lesion Segmentation

## Description
This is a private challenge of **AIMA Warm-up reasearch program**, created to support participants in exploring and practicing Medical AI.  
The task focuses on **dermatoscopic skin images (2D)** with the objective of building an model for **binary skin lesion segmentation**


## Goal
- Develop and train a model that segments lesions from dermatoscopic images  
- Evaluate segmentation performance using the **Dice score**


## Evaluation
- **Metric**: Dice Score 
- **Submission Rules**:
  - Each participant is allowed **7 submissions per day**
  - The evaluation process is divided into two phases:
    - **Public phase**: scores are displayed immediately after submission
    - **Private phase**: the final leaderboard is revealed after the challenge deadline
  - A maximum of **2 submissions** can be selected for the final private evaluation


## Dataset Description
The dataset includes dermatoscopic images with corresponding binary masks

- `Train/` → training images and their corresponding masks
- `Test/` → test images for submission  





## Submission Format
To meet file size constraints, **Run-Length Encoding (RLE)** is used to represent predicted masks:  
- Pixels are **1-indexed** and ordered **top-to-bottom, left-to-right**.  
- Example encodings:
  - `"1 3"` → pixels 1, 2, 3 belong to the mask.  
  - `"1 3 10 5"` → pixels 1, 2, 3, 10, 11, 12, 13, 14 belong to the mask.  
- All test images must be **resized to (512x512)** prior to prediction and submission.  
