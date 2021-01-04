# face-recognition-attendance-system

The HOG (Histogram of Gradients) is a straightforward feature extraction process that was developed with the idea of identifying real world entities such as human, objects, buildings, vehicles, pedestrians within images.


Basics python implementations

First we will find the faces in our images . This is done using HOG (Histogram of Oriented Gradients) at the backend.
Once we have the face they are warped to remove unwanted rotations. Then the image is feed to a pretrained neural network that out puts 128 measurements that are unique to that particular face. The parts that the model measures is not known as this is what the model learns by itself when it was trained.

Compare Faces and Find Distance :
We can use the compare_faces function to find if the faces match. This function returns True or False. Similarly we can use the face_distance function to find how likely is the faces match in terms of numbers. This is helpul particularly when there are multiple faces to detect from. The lower the distance the better the match.

attendance python implementation : An attendance system where the user is automatically logged when they are detected in the camera. We will store the name along with the time when they appeared.

step 1 : Importing images : Imported same images as done in basics.py. can add the images also if it necessary.  when we have multiple images, importing them individually can become messy. Therefore we will write a script to import all images in a given folder at once. For this we will need the os library so we will import that first. We will store all the images in one list and their names in another.

step 2 : Compute Encodings

step3 : Webcam : The while loop is created to run the webcam. But before the while loop we have to create a video capture object so that we can grab frames from the webcam.
Webcam Image : First read the image from the webcam and then resize it to quarter the size. This is done to increase the speed of the system. Even though the image being used is 1/4 th of the original, we will still use the original size while displaying.
Webcam Encodings : find all the faces in our image. The face_locations function is used for this purpose. Later, find the face_encodings as well.

step 4 : Find Matches : Now we can match the current face encodings to our known faces encoding list to find the matches. We will also compute the distance. This is done to find the best match in case more than one face is detected at a time.

step 5 : Automated attendance system :  If the user in the camera already has an entry in the file then nothing will happen. On the other hand if the user is new then the name of the user along with the current time stamp will be stored. We can use the datetime class in the date time package to get the current time.
