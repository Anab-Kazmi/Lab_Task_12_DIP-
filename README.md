# **Task 12: Image Segmentation Techniques**

**Roll Number:** 2023-SE-06

---

### **Prompt**

*"Perform a comprehensive segmentation analysis on a color image by:*

* Uploading a color image and converting it to grayscale.
* Applying global thresholding with a fixed threshold value.
* Applying Otsu’s thresholding for automatic global threshold selection.
* Applying adaptive thresholding using Gaussian weighting.
* Performing K-Means color segmentation for k = 2, 3, 4 clusters.
* Applying Mean Shift filtering for image segmentation.
* Displaying the original image alongside all segmentation results in a grid for visual comparison.
* Analyzing and discussing the strengths and limitations of each segmentation technique in terms of accuracy, noise sensitivity, and visual quality."*

---

## **Objective**

The objective of this task is to explore **various image segmentation techniques** for both grayscale and color images, including:

* **Thresholding methods:** global, Otsu, adaptive
* **Clustering:** K-Means segmentation
* **Edge-preserving filtering:** Mean Shift segmentation

Segmentation separates an image into meaningful regions for analysis, highlighting objects and structures.

---

## **Methodology / Approach**

1. **Upload Image:** User uploads a color image in Google Colab.
2. **Grayscale Conversion:** Convert color image to grayscale for thresholding.
3. **Thresholding:**

   * **Global Thresholding:** Fixed threshold for uniform illumination.
   * **Otsu Thresholding:** Automatic threshold based on bimodal histogram.
   * **Adaptive Thresholding:** Gaussian-weighted local thresholding for non-uniform lighting.
4. **K-Means Segmentation:** Color-based clustering for **k = 2, 3, 4** clusters.
5. **Mean Shift Segmentation:** Edge-preserving smoothing and clustering in color space.
6. **Visualization:** Display all segmentation results alongside the original image in a 3×3 grid.
7. **Analysis:** Discuss strengths and limitations of each method.

---

## **Results / Observations**

* **Global Thresholding:**

  * Works well with images having uniform lighting.
  * Sensitive to illumination changes; may fail on unevenly lit areas.

* **Otsu Thresholding:**

  * Automatically selects optimal threshold for bimodal histograms.
  * Less effective for multimodal or complex lighting patterns.

* **Adaptive Thresholding:**

  * Handles non-uniform lighting effectively.
  * Computationally more intensive; block size must be chosen carefully.

* **K-Means Segmentation:**

  * Groups similar colors together; works best on color images.
  * Increasing **k** creates more clusters but may over-segment simple regions.

* **Mean Shift Segmentation:**

  * Preserves edges and smooth regions, produces visually appealing clusters.
  * Slower for large images; requires careful tuning of spatial (`sp`) and color (`sr`) bandwidth.

**Conclusion:** Combining thresholding with clustering and edge-preserving filtering provides flexible segmentation options depending on image characteristics and application requirements.

---

## **Tools and Libraries Used**

* **Python 3.x**
* **OpenCV (cv2):** Image reading, thresholding, K-Means, Mean Shift
* **NumPy (np):** Array manipulation and reshaping
* **Matplotlib (plt):** Visualization in a 3×3 grid
* **Google Colab:** Safe image upload and execution environment

---
