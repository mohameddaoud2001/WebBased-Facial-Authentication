# Web-Based-Facial-Authentication-System

AddDataToDatabase.py: This is responsible for adding student data to the Firebase Realtime Database. It starts by initializing the Firebase app with the provided credentials. Then, it defines a reference to the "Students" node in the database. Next, it defines a dictionary containing information about each student, such as their name, major, starting year, total attendance, etc. Finally, it iterates over this dictionary, sets each student's data under their respective ID in the database.



encodeGenerator.py: This script handles the generation of facial encodings for student images using the face_recognition library. It also uploads the student images to Firebase Storage for later retrieval. It starts by initializing the Firebase app with the provided credentials, similar to the previous script. Then, it loads student images from a specified folder and generates facial encodings for each image using face_recognition. These encodings are then stored along with the corresponding student IDs in a pickle file named "EncodeFile.p". Additionally, the script uploads the student images to Firebase Storage for future reference.



main.py: This is the main script for the facial recognition attendance system. It begins by initializing the Firebase app with the provided credentials, just like the other scripts. Then, it captures video frames from a webcam and detects faces using face_recognition. For each detected face, it compares the facial encoding with the known encodings stored in "EncodeFile.p". If a match is found, it retrieves the corresponding student ID and fetches their information from the Firebase Realtime Database. It updates the student's attendance record in the database and displays relevant information on the screen, such as the student's name, major, total attendance, etc. Additionally, it handles different modes for displaying information and transitions between them based on the recognition process.

what you should do next: we need to go to https://console.firebase.google.com/project/webbased-facial-authentication/overview settings project settings
here we need to go to service accounts and in the service account we are going to go to python
and here we will generate new private key so we are going to
create and this will create our private key and then we have to copy this code
and add it to our uh python code so that it runs.

![image](https://github.com/mohameddaoud2001/WebBased-Facial-Authentication/assets/128754692/e4fd261c-ae96-417b-b520-98bacca24034)

