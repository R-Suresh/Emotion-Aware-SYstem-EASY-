# Emotion-Aware-SYstem-EASY-

Order of running app –<br>
1.	Run the Quote Classifier Binary.ipynb -> this trains the quote classification model, find dependencies listed in that
2.  Run the Training Image Classification.ipynb -> this trains the image classification model 
2.	Run the video_face_eye_smile_detection.py file to generate live images that are used for the Image Classification model
3.	Run the EASY (Emotion Aware SYstem) app.ipynb -> this generates the list/ database for quotes, Then gets the emotion for the user image, also this runs the main app feature
<br>
To do in the future,<br>

1.	Train image Classifier and then integrate it with live image in app, it probably can write its classification result in a variable that is used by other components ( Do this First as I suspect will take the most time and also predicting with live image may be hard ( Classes, etc)) 
2.	Make the music database and then, get the music model working ( u can follow the same classes as text classification) (Maybe just increase the sequence length, and only read main paragraph of song)
3.	Integrate all 3 components
<br>
On D day –<br>
1.	Check model extensively 
2.	Can try to display detected emotion in a text box or paragraph
3.	Get the ppt ready
4.	Get portable speaker ( one with good bass )
