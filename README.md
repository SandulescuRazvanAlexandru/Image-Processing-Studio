# Image Processing Studio

Image Processing Studio is a comprehensive tool designed to facilitate a wide range of image processing tasks. Developed using C#, this tool encompasses a variety of modules each dedicated to specific image manipulation and analysis tasks such as edge detection, scaling, scatter plot visualization, and more.

## Table of Contents

1. [Installation](#installation)
2. [Usage](#usage)
   - [File Module](#file-module)
   - [Edge Detection Module](#edge-detection-module)
   - [Scale Module](#scale-module)
   - [Scatter Plot Visualization Module](#scatter-plot-visualization-module)
   - [Grayscale Conversion Module](#grayscale-conversion-module)
   - [Color Inversion Module](#color-inversion-module)
   - [Blurring Module](#blurring-module)
   - [Resizing Module](#resizing-module)
   - [Face Detection Module](#face-detection-module)
   - [Clustering Module](#clustering-module)
3. [Contributing](#contributing)
4. [License](#license)

## Installation

To get started with Image Processing Studio, follow these steps:

1. Clone the repository from GitHub.
2. Open the project in Visual Studio by double-clicking on the `.sln` file.

## Usage

### File Module

#### Summary:
- The File Module facilitates user interaction with image files and manages the content within the UI. It provides functionalities for opening, capturing, reloading, zooming, and saving images.

#### Key Features:
- Open Image: Upload images from local storage.
- Web Camera: Capture images using a web camera.
- Reload Image: Revert to the original image after applying effects.
- Resize Zoom: Reset the view of the image to its original size and scale.
- Save Image: Save the currently displayed image to local storage.

### Edge Detection Module

#### Summary:
- This module processes images to identify and highlight edges based on color differences. It is triggered by a button click in the user interface.

#### Key Features:
- Edge Detection: Identifies edges based on a user-defined threshold value.
- Color Difference Calculation: Computes color differences between adjacent pixels to determine edges.
- Adjustable Sensitivity: Users can adjust the sensitivity of edge detection through the threshold value.

### Scale Module

#### Summary:
- The Scale Module scales coordinates of points derived from the Edge Detection module to fit within a new coordinate space suitable for visualization.

#### Key Features:
- Scaling Equations: Utilizes linear equations to adjust the coordinates.
- Sorting: Sorts the scaled points.
- Data Reduction: Removes duplicate points to reduce data size.

### Scatter Plot Visualization Module

#### Summary:
- This module is responsible for visualizing the scaled data points as a scatter plot using an external library.

#### Key Features:
- Scatter Plot Visualization: Displays the scaled data points as a scatter plot.
- External Library Usage: Utilizes an external library for rendering the scatter plot.

### Grayscale Conversion Module

#### Summary:
- This module converts a color image to grayscale, maintaining the brightness.

#### Key Features:
- Grayscale Conversion: Converts the image to grayscale using a predefined grayscale value array.

### Color Inversion Module

#### Summary:
- The Color Inversion Module applies a negative effect to an image by inverting the color of each pixel.

#### Key Features:
- Color Inversion: Inverts the color values of each pixel to create a visual negative of the image.

### Blurring Module

#### Summary:
- This module applies a simple averaging blur effect to the image to reduce noise or achieve a desired visual effect.

#### Key Features:
- Averaging Blur: Applies a blur effect by averaging the colors of pixels within defined regions.

### Resizing Module

#### Summary:
- Facilitates the resizing of an image based on user input while maintaining the original aspect ratio.

#### Key Features:
- Resizing with Aspect Ratio Maintenance: Resizes the image to desired dimensions without distorting the aspect ratio.

### Face Detection Module

#### Summary:
- This module encompasses functionalities for detecting faces and eyes using different models and classifiers.

#### Key Features:
- Face and Eye Detection: Utilizes Haar cascades and LBP classifiers for face and eye detection.
- Landmark Detection: Detects face landmarks using a pre-trained model.

### Clustering Module

#### Summary:
- The Clustering module employs the K-Means clustering algorithm to group data points into clusters based on certain attributes.

#### Key Features:
- K-Means Clustering: Categorizes data points into clusters.
- Data Loading and Visualization: Loads data from CSV files and visualizes clustering results.

## Contributing

We welcome contributions that improve the code and functionality of Image Processing Studio. Feel free to submit pull requests, and ensure that your contributions adhere to the existing coding standards and conventions.

## License

MIT
