# 🖼️ **DFT-Based Image Watermarking**

This project demonstrates **watermark embedding in grayscale images using the Discrete Fourier Transform (DFT) domain**. The notebook implements both a **manual DFT/IDFT** and the **built-in OpenCV DFT/IDFT** functions to compare performance and image quality after watermarking.

---

## 🚀 **Project Overview**

Watermarking is a key technique for **digital image copyright protection**. This project explores embedding a **visible watermark in the frequency domain using DFT** to minimize visible distortion and improve robustness.

Two approaches are implemented:

1. **Manual DFT/IDFT**: Directly implementing 2D DFT and inverse DFT using nested loops.
2. **Built-in OpenCV DFT/IDFT**: Using OpenCV's optimized functions for frequency transforms.

---

## 🧠 **Features**

- **Custom implementation of 2D DFT and IDFT.**
- **Watermark embedding in the frequency magnitude.**
- **Comparison of manual and built-in methods in terms of:**
  - **Visual quality (PSNR, SSIM, RMSE)**
  - **Execution time**
- **Visualization of frequency domain magnitude before and after watermark embedding.**
- **Difference images to highlight watermark impact.**

---

## 🔍 **Methodology**

1. **Load and resize** the input image to 64x64 grayscale.
2. Compute the **2D DFT manually and using OpenCV**.
3. Create a **text watermark pattern**.
4. Embed the **watermark in the magnitude spectrum** with a scaling factor (alpha).
5. Compute the **inverse DFT to reconstruct the watermarked image**.
6. Evaluate and compare results using **quantitative metrics and visualizations**.
7. Measure **execution time** for both manual and built-in DFT/IDFT implementations.

---

## 🛠 **Installation**

Make sure you have the required Python packages installed:

```bash
pip install opencv-python numpy pandas matplotlib scikit-image
```

---

## 📌 Usage

1. Clone this repository or download the notebook `dft-watermarking.ipynb`.
2. Place a grayscale image named `professional.jpg` in the working directory.
3. Open the notebook and **run all cells sequentially**.
4. The notebook outputs:
    - **Original and watermarked images.**
    - **DFT magnitude visualizations.**
    - **Quality metrics and performance timing.**
    - Saved images `watermarked_manual.jpg` and `watermarked_builtin.jpg`.

---

## 🎯 Results

- Both manual and built-in methods successfully embed the watermark with **minimal perceptual distortion**.
- **PSNR and SSIM values indicate high similarity** between original and watermarked images.
- The built-in OpenCV functions are **significantly faster** than the manual implementation.
- Visualizations show how watermarking affects the **frequency magnitude spectrum**.

---

## 📊 Performance

| **Metric**                | **Built-in DFT/IDFT** | **Manual DFT/IDFT** |
|-----------------------|-------------------|-----------------|
| **Execution Time (DFT)**   | 0.000909 seconds     | 36.764212 seconds        |
| **Execution Time (IDFT)**  | 0.0 seconds     | 37.983244 seconds        |
| **PSNR**                  | High (26.173881 dB)     | High (26.173678 dB)   |
| **SSIM**                | 0.9918             | 0.991801           |
| **RMSE**                | Low (10.027465)    | Low (10.02783)     |

*(Note: Exact times depend on your hardware)*

---

## ✔ **Conclusion**

This project highlights the trade-offs between **clarity and computational efficiency**:

- The manual implementation offers a **clear understanding of DFT mechanics** but is **computationally expensive**.
- The built-in OpenCV functions provide a **practical solution with optimized speed** and **comparable image quality**.

**Watermark embedding in the frequency domain is effective for preserving image fidelity while adding copyright marks**.

---

## 💡 **Future Work**

- **Optimize the manual DFT implementation** using vectorized or parallel processing.
- **Test watermark robustness against attacks** like noise, compression, or cropping.
- Extend watermarking to **color images and adaptive watermark placement**.
- Implement **watermark extraction and verification**.
- Experiment with **different watermark patterns and embedding strengths**.

---

**Developed by [Dipanshu Modi](https://github.com/dipanshumodi31)**
