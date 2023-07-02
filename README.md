# Student Attendance Facial Recognition System

This program allows you to perform face recognition-based attendance using a webcam. The program integrates with Firebase for storing images and updating attendance data in real-time. Follow the instructions below to run the program successfully.

## Prerequisites

- Python 3.x installed on your machine.
- PyCharm IDE installed (optional but recommended).
- c++ Development environment (visual studio/ xcode)

## Setup

1. Clone or download the project files to your local machine.
2. Install the required Python packages by running the following command in the terminal or command prompt:

   ```
   pip install opencv-python numpy face-recognition cvzone firebase-admin
   ```

3. Create a Firebase project and set up a Realtime Database and Storage bucket. Make sure to note down the database URL and storage bucket name.

4. Generate a service account key file for your Firebase project following the steps mentioned in the Firebase documentation. Save the JSON file as `serviceAccountKey.json` in the project directory.

## Adding Data to the Database

1. Open the `AddDatatoDatabase.py` file in the PyCharm IDE or any other text editor.
2. Replace the `databaseURL` and `storageBucket` placeholders with your Firebase project's database URL and storage bucket name.
3. Customize the code in the file to add the required data to your database. For example, you can add student information such as name, major, year, etc., along with their corresponding images.
4. Save the file and run it using the PyCharm IDE or by executing the following command in the terminal:

   ```
   python AddDatatoDatabase.py
   ```

   This will add the data and images to your Firebase project's database and storage.

## Generating Face Encodings

1. Open the `EncodeGenerator.py` file in the PyCharm IDE or any other text editor.
2. Replace the `databaseURL` and `storageBucket` placeholders with your Firebase project's database URL and storage bucket name.
3. Customize the code in the file to retrieve the student images from the storage and generate their face encodings.
4. Save the file and run it using the PyCharm IDE or by executing the following command in the terminal:

   ```
   python EncodeGenerator.py
   ```

   This will generate the face encodings for the student images and save them in the `EncodeFile.p` pickle file.

## Running the Face Attendance Program

1. Open the `main.py` file in the PyCharm IDE or any other text editor.
2. Replace the `databaseURL` and `storageBucket` placeholders with your Firebase project's database URL and storage bucket name.
3. Save the file.
4. In the PyCharm IDE, open the terminal and navigate to the project directory.
5. Run the following command to execute the program:

   ```
   python main.py
   ```

   This will start the face recognition-based attendance program using your webcam. The program will display the webcam feed with attendance information overlaid on the screen.

6. The program will automatically recognize faces and update the attendance data in real-time based on the face matches. The attendance information will be retrieved from the Firebase Realtime Database and displayed on the screen.

7. To exit the program, press the "Esc" key or close the program window.

Note: Make sure your webcam is working correctly and properly positioned to capture faces.

Feel free to customize the program as per your requirements and integrate additional features if needed.
