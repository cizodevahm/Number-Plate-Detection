# Number-Plate-Detection
This repository contains Python scripts for detecting and recognizing number plates using Support Vector Machines (SVM) and Block Binary Pixel Sum descriptors.

# Overview
The project consists of two main scripts:
 1. ```train_simple.py```: Trains classifiers for alphabet characters and digits using a dataset of font images.
 2. ```recognize.py```: Uses the trained classifiers to detect and recognize characters in number plates from images.

# Features
- Font Image Processing: Converts font images to grayscale and applies thresholding.
- Contour Detection: Identifies and sorts contours in the images.
- Feature Extraction: Uses Block Binary Pixel Sum descriptors to extract features from the regions 
  of interest (ROIs).
- Model Training: Trains SVM classifiers for both alphabet characters and digits.
- Model Serialization: Saves the trained models to disk for later use.
- Number Plate Detection: Detects number plates in images using the trained classifiers.
- Character Recognition: Recognizes and displays characters from detected number plates.

# Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/cizodevahm/Number-Plate-Detection.git
   ```
2. Navigate to the project directory:
   ```bash
   cd Number-Plate-Detection
   ```
   
# Usage
Training the Model
 1. Prepare your fonts dataset and place it in a directory.
 2. Run the training script:
    ```bash
    python train_simple.py --fonts path/to/fonts --char-classifier output/char_classifier.cpickle --digit-classifier output/digit_classifier.cpickle
    ```
3. The trained models will be saved in the specified output paths.
Recognizing Number Plates
 1. Place your images in a directory.
 2. Run the recognition script:
    ```bash
    python recognize.py --images path/to/images --char-classifier output/char_classifier.cpickle --digit-classifier output/digit_classifier.cpickle
    ```
3. The script will display the processed images with detected and recognized number plates.

# License
This project is licensed under the MIT License.
