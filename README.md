# Automated-Digitization-and-Signal-Separation-in-Overlapping-ECG-Papers-using-Deep-Learning

Hi, I'm Jauza Zahra Ulaya, a Bachelor of Informatics graduate with an interest in Artificial Intelligence, Machine Learning, and Software Development. This repository contains my undergraduate thesis project, titled **"Automated Digitization and Signal Separation in Overlapping ECG Papers using Deep Learning."** The project explores the application of deep learning to automatically digitize 12-lead ECG signals and separate overlapping signals for better analysis.

I developed this project using **YOLOv12** for ECG lead detection and **U-Net** for signal segmentation and separation. This research was also presented at **ICOICT 2026**:
- **DOI:** [10.1109/ICoICT71118.2026.11664756](https://doi.org/10.1109/ICoICT71118.2026.11664756)

For your information, I used Kaggle to train my models and I recommend you to do so. Feel free to explore the repository and learn more about the implementation, methodology, and results.

---

## Important Note on Repository Contents & Path Configuration

- **Excluded Model Weights & Datasets:** To protect the originality of this thesis work and comply with repository storage limits, pre-trained model weights (`*.pt`, `*.pth`), compressed archives (`*.zip`), private clinical/hospital datasets, and the full generated synthetic training/validation datasets (`matplotlib_ecg/` and bulk cropped/segmented outputs) are **not included** in this repository.
- **Custom Path Configuration:** All local file and directory paths in the notebooks have been cleared and replaced with empty strings (`"" # Fill with your own path`). Before running any notebook locally, please fill in `""` with the appropriate path on your own device.

---

## Project Workflow

1. **Generate synthesized ECG images:**
   Run `final_ecg_plotting.ipynb` using the PhysioNet PTB-XL Dataset (download directly from PhysioNet). Set your local dataset and output directory paths in `""` before running.

2. **Training YOLOv12 (used Kaggle):**
   Import the notebook called `Training YOLOv12.ipynb` inside the `YOLOv12 matplotlib` folder to Kaggle. If you want to run it, upload the synthesized images as the input on Kaggle. The result of the evaluation (`results.csv`) is already in the `YOLOv12 matplotlib` folder.

3. **Visualize YOLOv12 evaluation metrics:**
   Run `yolov12_eval.ipynb` inside the `YOLOv12 matplotlib` folder (fill in your path to `results.csv`).

4. **Training U-Net (used Kaggle):**
   Import the notebook called `final_unet_segmentation_model.ipynb` inside the `U-Net Segmentation` folder to Kaggle. If you want to run it, upload the cropped lead dataset and ground truth masks as the input on Kaggle. The evaluation metrics and visualizations are already in the `U-Net Segmentation` folder.

5. **Final evaluation for signal extraction with the best models from each step:**
   Run `combinedtest.ipynb` (fill in your local model weight and dataset paths in `""`). Evaluation results are inside the `test/other` folder.

6. **Demo File Program for Final Project Defense:**
   Run `final_combinedtest.ipynb` (fill in your local paths in `""`). The demo results are in the `test` folder under the `demo` and `comp` subfolders.

7. **Revision for signal extraction with Image Degradation:**
   Run `final_combinedtest - Copy.ipynb` (fill in your local paths in `""`). Evaluation results are inside the `test/other` folder.

---

Feel free to email me if you have further questions.  
**Email:** jauzazahra1997@gmail.com
