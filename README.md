# [Warm-up][AI VIETNAM] Kaggle challenge: Binary Skin Lesion Segmentation

## 📝 Description
This is the first challenge in the **Medical AI Challenge Series**, designed to help participants get started with Medical AI.  
The task is to work with **dermatoscopic skin images (2D)** and build an automated system for **binary skin lesion segmentation**.

---

## 🎯 Goal
- Train a model to segment lesions from dermatoscopic images.  
- Evaluate the segmentation performance using the **Dice score**.

---

## 📊 Evaluation
- **Metric**: Dice Score (popular in medical image segmentation).  
- **Submission Rules**:
  - You can make **7 submissions per day**.  
  - The evaluation consists of two phases:
    - **Public phase**: score shown immediately after submission.  
    - **Private phase**: final leaderboard revealed after the challenge deadline.  
  - You can choose **up to 2 submissions** for the final private evaluation.  

---

## 📦 Dataset Description
The dataset consists of dermatoscopic images with corresponding binary masks.

- **Files**:
  - `Train/` → contains training images and their corresponding masks.  
  - `Test/` → contains test images for evaluation.  
  - `sample_submission.csv` → example submission file in the required format.  

- **Columns**:
  - `ID` → image ID.  
  - `Predicted_Mask` → predicted segmentation mask (RLE encoded).  

---

## 📐 Submission Format
Due to file size limits, **Run-Length Encoding (RLE)** is used for the predicted masks:  
- Pixels are **1-indexed** and counted **top-to-bottom, left-to-right**.  
- Example:
  - `"1 3"` → pixels 1, 2, 3 are part of the mask.  
  - `"1 3 10 5"` → pixels 1, 2, 3, 10, 11, 12, 13, 14 are part of the mask.  
- All test images must be **resized to (512x512)** before prediction and submission.  
