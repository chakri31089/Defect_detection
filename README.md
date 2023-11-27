# Defect_detection
This code seems to be performing defect detection and classification on two images: 'good.png' and 'defect2.png', using OpenCV and NumPy.

## Reading Images
* Reads the 'good.png' and 'defect2.png' images using OpenCV's cv2.imread() function.
* Creates copies of the 'defect2.png' image for further processing (d, d4, ans).

## Converting to Grayscale
* Converts the 'defect2.png' and 'good.png' images to grayscale using cv2.cvtColor().

## Defect Detection
* Creates a mask (d4) from the 'defect2.png' image by inverting its colors and performing a bitwise AND operation with the 'good.png' image.
* Finds contours in the D4 mask using CV2. findContours() and filters contours with an area larger than 10.
* Draws rectangles around detected contours and annotates them as "flashes" on the image.

## Additional Defect Detection
* Creates another mask (d1) by performing a bitwise AND operation between the inverted 'good.png' image and the 'defect2.png' image.
* Finds contours in the d1 mask, filters contours with an area larger than 10, and annotates them as "cuts" on the image.

## Displaying Output
* Displays the annotated image using Matplotlib's plt.imshow() and also with OpenCV's cv2.imshow().

## User Interface
* Pauses the program until a key is pressed (cv2.waitKey(0)) and then closes the windows after a key is pressed (cv2.destroyAllWindows()).

## Explanation:
* The code performs defect detection on the 'defect2.png' image by comparing it with the 'good.png' image.
* It identifies and annotates areas considered "flashes" or "cuts" based on differences between the images, highlighting these areas with rectangles and labels.

The use of masks and bitwise operations helps isolate and identify these differences between the defect image and the reference 'good' image, allowing for visualization and identification of potential defects.

Identifies and localizes the defects in the image   
![alt text](https://github.com/chakri31089/Defect_detection/blob/main/Screenshot%202023-09-07%20104231.png?raw=true)
