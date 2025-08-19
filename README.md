# Augmented Reality with ArUco Markers

This project demonstrates augmented reality (AR) using OpenCV's ArUco markers to overlay source media onto destination media in real-time.

Demo video: https://youtu.be/ig5e9YUGeJo

## Features

- **ArUco Marker Detection**: Detects 4 specific ArUco markers (IDs: 23, 25, 30, 33) to define a rectangular region
- **Perspective Transformation**: Applies homography to warp source content onto the detected marker region
- **Multi-format Support**: Works with both images and videos as source and destination media
- **Real-time Processing**: Processes video frames in real-time for smooth AR overlay

## Files

- `main.ipynb` - Main Jupyter notebook containing the AR implementation
- `source.mp4` - Source video to be overlaid
- `destination.mp4` - Destination video containing ArUco markers
- `final_output.mp4` - Generated output video with AR overlay
- `marker_*.png` - ArUco marker images (IDs: 23, 25, 30, 33)

## Usage

1. Ensure your destination media contains the 4 ArUco markers positioned at the corners of your desired overlay region
2. Run the Jupyter notebook `main.ipynb`
3. The processed output will be saved as `final_xxx.mp4`

## Dependencies

- OpenCV
- NumPy
- Matplotlib
- MoviePy (for video display)

## How it Works

1. **Marker Detection**: Detects ArUco markers in the destination frame
2. **Corner Extraction**: Extracts corner coordinates from the 4 markers
3. **Homography Calculation**: Computes perspective transformation matrix
4. **Warping**: Applies transformation to overlay source content onto the marker region
5. **Blending**: Combines the warped content with the original destination frame