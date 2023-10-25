# Color Inversion Module Documentation

The Negative Module is designated for applying a negative effect to an image. This effect inverts the color of each pixel, creating a visual negative of the original image. The color inversion is done individually on each color channel (Red, Green, and Blue) of every pixel.

## Core Methods

### `negative_Click`
- **Parameters:**
  - `object sender`: The source of the event.
  - `EventArgs e`: An EventArgs that contains the event data.
- **Behavior:**
  - Verifies if an image is loaded in the `drawArea`.
  - If an image is loaded, an instance of the `Procesare` class is created, passing the bitmap from `drawArea`.
  - Calls the `Negative` method of the `Procesare` instance to apply the negative effect.
  - Invokes `Polishing` method, passing the `Procesare` instance, to finish the processing and update the `drawArea`.
  - If no image is loaded, calls the `NoImageLoaded` method to handle the situation.

### `Negative`
- **Behavior:**
  - Iterates through each pixel of the image.
  - For each pixel, the Red, Green, and Blue values are inverted using the bitwise NOT operation (`~`).
  - Continues until all pixels have been processed.

### `Polishing`
- **Parameters:**
  - `Procesare procesare`: The `Procesare` instance handling the image processing.
- **Behavior:**
  - Calls `FinishProcessing` method of the `Procesare` instance to unlock the bitmap data.
  - Invalidates the `drawArea` to trigger a repaint with the updated image.

### `FinishProcessing`
- **Behavior:**
  - Unlocks the bitmap data to finalize the processing.

## Negative Effect Logic
The negative effect is achieved by inverting the color values of each pixel. This is executed using the bitwise NOT operation (`~`) on each color channel (Red, Green, and Blue) of each pixel. The bitwise NOT operation flips each bit in the binary representation of the number, effectively inverting the color value.

This operation is applied to every pixel in the image, resulting in an image with inverted colors, also known as a negative image.

