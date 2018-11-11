# Emotion-Aware-SYstem-EASY-

## Order of running app – <br>
1.	Run the Quote Classifier Binary.ipynb -> this trains the quote classification model, find dependencies listed in that
2.  Run the Training Image Classification.ipynb -> this trains the image classification model 
2.	Run the video_face_eye_smile_detection.py file to generate live images that are used for the Image Classification model
3.	Run the EASY (Emotion Aware SYstem) app.ipynb -> this generates the list/ database for quotes, Then gets the emotion for the user image, also this runs the main app feature
## To do in the future - <br>
1. Create a bigger data corpus to train all 3 components, especially for the image classifier give a lot of low res and low light photos that are typically seen in real world deployment
2. Create DNN for music classification
3. Make sure it runs on all other systems
4. Make a web app for easy deployment on all platforms - cuurently have to run two different files (one to capture image, other to deliver services)
## On D day – <br>
1. Check model extensively 
2. Can try to display detected emotion in a text box or paragraph
3. Get the ppt ready
4. Get portable speaker ( one with good bass )
## File descriptions - <br>
1. Requirements.txt - all the librarires intalled in my anaconda virtual env, ```python = 3.6.6``` 
2. [Image Corpus](https://drive.google.com/open?id=1Rq9An3UKM_iI_Y_yxWcN4hl-Z7-vfQgC)
3. [Happy songs](https://drive.google.com/open?id=1COYn4g5VcHbNZCPzWpyrq9DAsId3PCq1)
4. [Sad Songs](https://drive.google.com/open?id=1nz8cNJjT6BwDQAFeJEaelJWy6H5dbeO_)
5. [Happy Quotes](https://docs.google.com/spreadsheets/d/18jxlroMKeqfR_PBHx8Zon1QHY6TQv3NB0EnW909yn5s/edit?usp=sharing) Note: This has some quote repetions, remove if possible
6. [Motivational Quotes](https://drive.google.com/open?id=102iHGh4NITqejrMyMwGUOEeQaKDLO1xYNTSvhTmLlEw) Note: This has some quote repetions, remove if possible
7. [Calm Quotes](https://drive.google.com/open?id=1j6ss3V4BKX7OXN4kpar4XdnPZWbxk67proouk0_tSac)

All Copy rights of Music belong to owners
