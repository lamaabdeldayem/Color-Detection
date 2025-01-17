
# Video Processing Project with OpenCV and PIL

This project demonstrates the detection of a yellow ball in a video using OpenCV and PIL. The code applies color-based masking and identifies the bounding box of the detected object, then draws the bounding box around the object in the video frames.

## Requirements

To run the project, you need to install the required dependencies using `pip`:

- `opencv-python`
- `Pillow`
- `numpy`

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/lamaabdeldayem/Color-Detection.git
   cd Color-Detection
   ```

2. Install the dependencies:
   ```bash
   pip install opencv-python Pillow numpy
   ```

## Usage

Make sure the video file `Bouncing Red Ball (1).mp4` is in the same directory as the script, or update the path in the script accordingly.

Run the script:

```bash
python script_name.py
```

### Description of the code

- The script loads a video (`Bouncing Red Ball (1).mp4`) using OpenCV.
- It converts each frame from the video to the HSV color space.
- It defines a color range for yellow in the HSV space and creates a mask for pixels within this range.
- The script finds the bounding box of the yellow object in the mask and draws a rectangle around it on the original frame.
- The video is displayed with the bounding box, and you can press `q` to quit the video.

### Example

The video will show the bounding box drawn around the yellow object as it moves through the frames.

### Customizing the Color

If you want to track a different color, you can modify the `yellow` variable with a new color in the BGR color space. The `get_limits` function will automatically adjust the HSV range for the new color.

```python
yellow = [0, 0, 255]  # Change to a new BGR color if needed
```

### Example of `get_limits`:

If you have your custom function `get_limits` to return the lower and upper limits for HSV color detection, ensure it’s implemented in the `util.py` file as shown in the code.

```python
# Example get_limits function
def get_limits(color):
    # Your implementation of HSV limits based on the input color
    pass
```

