# Blurring Module Documentation

The Blur Module in this project is responsible for applying a simple averaging blur effect to the image. The blurring operation helps in reducing noise or achieving a desired visual effect by averaging the colors of pixels within defined regions. Below is a breakdown of the core functionalities within this module:

## Method Descriptions:

### `blurr_Click` Method:

- **Trigger**: This method is triggered when the user clicks the Blur button.
- **Functionality**: 
  - It checks if an image is loaded into `drawArea`.
  - If an image is loaded, it creates an instance of the `Procesare` class and calls the `Blur` method on the `Procesare` instance to apply the blur effect.
  - It then updates `drawArea` with the blurred image using `DrawFully` method.
  - If no image is loaded, it calls `NoImageLoaded` method to handle this case.

### `Blur` Method (Overloaded):

- **Parameters**:
  - `Bitmap image`: The image to be blurred.
  - `Int32 blurSize`: The size of the blur effect, indicating the size of the region around each pixel to be averaged.

- **Functionality**: 
  - The first overload simply calls the second overload, passing a rectangle representing the entire image dimensions along with the blur size.
  - The second overload performs the actual blurring operation:
    - It creates a new bitmap to hold the blurred image and copies the original image into it.
    - It locks the bits of the blurred image for direct memory access.
    - Iterates through each pixel in the specified rectangle, calculates the average color of a square region around each pixel (defined by `blurSize`), and sets all pixels in the region to this average color.

### `DrawFully` and Helper Methods:

- **Functionality**:
  - These methods (`JustDraw`, `DrawBitmapOnDrawArea`, `ResetDrawArea`) are used to update the `drawArea` with the new blurred image.

## How Blur Works:

The blurring operation in this module is a type of box blur, achieved through a three-step process for each pixel in the specified rectangle of the image:

1. **Region Definition**:
   - A square region around each pixel is defined, controlled by the `blurSize` parameter. For instance, if `blurSize` is set to 5, a 5x5 square region around each pixel is considered.

2. **Color Averaging**:
   - Within each defined region, the average color is computed. This involves summing the Red, Green, and Blue (RGB) values of all pixels within the region, and then dividing each sum by the total number of pixels in the region to obtain the average Red, Green, and Blue values.

3. **Color Assignment**:
   - All pixels within the defined region are then set to the average color calculated in the previous step. This process smooths out the color variations within each region, thereby achieving a blur effect.

The above steps are carried out iteratively for each pixel in the specified rectangle, resulting in a blurred version of the original image.

## Aspect Ratio Maintenance:

- The averaging method used in this module does not alter the aspect ratio of the image. The dimensions of the image remain unchanged; only the color values of the pixels are altered.

## Usage:

- The `blurSize` parameter controls the extent of the blurring. A larger `blurSize` value will result in a more pronounced blur effect, as a larger region around each pixel is averaged.

- It's important to note that increasing the `blurSize` value will also increase the processing time, as more pixels will need to be averaged for each pixel in the image.

