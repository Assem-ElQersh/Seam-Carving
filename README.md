# Seam Carving

Welcome to the Seam Carving repository! This mini-project is part of the "Computer Vision and Pattern Recognition" course (CSE 429) at E-JUST. This project aims to implement a content-aware image resizing algorithm (seam carving) that scales down images horizontally and vertically without distorting important content.

## Project Overview

Seam carving is a technique that resizes images by intelligently removing (or inserting) seams—paths of pixels that have the least importance (as measured by an energy function). In our implementation, the energy function is defined as:

> **e₁ = |∂ₓI| + |∂ᵧI|**

This repository contains multiple versions of the implementation, showcasing the evolution of the project from a basic implementation to an optimized version with horizontal seam carving support.

## Repository Structure

```plaintext
Seam-Carving/
├── README.md                    # Project overview and instructions
├── LICENSE                      # MIT License
├── requirements.txt             # List of dependencies
├── input/                       # Folder for input images
│   └── original.jpg             # Example input image
├── outputs/                     # Folder for generated outputs
│   ├── carved_image.jpg         # Resized image after seam carving
│   ├── seams_visualization.jpg  # Original image with removed seams marked in red
│   ├── energy.jpg               # Energy map visualization
│   └── grayscale.jpg            # Grayscale version of the original image
└── Version_01.py                # Initial implementation
```

## How to Run

1. **Clone the repository:**

    ```sh
    git clone https://github.com/Assem-ElQersh/Seam-Carving.git
    cd Seam-Carving
    ```

2. **Install the required dependencies:**

    ```sh
    pip install -r requirements.txt
    ```

3. **Run the script:**

    The current release (Version3.py) automatically scales down the image in both directions (horizontal and vertical) to 50% of its original dimensions and generates four outputs:
    - The **resized image**.
    - The **seam visualization** (original image with removed seams marked in red).
    - The **energy visualization**.
    - The **grayscale image** for reference.

    ```sh
    python Version_01.py
    ```

    Make sure to place your input image (`original.jpg`) in the `input/` folder. You can adjust the desired scale factor and number of rows/columns to remove within the code if needed.

## Outputs

After running the script, you will find the following images in the `outputs/` folder:
- **carved_image.jpg**: The image after seam carving (resized to 50% of original dimensions).
- **seams_visualization.jpg**: The original image with the removed seams is marked in red.
- **energy.jpg**: Visualization of the computed energy map.
- **grayscale.jpg**: Grayscale version of the original image.

## Future Versions

This repository is structured to support multiple versions. You can extend this project by adding further improvements or new techniques in subsequent versions (e.g., Version3.py, etc.).

## License

This project is licensed under the MIT License. See the [LICENSE](https://github.com/Assem-ElQersh/Seam-Carving/blob/main/LICENSE) file for details.
