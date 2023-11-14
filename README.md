# Photo Mosaic Creator

## Overview

The Photo Mosaic Creator is a Python project that transforms an input image into a mosaic by replacing its tiles with smaller images from a predefined set. The project utilizes OpenCV and NumPy for image processing.

## Getting Started

### Prerequisites

- Python 3.x
- OpenCV
- NumPy

### Installation

1. Clone the repository

2. Install dependencies:

    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. Ensure that the input image is the one present in "image.jpg" and the source tile images are in the predefined animals folder.
2. Run the Photo Mosaic Creator script:

    ```bash
    python main.py
    ```

3. View the generated mosaic in the "output.jpg" file.

## How It Works

The Photo Mosaic Creator follows these steps:

1. **Image Caching:**
   - The script reads images from the "animals" directory and calculates the average color for each image.
   - The data is cached in a JSON file named "cache.json" to avoid recalculating for every run.

2. **Mosaic Generation:**
   - The input image is divided into tiles, and each tile's average color is calculated.
   - For each tile, the closest match from the cached image data is determined based on average color.
   - The selected image is resized to match the tile dimensions and replaces the original tile.

3. **Display and Save:**
   - The resulting mosaic is displayed using OpenCV.
   - The final mosaic is saved as "output.jpg."

## OpenCV Usage

In the Photo Mosaic Creator project, [OpenCV (cv2)](https://opencv.org/) is a key library for various image processing tasks:

1. **Image Loading:**
   - `cv2.imread()` is used to read input images and images from the predefined set.

2. **Image Resizing:**
   - `cv2.resize()` is employed to resize the selected images to match the dimensions of the tiles in the mosaic.

3. **Image Display:**
   - `cv2.imshow()` is utilized to display the intermediate mosaic during the creation process.

4. **Final Mosaic Save:**
   - `cv2.imwrite()` is used to save the final mosaic as "output.jpg."

OpenCV plays a crucial role in handling various image manipulation tasks, contributing to the creation of vibrant and visually appealing photo mosaics.


## Configuration

Adjust parameters like `tile_height`, `tile_width`, and others in the script to experiment with different mosaic effects.

## Contributing

Contributions are welcome! If you have ideas for improvements or find issues, please create an issue or submit a pull request.

## License

This project is licensed under the [MIT License](LICENSE).
