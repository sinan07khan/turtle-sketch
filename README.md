# Image to Turtle Drawing

A Python project that converts an image into a drawing using **OpenCV** and Python's built-in **Turtle graphics** module. It detects the outlines of an image and redraws them on the screen with an animated drawing effect.

## Features

- Convert images into turtle drawings.
- Detect image contours using OpenCV.
- Resize images while maintaining their aspect ratio.
- Remove small noise contours.
- Draw large shapes first.
- Animate the drawing process.
- Customize the image name, drawing size, speed, and pen settings.

## Requirements

- Python 3.x
- OpenCV
- Turtle (included with standard Python installations)

## Installation

Install OpenCV using pip:

```bash
python -m pip install opencv-python
```

## How to Use

1. Clone this repository:

   ```bash
   git clone https://github.com/sinan07khan/YOUR-REPOSITORY.git
   ```

2. Open the project folder.

3. Place your image in the same folder as the Python script.

4. Rename your image to `ss.png`, or change the image name on **line 12**:

   ```python
   IMAGE = "ss.png"
   ```

   For example:

   ```python
   IMAGE = "my_photo.jpg"
   ```

5. Run the Python script:

   ```bash
   python main.py
   ```

6. Watch your image transform into a turtle drawing.

## Customization

You can customize the drawing by changing these values in the code:

| Setting | Purpose |
|---|---|
| `IMAGE` | Image filename |
| `height = 600` | Drawing image height |
| `scale = 0.8` | Drawing scale |
| `UPDATE_EVERY = 3` | Screen refresh frequency |
| `pen.speed(3)` | Drawing animation speed |
| `pen.pensize(1)` | Pen thickness |
| `pen.color("black")` | Drawing color |
| `screen.bgcolor("white")` | Background color |

## Supported Image Formats

Common formats supported by OpenCV include:

- PNG
- JPG / JPEG
- BMP
- WebP

For the best results, use a clear image with good contrast between the subject and its background.

## How It Works

1. Loads the selected image.
2. Resizes the image while preserving its aspect ratio.
3. Converts the image to grayscale.
4. Applies thresholding to separate the foreground from the background.
5. Detects contours using OpenCV.
6. Filters out small contours and sorts the remaining shapes by area.
7. Converts image coordinates into Turtle coordinates.
8. Draws and fills the detected shapes using Turtle graphics.

## Notes

- Keep the image and Python script in the same folder, or provide the full image path.
- The current threshold value is `180`. Depending on the image, you may need to adjust it.
- The program primarily detects external contours, so internal details may not appear.
- Complex images with many contours can take longer to draw.
- The final result depends on the image's contrast, background, and composition.

## Technologies Used

- Python
- OpenCV
- Turtle Graphics

## Author

**Sinan Khan**

GitHub: [@sinan07khan](https://github.com/sinan07khan)

---

If you find this project useful, consider giving the repository a star!

