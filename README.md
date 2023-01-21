# Simple face regconition system
## Prerequisite

* MTCNN - detect faces
* Facenet - extract features from the cropped face

# Introduction 

With the use of already established and well documented models, this program uses such components to deviate a simple system to regconize faces. With the face detected and cropped with MTCNN, we extract its features via Facenet, serialized and stored with pickles. The already saved features which are labeled accordingly to the user whose indentity we want to recognize, are used to compared whether the current face detected is registered in the system. The process is carried out by computating the cosine similarity between the current detected face and every labeled features stored in the database, if the returned result passes a certain threshold which is 0.6, display the name of the recognized individual using the system. Otherwise display as unknown.

# Quick start

* Run FaceCapture.ipynb file, enter the name corresponding to the face wanted to be registered, angle your face in many angles to increase the variation of extracted features which improve system capibility to recognize your face

* Run ExtractingFeatures.ipynb file to extract the features from the cropped images and serilize it for later use

* Run Test.ipynb, the system will draw a bounding box around your face which indicates if it's detecting a face. It will then display the name of the face if it's registered beforehand or isn't - uknown.

 # Demonstration
 

https://user-images.githubusercontent.com/82890282/210814609-bc385522-ed04-40af-802f-d338677f1bb5.mp4



# Disclaimer 
The face recognition will run through every single extracted features to compare with the current face detected so it doesn't scale very well with a big database and should be replaced with a classification model to solve such problem



