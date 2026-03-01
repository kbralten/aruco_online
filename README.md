# ArUco Online Scanner

A fast, lightweight web application for detecting and decoding ArUco markers directly in your browser.

## Features

- **Multi-Dictionary Detection**: Automatically tests against all predefined ArUco dictionaries (4x4, 5x5, 6x6, 7x7, AprilTag, and Original).
- **Robust Image Processing**: Automatically attempts to decode markers in four different image variations:
  - Standard RGB
  - Inverted RGB (useful for dark-themed or inverted markers)
  - Grayscale
  - Inverted Grayscale
- **Privacy-First**: All image processing is done locally in your browser using OpenCV.js. No images are uploaded to any server.
- **Drag & Drop**: Simple interface for uploading images by dragging them onto the workspace.

## How to Use

1. **Open the Scanner**: Open `index.html` in any modern web browser.
2. **Upload an Image**: Drag and drop an image file (PNG, JPEG, WebP) onto the upload zone, or click the zone to select a file from your device.
3. **Wait for Analysis**: The application uses your device's CPU to run the OpenCV.js detection engine. It may take a moment to scan through all 22+ dictionaries and 4 image variations.
4. **View Results**: 
   - Detected markers will be highlighted on the image canvas with colorful bounding boxes and ID labels.
   - A detection report will list each unique Marker ID found, the dictionary used, and the image variation that successfully decoded it.

## Technical Details

- **Built with**: HTML5, CSS3 (Vanilla), and JavaScript.
- **Computer Vision**: Powered by [OpenCV.js](https://docs.opencv.org/4.10.0/opencv.js).
- **AESTHETICS**: Features a dark-mode glassmorphism theme for a clean, modern look.

## Local Testing

Since this tool uses standard web APIs, you can run it by opening `index.html` directly from your file system. Note that some advanced browser security policies (CORS) may occasionally interfere with `cv.imread()` on local files; if this occurs, the script will attempt to decode the error and notify you in the browser console.
