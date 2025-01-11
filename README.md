Parking Space Picker

Project Overview

The Parking Space Picker is a Python project that uses OpenCV to process parking lot images and videos to detect and manage parking spaces. It counts the number of occupied and vacant parking spaces and notifies the user when a parking space becomes available or is freed up. This tool is ideal for monitoring parking lots in real-time.

Features

Parking Space Detection:

Displays the total number of parking spaces available and occupied.

Real-time Updates:

Provides real-time updates on parking lot occupancy based on input video or image.

Notifications:

Sends desktop notifications when parking spaces are freed up or become available, along with their positions.

Visual Representation:

Shows a graphical overlay indicating vacant spaces in green and occupied spaces in red.

Dependencies

This project requires the following Python libraries:

cv2 (OpenCV): For image and video processing.

pickle: To serialize and deserialize Python objects.

cvzone: To simplify image processing tasks.

numpy: For array manipulations.

plyer: To send desktop notifications.

How It Works

Main Components

Mouse Interaction for Parking Spot Selection:

The user can select parking spaces in an image using left and right mouse clicks.

Left-click to add a parking space.

Right-click to remove a parking space.

The coordinates of the selected parking spaces are saved to a file (CarParkPos) using pickle.

Parking Space Detection:

Each parking space is processed to detect occupancy.

Vacant spaces are displayed in green, while occupied spaces are displayed in red.

Thresholding techniques are used to count the non-zero pixels in the cropped parking space regions.

Notifications:

Notifications are sent when:

A parking space becomes available.

A previously occupied parking space is freed up.

Workflow

Load a video or image of the parking lot.

Use the Parking Space Picker to define parking spaces.

Process each frame of the video:

Detect whether each defined parking space is vacant or occupied.

Count and display the number of free spaces.

Send notifications when changes in parking space status are detected.

Display the processed video with graphical overlays.

Usage Instructions

Setup Parking Spaces:

Run the Parking Space Picker script to define parking spaces in the image carParkImg.png.

Use the left and right mouse buttons to add/remove parking spaces.

Save the parking space coordinates to the file CarParkPos.

Run the Main Script:

Execute the main script to process the parking lot video (carPark.mp4).

View the real-time occupancy status on the displayed video.

Receive notifications about changes in parking space status.

Code Overview

Main File

The primary script for processing the parking lot video. It:

Reads the coordinates of parking spaces from the CarParkPos file.

Detects parking space occupancy using thresholding and pixel counting.

Displays the processed video with occupancy overlays.

Sends notifications about parking space availability.

Parking Space Picker File

A script to manually define parking spaces in a static image (carParkImg.png).

Use mouse interactions to define the parking spaces.

Saves the positions to a file for use in the main script.

Example Output

Graphical Overlay:

Green rectangles for vacant spaces.

Red rectangles for occupied spaces.

Notifications:

"Parking Space Available: 5/20\nAvailable Spaces: 3, 7, 15"

"Parking Space Freed Up: 4"

Console Output:

Displays the count of free and total parking spaces.

Future Improvements

Add support for multi-camera inputs for larger parking lots.

Use machine learning models to improve parking space detection accuracy.

Implement a web-based dashboard for remote monitoring.

Author

This project is created by combining the power of OpenCV and Python to provide an intuitive and functional parking lot management system.
