# License Plate Detection with YOLOv3-tiny

This project demonstrates how to train a YOLOv3-tiny object detection model to detect license plates in images. The dataset used is a combination of the "Indian Vehicle Dataset" from Kaggle and additional images from "State-wise_OLX".

## Steps:

1. **Data Preparation:**
   - Download the datasets and extract them.
   - Parse the XML annotation files to extract bounding box coordinates and license plate numbers.
   - Calculate center coordinates, bounding box width and height, and other relevant features.
   - Concatenate and shuffle the data.
   - Split the data into train, validation, and test sets.

2. **Model Configuration:**
   - Clone the Ultralytics YOLO repository.
   - Modify the `yolov3-tiny.yaml` file to set the number of classes (nc) to 1 (license plate).

3. **Dataset Organization:**
   - Create directories for train, validation, and test sets within the `ultralytics/datasets` folder.
   - Copy images and generate corresponding text files with label information (class, center coordinates, width, height) for each set.

4. **Training:**
   - Create a `custom_dataset.yaml` file specifying the paths to train, validation, and test sets.
   - Train the YOLOv3-tiny model using the command:
     
5. **Evaluation:**
   - Analyze the training results in the `results.csv` file.

## Next Steps:

- **Optical Character Recognition (OCR):**
   - Integrate an OCR library (e.g., EasyOCR, Tesseract) to extract the text from the detected license plates.
   - This step would involve:
     - Cropping the license plate region from the image based on the detected bounding box.
     - Preprocessing the cropped image (e.g., resizing, noise reduction).
     - Applying the OCR library to recognize the characters.
     - Post-processing the OCR output to refine the extracted text.

## Usage:

- To use the trained model for inference, follow the instructions in the previous response.

## Additional Notes:

- Consider experimenting with different YOLO architectures or hyperparameters to improve detection accuracy.
- Explore data augmentation techniques to increase the robustness of the model.
- Implement error handling and validation checks to ensure the OCR process is reliable.     
