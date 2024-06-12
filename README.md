# Screen-Recording-Script-with-OpenCV-and-PyAutoGUI


https://github.com/khushi-98/Screen-Recording-Script-with-OpenCV-and-PyAutoGUI/assets/102850725/2cde2723-53b5-48d0-896a-e99e8acbbd7f

1. Library Imports:

-cv2: OpenCV library for handling video creation and processing.
-pyautogui: Used to capture screenshots of the screen.
-win32api: Retrieves system metrics like screen width and height.
-numpy: Converts screenshots into array format for OpenCV processing.
-time: Manages the timing and duration of the recording.

2.Screen Dimensions:

The script gets the screen width and height using GetSystemMetrics, which allows it to capture the full screen.

3.Video Writer Setup:

It sets up a VideoWriter object using OpenCV, specifying the codec (XVID), frame rate (30 frames per second), and dimensions of the video.

4.User Input for Duration:

The user is prompted to enter the desired recording duration in seconds.

5.Timing Calculation:

The script captures the current time and calculates the end time based on the user’s input, with an additional 2-second buffer.

6.Screen Capture Loop:

-The script enters a loop where it continuously takes screenshots of the screen.
-Each screenshot is converted from a PIL image to a NumPy array and then from BGR to RGB color format using OpenCV.
-The processed frames are written to the video file.
-The loop breaks when the current time exceeds the calculated end time.

7.Release Resources:

After the loop ends, the script releases the VideoWriter object to ensure that the video file is properly saved.
It prints a message indicating the end of the recording process.
