## This project is designed to detect colors within an image and provide information on the color, such as the name and the hex code. It was created using Python and the OpenCV library.

### Dependencies
- Python 3.x
- OpenCV
- Numpy
### Usage
### To use this color detection project, follow the steps below:

- Clone this repository
- Install the dependencies using pip install -r requirements.txt
- Run the color_detection.py script
- Enter the file name (with extension) of the image you want to detect colors from
- Click on any pixel on the image to detect its color and display the color name and hex code
### How it works
The color detection algorithm works by first converting the input image from the RGB color space to the HSV (Hue, Saturation, Value) color space. This is because the HSV color space separates the image intensity (value) from the color information (hue and saturation), which makes it easier to detect colors.

After converting to the HSV color space, the script creates a list of color ranges that correspond to specific colors (e.g. red, green, blue, etc.). The script then uses OpenCV's inRange() function to create a mask for each color range, which highlights all pixels in the image that fall within the range.

The script then uses OpenCV's moments() function to calculate the centroid of each color region. The centroid represents the center of the color region and is used to determine the color name and hex code of the detected color.

Finally, the script uses a dictionary to map the centroid coordinates to color names and hex codes, and displays the information on the screen when a pixel is clicked




