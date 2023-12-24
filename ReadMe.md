# Project Documentation
This project is a facial recognition system that captures faces from a video feed, stores them, and uses them to take attendance. The project is structured as follows:

# Files
\ add_faces.py
This script captures faces from a video feed using OpenCV and a Haar Cascade classifier. The faces are resized and stored in a list. The user is prompted to enter their name, and the script captures 100 images of the user's face. The images and the name are then stored in pickle files in the data/ directory.

\ app.py
This is a Streamlit application that displays the attendance data in a table. The attendance data is read from a CSV file in the Attendance/ directory. The file is named with the current date. The application refreshes every 2 seconds to update the attendance data.

test.py
This script uses a K-Nearest Neighbors classifier to recognize faces. The classifier is trained on the faces and names stored in the pickle files in the data/ directory. The script captures faces from a video feed, recognizes them, and records the attendance in a CSV file in the Attendance/ directory. The file is named with the current date.

Attendance/Attendance_24-12-2023.csv
This is an example of an attendance CSV file. It contains two columns: 'NAME' and 'TIME'. Each row represents a recognized face and the time it was recognized.

data/faces.pkl and data/names.pkl
These are pickle files that store the faces and names captured by the add_faces.py script. They are used to train the K-Nearest Neighbors classifier in the test.py script.

data/haarcascade_frontalface_default.xml
This is a Haar Cascade classifier file used by OpenCV to detect faces in the video feed.

Usage
Run the add_faces.py script and follow the prompts to capture your face and enter your name.
Run the test.py script to start the facial recognition and attendance recording system.
Run the app.py script to start the Streamlit application and view the attendance data.
Dependencies
This project requires the following Python libraries:

OpenCV
Streamlit
pandas
numpy
pickle
sklearn
win32com.client
datetime
time
You can install these libraries using pip:

