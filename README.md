# Emotion-Aware-SYstem-EASY
## Working <br>
![](working.gif)
   <br>
    User Emotion : Happy <br>
    Song Played : Taki Taki <br>
    Quote Displayed : happiness is a state of mind
   
## Current Results <br>
| Module        | Quote Emotion Detection           | User Emotion Detection           |
| ------------- |:-------------:|:-------------:|
| Accuracy      | 56.25% | 90.00% |
| Input      | Quote | User Facial Image |
| Filename      | model-10-0.0704.hdf5 |  model-07-0.1495.hdf5 |
| Technique      | Ensembling | - |
| Tips to improve      | Expand Dataset | Expand Dataset |


## Running the app  
1. Training the quote classification model -
   1. Place the happy, motivated and compiled ( combined happy and motivated ) spread sheets in the same directory
   2. Create a folder called ```QuoteBinaryData``` where trained model files appear  
   2. Place ```model-10-0.0704.hdf5``` in it (or alternatively train model on your own)
   3. Now run the ```Quote Classifier Binary new.ipynb``` file in jupyter notebook
2. Training the image classification model -  
   1. [Download the ```images``` folder](https://drive.google.com/open?id=15Yiqo51onEdvZEsfBHo7IQuM0gt8no8U) and place folder in the same directory
   2. The trained model files appear in the ```images``` folder  
   2. The ```model-07-0.1495.hdf5``` (for 3 emotions) appear in it (or alternatively train model on your own)
   3. Now run the ```Training 3 Image Classification new.ipynb``` (for 3 emotions) file in jupyter notebook
2.	Run the video_face_eye_smile_detection.py file to generate live images that are used for the Image Classification model
3.	Run the EASY (Emotion Aware SYstem) app.ipynb -> this generates the list/ database for quotes, Then gets the emotion for the user image, also this runs the main app feature
## Maping Scheme

3 human emotions are detected by the model - Happy, Sad and Anger <br>
The mapping scheme between the user emotion, music played and quote displayed is as shown. 

| User Emotion        | Happy           | Sad           |  Anger           |
| ------------- |:-------------:|:-------------:|:-------------:|
| Music Played      | Happy | Sad | Calm|
| Quote Displayed      | Happy | Motivation| Motivation|

## Architecture
## File Structure
## Working <br>
In order to better serve user on a long term basis, the emotions of surprise, disgust and fear wchich were fleeting in nature compared to the emotions of happy, sad and anger, was dropped and a 3 emotion model was developed.<br>
Alternatively can make the 3 emotion model as the main one and the 6 emotion model as experimental
## To do in the future - <br>
1. Create a bigger data corpus to train all 3 components, especially for the image classifier give a lot of low res and low light photos that are typically seen in real world deployment
2. Create DNN for music classification
3. Make sure it runs on all other systems
4. Make a web app for easy deployment on all platforms - cuurently have to run two different files (one to capture image, other to deliver services)
5. Have some different Images in my system have to remove duplicates and upload to image corpus
## Experimental 
Have tried to develop a model to detect 6 basic human emotions.

| Module        | 6 Emotions Detection           |
| ------------- |:-------------:|
| Accuracy      | 13.06% |
| Filename      | final_emotion_model.hdf5 |
| Tips to improve      | Expand Dataset; Try Ensembling; retrain model; Instead of VGG try using Inception etc |

### Running the experimental app  
1. Training the quote classification model remains the same as for the main model
2. Training the image classification model -  
   1.  [Download the ```images``` folder](https://drive.google.com/open?id=15Yiqo51onEdvZEsfBHo7IQuM0gt8no8U) and place folder in the same directory
   2. The trained model files appear in the ```images``` folder  
   2. The final ```final_emotion_model.hdf5``` (for 6 emotions)  appear in it (or alternatively train model on your own)
   3. Now run the ```Training 6 Image Classification new.ipynb``` (for 6 emotions)  file in jupyter notebook
3. All other steps remain the sameas in the main model
### Maping Scheme

In the 6 emotion model, 6 basic human emotions are detected - Happy, Sad, Fear, Disgust, Suprise, Anger <br>
The mapping scheme between the user emotion, music played and quote displayed is as shown. 

| User Emotion        | Happy           | Sad           | Fear           | Disgust           | Suprise           | Anger           |
| ------------- |:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|:-------------:|
| Music Played      | Happy | Sad | Motivation| Calm| Happy| Calm|
| Quote Displayed      | Happy | Motivation| Motivation| Happy| Happy| Motivation|

## File descriptions - <br>
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

All Copy rights of Music belong to owners
