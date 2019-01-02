# Emotion-Aware-SYstem-EASY
## Demonstration <br>
![](working.gif)
   <br>
    User Emotion : Happy <br>
    Song Played : Taki Taki.mp3 <br>
    Quote Displayed : happiness is a state of mind
   
## Current Results <br>
| Module        | Quote Emotion Detection           | User Emotion Detection           | Music Emotion Detection           |
| ------------- |:-------------:|:-------------:|:-------------:|
| Accuracy      | 56.25% | 90.00% | 69.44% |
| Input      | Quote | User Facial Image | Music File |
| Filename      | model-10-0.0704.hdf5 |  model-07-0.1495.hdf5 | |
| Technique      | Ensembling | - | - |
| Tips to improve      | Expand Dataset | Expand Dataset | Expand Dataset |


## Running the app  
1. Training the quote classification model -
   1. The happy, motivated and compiled ( combined happy and motivated ) csv files ( in the same directory ) will be used ( or alternatively download the [happy](https://docs.google.com/spreadsheets/d/18jxlroMKeqfR_PBHx8Zon1QHY6TQv3NB0EnW909yn5s/edit?usp=sharing) and [motivated](https://docs.google.com/spreadsheets/d/102iHGh4NITqejrMyMwGUOEeQaKDLO1xYNTSvhTmLlEw/edit?usp=sharing) sheets in csv format and combine them yourself )
   2. Create a folder called ```QuoteBinaryData``` where trained model files appear  
   2. Place ```model-10-0.0704.hdf5``` in it (or alternatively train model on your own)
   3. Now run the ```Quote Classifier Binary new.ipynb``` file in jupyter notebook
2. Training the image classification model -  
   1. [Download the ```images``` folder](https://drive.google.com/open?id=15Yiqo51onEdvZEsfBHo7IQuM0gt8no8U) and place folder in the same directory
   2. The trained model files appear in the ```images``` folder  
   2. The ```model-07-0.1495.hdf5``` (for 3 emotions) appear in it (or alternatively train model on your own)
   3. Now run the ```Training 3 Image Classification new.ipynb``` (for 3 emotions) file in jupyter notebook
2. Training the music classification model -  
   1. [Download the ```songs``` folder](https://drive.google.com/open?id=1COYn4g5VcHbNZCPzWpyrq9DAsId3PCq1) and place folder in the same directory
   2. The trained model files appear in the ```songs``` folder  
   2. The ```.hdf5``` (for 3 emotions) appear in it (or alternatively train model on your own)
   3. Now run the ```.ipynb``` (for 3 emotions) file in jupyter notebook
2.	Run the video_face_eye_smile_detection.py file to generate live images that are used for the Image Classification model
3.	Run the EASY (Emotion Aware SYstem) app.ipynb -> this generates the list/ database for quotes, Then gets the emotion for the user image, also this runs the main app feature
## Maping Scheme

3 human emotions are detected by the model - Happy, Sad and Anger <br>
The mapping scheme between the user emotion, music played and quote displayed is as shown. 

| User Emotion        | Happy           | Sad           |  Anger           |
| ------------- |:-------------:|:-------------:|:-------------:|
| Music Played      | Happy | Sad | Calm|
| Quote Displayed      | Happy | Motivation| Motivation|

## Working 

The system delivers its service through the use of 3 submodels, namely -
* User emotion detection - User's facial image is captured and his/her emotion is discerned from that
* Quote emotion detection - The emotion from quotes is detected. The advantage of having a separate quote classifier is
   * No manual sorting of quotes needed in the future to add new quotes to the model
   * User has an option to add quotes or use only quotes of his choice. He can simply enter the text and the model would classify the quote by itslef and use it when it services him/her.
* Music emotion detection - The emotion from quotes is detected. The advantage of having a separate music classifier is similar to that of having a separate quote model.

### File Structure

### Architecture

## Experimental 

The model has been tweaked to detect 6 basic human emotions - happy, sad, fear, disgust, surprise and anger.<br>
The quote emotion detection model remains the same while the music emotion model has been expanded to detect 4 emotions - happy, sad, calm and motivation from music. 

| Module        | User Emotion Detection (6 emotions)          | Music Emotion Detection (4 emotions)          | 
| ------------- |:-------------:|:-------------:|
| Input      | User Facial Image | Music File |
| Accuracy      | 13.06% | 69.44% |
| Filename      | final_emotion_model.hdf5 | model-01-11.1613.hdf5 |
| Tips to improve      | Expand Dataset; Try Ensembling; retrain model; Instead of VGG try using Inception etc | Expand dataset |

### Running the experimental app  
1. Training the quote classification model remains the same as for the main model
2. Training the image classification model -  
   1.  [Download the ```images``` folder](https://drive.google.com/open?id=15Yiqo51onEdvZEsfBHo7IQuM0gt8no8U) and place folder in the same directory
   2. The trained model files appear in the ```images``` folder  
   2. The final ```final_emotion_model.hdf5``` (for 6 emotions)  appear in it (or alternatively train model on your own)
   3. Now run the ```Training 6 Image Classification new.ipynb``` (for 6 emotions)  file in jupyter notebook
2. Training the music classification model -  
   1. [Download the ```songs``` folder](https://drive.google.com/open?id=1COYn4g5VcHbNZCPzWpyrq9DAsId3PCq1) and place folder in the same directory
   2. The trained model files appear in the ```songs``` folder  
   2. The ```.hdf5``` (for 4 emotions) appear in it (or alternatively train model on your own)
   3. Now run the ```.ipynb``` (for 4 emotions) file in jupyter notebook
3. All other steps remain the sameas in the main model
### Maping Scheme

In the 6 emotion model, 6 basic human emotions are detected - Happy, Sad, Fear, Disgust, Suprise, Anger <br>
The mapping scheme between the user emotion, music played and quote displayed is as shown. 

| User Emotion        | Happy           | Sad           | Fear           | Disgust           | Suprise           | Anger           |
| ------------- |:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| Music Played      | Happy | Sad | Motivation| Calm| Happy| Calm|
| Quote Displayed      | Happy | Motivation| Motivation| Happy| Happy| Motivation|

## Related 
1. Requirements.txt - all the librarires intalled in my anaconda virtual env, ```python = 3.6.6``` 
2. [Image Corpus](https://drive.google.com/open?id=1Rq9An3UKM_iI_Y_yxWcN4hl-Z7-vfQgC)
3. [Happy songs](https://drive.google.com/open?id=1COYn4g5VcHbNZCPzWpyrq9DAsId3PCq1)
4. [Sad Songs](https://drive.google.com/open?id=1nz8cNJjT6BwDQAFeJEaelJWy6H5dbeO_)
5. [Calm Nature sounds](https://drive.google.com/open?id=1STlY0fBfP0pAsfHo_fvUBR37ZAkDmLiJ)
6. [Unsorted English Songs](https://drive.google.com/open?id=1SgjH6D-EKa6Tw-8y6RO1ufk5jg645eTP)
7. [Happy Quotes Processed](https://docs.google.com/spreadsheets/d/1lkEVYlqvIS5cV2rDRnlt2WICvK9VXiQkL75E8baU1w4/edit?usp=sharing) [Happy Quotes Unprocessed](https://docs.google.com/spreadsheets/d/18jxlroMKeqfR_PBHx8Zon1QHY6TQv3NB0EnW909yn5s/edit?usp=sharing) Note: This has some quote repetions, remove if possible
8. [Motivational Quotes](https://drive.google.com/open?id=102iHGh4NITqejrMyMwGUOEeQaKDLO1xYNTSvhTmLlEw) Note: This has some quote repetions, remove if possible
9. [Calm Quotes](https://drive.google.com/open?id=1j6ss3V4BKX7OXN4kpar4XdnPZWbxk67proouk0_tSac)
10. [Experimental Analysis and Testing ppt](https://docs.google.com/presentation/d/1QhqxY8rquuZjTnNE-IdLp1n02qkLtoIbwqBvuKvgn9A/edit?usp=sharing) Note: The values of accuracy have to be double checked
11. [Lit review, High level design and Low level design](https://docs.google.com/presentation/d/12rnb9dW4cCrw353vMp1lYFaMFPiRLtmV8wUuqWd8sPE/edit?usp=sharing)
11. HappySongs1_features.csv and HappySongs2_features.csv have a common 'Saiyan...' song entry, pls remove before merging, also the ' charecter causes pandas.read_csv() to have decoding problems, so change such names if possible
12. SadSongs_features.csv has the features extracted for sad songs
13. MotivationSongs_features.csv and CalmSongs.csv have only names of tracks, features still have to be extracted
1. Create a bigger data corpus to train all 3 components, especially for the image classifier give a lot of low res and low light photos that are typically seen in real world deployment
4. Make a web app for easy deployment on all platforms - cuurently have to run two different files (one to capture image, other to deliver services)

All Copy rights of Music belong to owners
