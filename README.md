# Image Colorization: Prokudin-Gorskii Glass Plate Reconstruction 🎨
* **Course:** CMSC426
* **Author:** Arik Gershman

## Viewing This Project
The Jupyter notebook contains embedded output and visualizations, which makes it too large to render directly on GitHub. For the best experience:
* 📄 **[View the PDF](CMSC426_Assignment1_sp26.pdf)** — recommended for a quick look at the code and results
* 📓 **[View the notebook on nbviewer](https://nbviewer.org/github/arikgershman/image-colorization-cv/blob/main/CMSC426_Assignment1_sp26.ipynb)** — for interactive notebook rendering
* 💾 Download the `.ipynb` file to run it locally

## Project Overview
The goal of this project is to reconstruct a full-color image from digitized Prokudin-Gorskii glass plate photographs. These historical photographs consist of three grayscale images captured through red, green, and blue filters. Because the images were taken with slight camera movement and subject motion during exposure, the three color channels are vertically stacked and slightly misaligned.

To produce a visually coherent color image, the three color channels must first be extracted. The primary challenge lies in accurately aligning the channels to minimize visual artifacts. They are then precisely aligned with one another before being combined into a single RGB image.

## Methodology
The alignment is performed by searching over possible displacements and selecting the one that maximizes a similarity metric between channels. The metrics used to evaluate and score alignment accuracy include:
* **Sum of Squared Differences (SSD)**
* **Normalized Cross-Correlation (NCC)**

Once the optimal alignment is found, the channels are stacked to form the final color image.

## Technologies Used
* **Language:** Python
* **Environment:** Jupyter Notebook
* **Libraries:** NumPy, PIL (Python Imaging Library)
