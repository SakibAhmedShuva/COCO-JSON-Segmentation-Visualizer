# COCO JSON Segmentation Visualizer

A simple and efficient tool for visualizing COCO format annotations including bounding boxes, segmentation masks, and category labels using Jupyter Notebook.

## Overview

This repository provides a Jupyter notebook implementation for visualizing COCO (Common Objects in Context) format annotations. It supports:
- Bounding box visualization
- Segmentation mask overlay
- Category labels
- Random sample visualization
- Individual image inspection

## Requirements

```bash
pip install -r requirements.txt
```

Required packages:
- opencv-python
- numpy
- matplotlib
- jupyter

## Repository Structure

```
COCO-JSON-Segmentation-Visualizer/
├── coco_viz.ipynb          # Main Jupyter notebook with visualization code
├── requirements.txt        # Python dependencies
├── annotations/           # Directory for COCO JSON annotation files
│   └── modified_annotations.json
└── images/               # Directory containing image files
```

## Usage

1. Clone the repository:
```bash
git clone https://github.com/SakibAhmedShuva/COCO-JSON-Segmentation-Visualizer.git
cd COCO-JSON-Segmentation-Visualizer
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Open and run the Jupyter notebook:
```bash
jupyter notebook coco_viz.ipynb
```

### Visualizing Random Samples

```python
visualizer = COCOVisualizer(
    annotations_file='./annotations/modified_annotations.json',
    images_dir='./images'
)

# Show random samples
visualizer.show_random_samples()
```

### Visualizing Specific Images

```python
visualizer = COCOVisualizer(
    annotations_file='./annotations/modified_annotations.json',
    images_dir='./images'
)

# List available images
print(visualizer.list_images())

# Show specific image
visualizer.show_image('image_filename.jpg')
```

## Features

- **Multiple Visualization Options:**
  - Bounding boxes
  - Segmentation masks
  - Category labels
  - Random sample viewing
  - Individual image inspection

- **Customization Options:**
  - Adjustable figure size
  - Toggle bounding boxes
  - Toggle segmentation masks
  - Toggle category labels
  - Consistent color mapping for categories

- **Error Handling:**
  - Validates image file existence
  - Validates annotation presence
  - Clear error messages for missing files/annotations

## Class Methods

- `__init__(annotations_file, images_dir)`: Initialize visualizer with paths
- `list_images()`: List all available image filenames
- `show_image(filename, figsize=(15, 10))`: Display specific image with annotations
- `show_random_samples(num_samples=4, figsize=(15, 15))`: Display random sample images
- `visualize_image_by_filename(filename, show_bbox=True, show_segmentation=True, show_labels=True)`: Core visualization method

## Contributing

Feel free to open issues or submit pull requests for any improvements or bug fixes.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- COCO Dataset format: [COCO - Common Objects in Context](https://cocodataset.org/)
- OpenCV and Matplotlib libraries

## Contact

If you have any questions or suggestions, please feel free to open an issue in the repository.
