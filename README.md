# FaceExtraction
Using dLib and openCV  to extract faces from the image and making the background Transparent.

# Method
Loaded images are applied in two dLib functions of detector and predictor.
We iterate on the faces detected by detector and each face is passed into predictor to find out the facial landmarks on the face.
To use predictor function we need to use a shape_predictor_68_face_landmarks.dat file of which first 17 are jaw line landmarks.
We use jaw line landmarks and the top-left and top-right corners of the face rectangle. 
The points discussed above are used in a openCV function fillPoly to extract the face.
Next all the channels are split in the image and a new channel(alpha channel) is created and will merge all the channels making
into 4 channels (R,B,G,Alpha)
Saving the resultant image in a PNG format will give the required output.
